1.1 Preview of the Book
=====================================

The initial questions treated by information theory lay in the areas of data compression and transmission. The answers are quantities such as entropy and mutual information.

The **entropy** of a random variable :math:`X` with a probability mass function :math:`p(x)` is defined by

.. math::

   H(X) = -\sum_x p(x) \log_2 p(x)

The entropy is a measure of the average uncertainty in the random variable, and is the number of bits on average required to describe the random variable.

We can define conditional entropy :math:`H(X \mid Y)`, which is the entropy of a random variable conditional on the knowledge of another random variable. The reduction in uncertainty due to another random variable is called the **mutual information**:

.. math::

   I(X; Y) = I(Y; X) = H(X) - H(X \mid Y) = \sum_{x, y} p(x, y) \log \frac{p(x, y)}{p(x) p(y)}

A **communication channel** is a system in which the output depends probabilistically on its input. For a communication channel with input :math:`X` and output :math:`Y`, we can define the capacity :math:`C` by

.. math::

   C = \max_{p(x)} I(X; Y)

Mutual information turns out to be a special case of a more general quantity called **relative entropy** :math:`D(p \mid\mid q)`, which is a measure of the "distance" between two probability mass functions :math:`p` and :math:`q`. It is defined as

.. math::

   D(p \mid\mid q) = \sum_x p(x)\log \frac{p(x)}{q(x)}

Relative entropy can be used to define a geometry for probability distributions that allows us to interpret many of the results of large deviation theory.

----

The quantities :math:`H, I, C, D, K, W` arise naturally in the following areas:

- **Data compression.** The entropy :math:`H` of a random variable is a lower bound on the average length of the shortest description of a random variable. If we relax the constraint of recovering the source perfectly, we can then ask what communication rates are required to describe the source up to distortion :math:`D`? When we try to formalize the notion of the shortest description for nonrandom objects, we are led to the definition of **Kolmogorov complexity** :math:`K`.
- **Inference.** We can use the notion of Kolmogorov complexity :math:`K` to find the shortest description of the data and use that as a model to predict what comes next. A model that maximizes the uncertainty or entropy yields the maximum entropy approach to inference.
