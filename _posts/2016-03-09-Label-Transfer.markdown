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

By visual inspection, the network parameters that performed best on the real images occurred at around epoch 225. A snapshot of the corresponding outputs is shown below, and compared with a "naive" algorithm that simply converts the input image to greyscale.
<figure>
  <a href="/assets/transfer/225__testpreds.png">
    <img class="preds" src='/assets/transfer/225__testpreds.png' alt='missing' />
  </a>
</figure>


## Second phase:

In the second phase, we retrain the network with an augmented training set consisting of 400 labeled synthetics images, plus 40 real images, which now have labels coming from the previous phase. Training on this augmented data set doesn't seem to make much of a difference. Below are sample outputs from the inital network, and the network after 500 epochs:

<figure>
<figcaption>Before training:</figcaption>
  <a href="/assets/transfer/phase2_000.png">
    <img class="preds" src='/assets/transfer/phase2_000.png' alt='missing' />
  </a>
</figure>

<figure>
<figcaption>After 500 epochs:</figcaption>
  <a href="/assets/transfer/phase2_500.png">
    <img class="preds" src='/assets/transfer/phase2_500.png' alt='missing' />
  </a>
</figure>


