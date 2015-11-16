---
layout: post
title:  "Convolutional Autoencoder - MNIST"
date:   2015-11-13 11:33:55 -0500
categories: mnist
---

# Comparing 4 convolutional autoencoder architectures:

1. **Single layer convolutional autoencoder**:

        input -> 100 x (17x17) -> pool -> upsample -> deconv -> output

2. **Single layer _denoising_ convolutional autoencoder**:

        (noisy) input -> 100 x (17x17) -> pool -> upsample -> deconv -> output

3. **Two layer convolutional autoencoder, (CE cost function)**:

        input -> 100 x (17x17) -> pool -> 32 x (3x3) -> pool ->
        -> upsample -> deconv -> upsample -> deconv -> output

4. **Two layer convolutional autoencoder, (MSE cost function)**:

        input -> 100 x (17x17) -> pool -> 32 x (3x3) -> pool ->
        -> upsample -> deconv -> upsample -> deconv -> output

# Training

<table class="tables">
  <thead>
    <tr>
      <th></th>
      <th>(1) Single layer network</th>
      <th>(2) Single layer denoising network</th>
      <th>(3) Two layer network</th>
      <th>(4) Two layer network</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Epochs</td>
      <td>400</td>
      <td>400</td>
      <td>400</td>
      <td>400</td>
    </tr>
    <tr>
      <td>Training time</td>
      <td>3.5 hours</td>
      <td>4.5 hours</td>
      <td>7 hours</td>
      <td>7 hours</td>
    </tr>
    <tr>
      <td>Batch size</td>
      <td>50</td>
      <td>50</td>
      <td>50</td>
       <td>50</td>
    </tr>
    <tr>
      <td>Learning rate</td>
      <td>0.005</td>
      <td>0.005</td>
      <td>0.005</td>
      <td>0.005</td>
    </tr>
    <tr>
      <td>Momentum</td>
      <td>0.9</td>
      <td>0.9</td>
      <td>0.9</td>
      <td>0.9</td>
    </tr>
    <tr>
      <td>Regularization</td>
      <td>none</td>
      <td>none</td>
      <td>none</td>
      <td>none</td>
    </tr>
    <tr>
      <td>Loss function</td>
      <td>Cross-entropy</td>
      <td>Cross-entropy</td>
      <td>Cross-entropy</td>
      <td>MSE</td>
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
                <figcaption>(1)</figcaption>
                <img class="preds" src='/assets/onelayer-predictions.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="middle">
        <figure>
            <a href="/assets/twolayer-predictions.png">
                <figcaption>(2)</figcaption>
                <img class="preds" src='/assets/onelayernoise-predictions.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="right">
        <figure>
            <a href="/assets/twolayer-predictions.png">
                <figcaption>(3)</figcaption>
                <img class="preds" src='/assets/twolayer-predictions.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="right">
        <figure>
            <a href="/assets/twolayermse-predictions.png">
                <figcaption>(4)</figcaption>
                <img class="preds" src='/assets/twolayermse-predictions.png' alt='missing' />
            </a>
        </figure>
    </div>
</section>

#Filters (first layer only):
<section class="reconstructions">
    <!--div class="head">
    Reconstructions
    </div-->
    <div class="left">
        <figure>
            <a href="/assets/onelayer-filters.png">
                <figcaption>(1)</figcaption>
                <img class="filters" src='/assets/onelayer-filters.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="middle">
        <figure>
            <a href="/assets/onelayernoise-filters.png">
                <figcaption>(2)</figcaption>
                <img class="filters" src='/assets/onelayernoise-filters.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="right">
        <figure>
            <a href="/assets/twolayer-filters.png">
                <figcaption>(3)</figcaption>
                <img class="filters" src='/assets/twolayer-filters.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="right">
        <figure>
            <a href="/assets/twolayermse-filters.png">
                <figcaption>(4)</figcaption>
                <img class="filters" src='/assets/twolayermse-filters.png' alt='missing' />
            </a>
        </figure>
    </div>
</section>



#Can they reconstruct noise? (Are they learning the identity function?)

<section class="reconstructions">
    <!--div class="head">
    Reconstructions
    </div-->
    <div class="left">
        <figure>
            <a href="/assets/onelayer-identity.png">
                <figcaption>(1)</figcaption>
                <img class="preds" src='/assets/onelayer-identity.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="middle">
        <figure>
            <a href="/assets/twolayer-identity.png">
                <figcaption>(2)</figcaption>
                <img class="preds" src='/assets/onelayernoise-identity.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="right">
        <figure>
            <a href="/assets/twolayer-identity.png">
                <figcaption>(3)</figcaption>
                <img class="preds" src='/assets/twolayer-identity.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="right">
        <figure>
            <a href="/assets/twolayermse-identity.png">
                <figcaption>(4)</figcaption>
                <img class="preds" src='/assets/twolayermse-identity.png' alt='missing' />
            </a>
        </figure>
    </div>

</section>
