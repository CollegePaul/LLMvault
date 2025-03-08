### Integration Test in Python

Integration testing is a level of software testing where individual units or components of an application are combined and tested as a group. The purpose is to ensure that different parts of an application work together correctly, detecting any issues that may arise from their interactions.

In the context of Python, integration tests often involve checking how modules or services interact with each other, possibly including external systems like databases, APIs, or file systems. Unlike unit tests which focus on small isolated pieces of code, integration tests consider larger parts of the system to validate complex behavior and data flows.

#### Example: Testing a Simple Service Interaction

Suppose you have two services in your application: `OrderService` and `InventoryService`. The `OrderService` is responsible for creating orders, while the `InventoryService` manages stock levels. When an order is created, it should also decrement the inventory count for the ordered items.

Here's a simplified example to demonstrate how these services might be tested together:

```python
# order_service.py
class OrderService:
    def __init__(self, inventory_service):
        self.inventory_service = inventory_service

    def create_order(self, item_id, quantity):
        if self.inventory_service.check_stock(item_id) >= quantity:
            self.inventory_service.decrement_stock(item_id, quantity)
            return {"order_id": 123, "item_id": item_id, "quantity": quantity}
        else:
            raise ValueError("Insufficient stock")

# inventory_service.py
class InventoryService:
    def __init__(self):
        self.stock = {1: 10, 2: 5}

    def check_stock(self, item_id):
        return self.stock.get(item_id, 0)

    def decrement_stock(self, item_id, quantity):
        if self.stock[item_id] >= quantity:
            self.stock[item_id] -= quantity
        else:
            raise ValueError("Stock level too low")

# test_integration.py
import unittest
from order_service import OrderService
from inventory_service import InventoryService

class TestOrderAndInventoryIntegration(unittest.TestCase):
    def setUp(self):
        self.inventory = InventoryService()
        self.order_service = OrderService(self.inventory)

    def test_create_order_success(self):
        result = self.order_service.create_order(1, 2)
        self.assertEqual(result["order_id"], 123)
        self.assertEqual(result["item_id"], 1)
        self.assertEqual(result["quantity"], 2)
        self.assertEqual(self.inventory.check_stock(1), 8)

    def test_create_order_insufficient_stock(self):
        with self.assertRaises(ValueError) as context:
            self.order_service.create_order(2, 6)
        self.assertTrue("Insufficient stock" in str(context.exception))
        self.assertEqual(self.inventory.check_stock(2), 5)

if __name__ == '__main__':
    unittest.main()
```

In this example:
- `OrderService` and `InventoryService` are two separate services.
- The integration test `TestOrderAndInventoryIntegration` verifies that creating an order correctly interacts with the inventory service, updating stock levels as expected.

#Integration test #Python