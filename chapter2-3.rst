2.3 Relative Entropy and Mutual Information
=====================================

The relative entropy :math:`D(p \mid\mid q)` is a measure of the distance between two distributions. It measures the inefficiency of assuming that the distribution is :math:`q` when the true distribution is :math:`p`.

**Definition.** The **relative entropy** or **Kullback-Leibler distance** between two probability mass functions :math:`p(x)` and :math:`q(x)` is defined as

.. math::

   D(p \mid\mid q) = \sum_{x \in \mathcal{X}} p(x) \log \frac{p(x)}{q(x)} = E_p \log \frac{p(X)}{q(X)}

It is not a true distance between distributions since it is not symmetric and does not satisfy the triangle inequality.

**Definition.** Consider two random variables :math:`X` and :math:`Y` with a joint probability mass function :math:`p(x, y)` and marginal probability mass functions :math:`p(x)` and :math:`p(y)`. The **mutual information** :math:`I(X; Y)` is the relative entropy between the joint distribution and the product distribution :math:`p(x)p(y)`:

.. math::

   I(X; Y) & = \sum_{x \in \mathcal{X}} \sum_{y \in \mathcal{Y}} p(x, y) \log \frac{p(x, y)}{p(x)p(y)} \\
   & = D(p(x, y) \mid\mid p(x)p(y)) \\
   & = E_{p(x, y)} \log \frac{p(X, Y)}{p(X)p(Y)}
