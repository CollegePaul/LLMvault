### Logic and Proofs in Mathematics

Logic and proofs are fundamental aspects of mathematics that form the basis of mathematical reasoning and argumentation. At its core, logic involves understanding and using rules of inference to draw conclusions from given statements or premises.

**Basic Concepts:**

1. **Statements:** These are declarative sentences that can be either true or false, but not both. For example, "$$2 + 2 = 4$$" is a statement that is true.

2. **Logical Connectives:** These are used to combine simple statements into more complex ones. Common logical connectives include:
   - **AND ($$\wedge$$):** Both statements must be true for the combined statement to be true.
     Example: "It is raining AND I am carrying an umbrella."
   - **OR ($$\vee$$):** At least one of the statements must be true for the combined statement to be true.
     Example: "I will eat pizza OR pasta tonight."
   - **NOT ($$\neg$$):** This negates a statement, making it false if it was true and vice versa.
     Example: "It is NOT raining."

3. **Implication:** This connects two statements where one (the hypothesis) implies the other (the conclusion).
   Example: "If I study hard (hypothesis), then I will pass my exam (conclusion)." 
   Symbolically, this can be written as $$P \rightarrow Q$$.

4. **Contrapositive:** A related statement that is logically equivalent to the original implication.
   Example: The contrapositive of "If I study hard, then I will pass my exam" is "If I do not pass my exam, then I did not study hard."
   Symbolically, this can be written as $$\neg Q \rightarrow \neg P$$.

**Basic Examples of Proofs:**

1. **Direct Proof:** This involves directly proving the conclusion from the premises using logical steps.
   Example: Prove that if n is an even integer, then $$n^2$$ is also an even integer.
     - Let $$n = 2k$$ for some integer k (since n is even).
     - Then $$n^2 = (2k)^2 = 4k^2 = 2(2k^2)$$, which is of the form $$2m$$ where $$m=2k^2$$.
     - Therefore, $$n^2$$ is an even integer.

2. **Proof by Contradiction:** This method assumes the opposite of what you are trying to prove and shows that this leads to a contradiction.
   Example: Prove that $$\sqrt{2}$$ is irrational.
     - Assume $$\sqrt{2}$$ is rational, so $$\sqrt{2} = \frac{p}{q}$$ where p and q have no common factors ($$\frac{p}{q}$$ is in lowest terms).
     - Then $$2 = \frac{p^2}{q^2}$$, so $$p^2 = 2q^2$$. This means $$p^2$$ is even, hence p must be even.
     - Let $$p = 2r$$ for some integer r. Then $$4r^2 = 2q^2$$, or $$q^2 = 2r^2$$, making $$q^2$$ (and thus q) even too.
     - This contradicts our initial assumption that p and q have no common factors.

3. **Proof by Induction:** This method is used to prove statements about natural numbers.
   Example: Prove that the sum of the first n positive integers is $$\frac{n(n+1)}{2}$$.
     - Base Case (n=1): $$1 = \frac{1(1+1)}{2}$$, which is true.
     - Inductive Step: Assume the statement holds for some k, i.e., $$1 + 2 + ... + k = \frac{k(k+1)}{2}$$.
       Show it holds for k+1: $$1 + 2 + ... + k + (k+1) = \frac{k(k+1)}{2} + (k+1)$$
                             $$= \frac{k^2 + k + 2k + 2}{2}$$
                             $$= \frac{(k+1)(k+2)}{2}$$, which is the formula for n=k+1.

By understanding and applying these concepts and techniques, mathematicians can construct rigorous arguments and verify mathematical truths. #Logic and Proofs #Maths