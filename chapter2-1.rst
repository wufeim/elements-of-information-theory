2.1 Entropy
=====================================

Entropy is a measure of the uncertainty of a random variable. Let :math:`X` be a discrete random variable with alphabet :math:`\mathcal{X}` and probability mass function :math:`p(x) = \Pr\{X = x\}`, :math:`x \in \mathcal{X}`.

**Definition.** The **entropy** :math:`H(X)` of a discrete random variable :math:`X` is defined by

.. math::

   H(X) = - \sum_{x \in \mathcal{X}} p(x) \log p(x)
