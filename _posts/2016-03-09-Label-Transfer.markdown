---
layout: post
title:  "Label Transfer"
date:   2016-03-09
---

# Network architecture
    (100x100x3) input -> 5 x (3x3) -> deconv 5 x (3x3) -> (100x100x1) output

## First phase:

We begin by training the network using 400 synthetic images (the training set), using a batch size of 10. A validation set of 100 synthetic is reserved.

<figure>
  <a href="/assets/transfer/trainingcurve1.png">
    <img class="preds" src='/assets/transfer/trainingcurve1.png' alt='missing' />
  </a>
</figure>

By visual inspection, the network parameters that performed best on the real images occurred at around epoch 225. A snapshot of the corresponding outputs is shown below, and compared a "naive" that simply converts the input image to greyscale.
<figure>
  <a href="/assets/transfer/225__testpreds.png">
    <img class="preds" src='/assets/transfer/225__testpreds.png' alt='missing' />
  </a>
</figure>


