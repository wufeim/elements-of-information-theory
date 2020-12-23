2.1 Entropy
=====================================

Entropy is a measure of the uncertainty of a random variable. Let :math:`X` be a discrete random variable with alphabet :math:`\mathcal{X}` and probability mass function :math:`p(x) = \Pr\{X = x\}`, :math:`x \in \mathcal{X}`.

**Definition.** The **entropy** :math:`H(X)` of a discrete random variable :math:`X` is defined by

.. math::

   H(X) = - \sum_{x \in \mathcal{X}} p(x) \log p(x)

The log is to the base :math:`2` and entropy is expressed in bits.

We denote the expectation by :math:`E`. The expected value of the random variable :math:`g(X)` is written

.. math::

   E_pg(X) = \sum_{x \in \mathcal{X}} g(x)p(x)

We shall take a peculiear interest in the eerily self-referential expectation of :math:`g(X)` when :math:`g(X) = \log \frac{1}{p(X)}`.

**Remark.** The entropy of :math:`X` can also be interpreted as the expected value of the random variable :math:`\log \frac{1}{p(X)}`. Thus,

.. math::

   H(X) = E_p \log \frac{1}{p(X)}

**Lemma 2.1.1.** :math:`H(X) \geq 0`.

**Lemma 2.1.2.** :math:`H_b(X) = (\log_b a)H_a(X)`.
