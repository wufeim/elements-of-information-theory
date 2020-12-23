2.5 Chain Rules for Entropy, Relative Entropy, and Mutual Information
=====================================

**Theorem 2.5.1 (Chain rule for entropy).** Let :math:`X_1, \dots, X_n` be drawn according to :math:`p(x_1, \dots, x_n)`. Then

.. math::

   H(X_1, \dots, X_n) = \sum_{i=1}^n H(X_i \mid X_{i-1}, \dots, X_1)

**Definition.** The **conditional mutual information** of random variables :math:`X` and :math:`Y` given :math:`Z` is defined by

.. math::

   I(X; Y \mid Z) & = H(X \mid Z) - H(X \mid Y, Z) \\
   & = E_{p(x, y, z)} \log \frac{p(X, Y \mid Z)}{p(X \mid Z)p(Y \mid Z)}

**Theorem 2.5.2 (Chain rule for information).**

.. math::

   I(X_1, \dots, X_n; Y) = \sum_{i=1}^n I(X_i; Y \mid X_{i-1}, \dots, X_1)

**Definition.** For joint probability mass functions :math:`p(x, y)` and :math:`q(x, y)`, the **conditional relative entropy** :math:`D(p(y \mid x) \mid\mid q(y \mid x))` is the average of the relative entropies between the conditional probability mass functions :math:`p(y \mid x)` and :math:`q(y \mid x)` averaged over the probability mass function :math:`p(x)`. More precisely,

.. math::

   D(p(y \mid x) \mid\mid q(y \mid x)) & = \sum_x p(x) \sum_y p(y \mid x) \log \frac{p(y\mid x)}{q(y \mid x)} \\
   & = E_{p(x, y)} \log \frac{p(Y \mid X)}{q(Y \mid X)}

**Theorem 2.5.3 (Chain rule for relative entropy).**

.. math::

   D(p(x, y) \mid\mid q(x, y)) = D(p(x) \mid\mid q(x)) + D(p(y \mid x) \mid\mid q(y \mid x))
