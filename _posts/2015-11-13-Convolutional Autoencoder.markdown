---
layout: post
title:  "Convolutional Autoencoder - MNIST"
date:   2015-11-13 11:33:55 -0500
categories: mnist
---

# Comparing two convolutional autoencoder architectures:

**Single layer convolutional autoencoder**:

    input -> 100 x (17x17) -> pool -> upsample -> deconv -> output

**Two layer convolutional autoencoder**:

    input -> 100 x (17x17) -> pool -> 36 x (3x3) -> pool ->
    -> upsample -> deconv -> upsample -> deconv -> output

# Training

<table class="tables">
  <thead>
    <tr>
      <th></th>
      <th>Single layer network</th>
      <th>Two layer network</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Epochs</td>
      <td>400</td>
      <td>400</td>
    </tr>
    <tr>
      <td>Training time</td>
      <td>3.5 hours</td>
      <td>7 hours</td>
    </tr>
    <tr>
      <td>Batch size</td>
      <td>50</td>
      <td>50</td>
    </tr>
    <tr>
      <td>Learning rate</td>
      <td>0.005</td>
      <td>0.005</td>
    </tr>
    <tr>
      <td>Momentum</td>
      <td>0.9</td>
      <td>0.9</td>
    </tr>
  </tbody>
</table>


#Reconstructions
<section class="reconstructions">
    <!--div class="head">
    Reconstructions
    </div-->
    <div class="left">
        <figure>
            <a href="/assets/onelayer-predictions.png">
                <figcaption>Single Layer Reconstructions</figcaption>
                <img class="preds" src='/assets/onelayer-predictions.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="right">
        <figure>
            <a href="/assets/twolayer-predictions.png">
                <figcaption>Two Layer Reconstructions</figcaption>
                <img class="preds" src='/assets/twolayer-predictions.png' alt='missing' />
            </a>
        </figure>
    </div>
</section>

#Filters:
<section class="reconstructions">
    <!--div class="head">
    Reconstructions
    </div-->
    <div class="left">
        <figure>
            <a href="/assets/onelayer-filters.png">
                <figcaption>Single Layer Filters</figcaption>
                <img class="preds" src='/assets/onelayer-filters.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="right">
        <figure>
            <a href="/assets/twolayer-filters.png">
                <figcaption>Two Layer Filters (first layer)</figcaption>
                <img class="preds" src='/assets/twolayer-filters.png' alt='missing' />
            </a>
        </figure>
    </div>
</section>



#Can they reconstruct noise?
<section class="reconstructions">
    <!--div class="head">
    Reconstructions
    </div-->
    <div class="left">
        <figure>
            <a href="/assets/onelayer-identity.png">
                <figcaption>Single Layer Reconstructions</figcaption>
                <img class="preds" src='/assets/onelayer-identity.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="right">
        <figure>
            <a href="/assets/twolayer-identity.png">
                <figcaption>Two Layer Reconstructions</figcaption>
                <img class="preds" src='/assets/twolayer-identity.png' alt='missing' />
            </a>
        </figure>
    </div>
</section>
