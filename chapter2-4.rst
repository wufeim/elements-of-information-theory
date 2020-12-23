2.4 Relationship Between Entropy and Mutual Information
=====================================

The mutual information :math:`I(X; Y)` can be rewritten as

.. math::

   I(X; Y) & = \sum_{x, y} p(x, y) \log \frac{p(x, y)}{p(x)p(y)} \\
   & = \sum_{x, y} p(x, y) \log \frac{p(x \mid y)}{p(x)} \\
   & = - \sum_{x, y} p(x, y) \log p(x) + \sum_{x, y} p(x, y) \log p(x \mid y) \\
   & = H(X) - H(X \mid Y)

Thus, the mutual information :math:`I(X; Y)` is the reduction in the uncertainty of :math:`X` due to the knowledge of :math:`Y`.

**Theorem 2.4.1 (Mutual information and entropy).**

.. math::

   I(X; Y) & = H(X) - H(X \mid Y) \\
   I(X; Y) & = H(Y) - H(Y \mid X) \\
   I(X; Y) & = H(X) + H(Y) - H(X, Y) \\
   I(X; Y) & = I(Y; X) \\
   I(X; X) & = H(X)
