### Signals in Django

In Django, signals are used to decouple applications by sending notifications when actions occur elsewhere in the framework. Essentially, signals allow certain senders to notify a set of receivers that some action has taken place. They are particularly useful for creating modular and reusable components.

Django provides several built-in signals that you can use in your applications, such as `pre_save`, `post_save`, `pre_delete`, and `post_delete`. These signals are sent before or after models’ save or delete methods are called.

For example, if you want to automatically generate a thumbnail for an uploaded image every time an Image model instance is saved, you can use the `post_save` signal. Here's how you might implement this:

```python
from django.db.models.signals import post_save
from django.dispatch import receiver
from .models import Image

@receiver(post_save, sender=Image)
def generate_thumbnail(sender, instance, created, **kwargs):
    if created:
        # Logic to create a thumbnail for the image
        print("Generating thumbnail for new image")
```

In this example, `generate_thumbnail` is a receiver function that will be called every time an instance of the Image model is saved. The `@receiver` decorator connects the `post_save` signal to the `Image` model.

#Signals #Django