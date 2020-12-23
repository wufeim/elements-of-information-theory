2.2 Joint Entropy and Conditional Entropy
=====================================

**Definition.** The **joint entropy** :math:`H(X, Y)` of a pair of discrete random variables :math:`(X, Y)` with a joint distribution :math:`p(x, y)` is defined as

.. math::

   H(X, Y) = - \sum_{x \in \mathcal{X}} \sum_{y \in \mathcal{Y}} p(x, y) \log p(x, y) = - E \log p(X, Y)

**Definition.** If :math:`(X, Y) \sim p(x, y)`, the **conditional entropy** :math:`H(Y \mid X)` is defined as

.. math::

   H(Y \mid X) & = \sum_{x \in \mathcal{X}} p(x) H(Y \mid X = x) \\
   & = - \sum_{x \in \mathcal{X}} p(x) \sum_{y \in \mathcal{Y}} p(y \mid x) \log p(y \mid x) \\
   & = - \sum_{x \in \mathcal{X}}\sum_{y \in \mathcal{Y}} p(x, y) \log p(y \mid x) \\
   & = - E \log p(Y \mid X)

**Theorem 2.2.1 (Chain Rule).** :math:`H(X, Y) = H(X) + H(Y \mid X)`.

**Corollary.** :math:`H(X, Y \mid X) = H(X \mid X) + H(Y \mid X, Z)`.

**Remark.** Note that

.. math::

   & H(Y \mid X) \neq H(X \mid Y) \\
   & H(X) - H(X \mid Y) = H(Y) - H(Y \mid X)
