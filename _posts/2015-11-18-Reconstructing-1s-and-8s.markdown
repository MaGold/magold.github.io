---
layout: post
title:  "Reconstructing 1s and 8s (MNIST)"
date:   2015-11-18
categories: mnist convolutional-autoencoder
---



# Convolutional Autoencoder Architecture

    input -> conv 20x(17x17) -> conv 2x(11x11) ->
          -> deconv 2x(11x11) -> deconv 20x(17x17) -> output

Non-linearities (`tanh`) follow each of the convolutional and each of the deconvolutional layers. Convolution and deconvolution weights are tied. No pooling was used.

# Training

Approximately 10,000 images of only 1s and 8s were used to train the network for 300 epochs (~2 hours). Other parameters:

- batch size: 64
- learning rate: 0.005
- momentum: 0.9
- loss function: mean squared error

# Feature map sizes:

The inputs images were scaled up from 28x28 to 36x36. This gives us the following feature map sizes:

    (36x36) -> 20x(20x20) -> 2x(10x10) -> 20x(20x20) -> (36x36)

# Filters

<section class="filtersection">
    <div class="blank">&nbsp;
    </div>
    <div class="left">
        <figure>
            <a href="/assets/1s8s/layer1_filters.png">
                <figcaption>Layer 1</figcaption>
                <img class="l1" src='/assets/1s8s/layer1_filters.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="right">
        <figure>
            <a href="/assets/1s8s/layer2_filters.png">
                <figcaption>Layer 2</figcaption>
                <img class="l2" src='/assets/1s8s/layer2_filters.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="blank">&nbsp;
    </div>
</section>

# Sample Activations (1)

<section class="activationsection">
    <div class="l1">
        <figure>
            <a href="/assets/1s8s/layer0_A.png">
                <figcaption>Input</figcaption>
                <img class="l1" src='/assets/1s8s/layer0_A.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="l2">
        <figure>
            <a href="/assets/1s8s/layer1_A.png">
                <figcaption>Layer 1</figcaption>
                <img class="l2" src='/assets/1s8s/layer1_A.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="l3">
        <figure>
            <a href="/assets/1s8s/layer2_A.png">
                <figcaption>Layer 2</figcaption>
                <img class="l3" src='/assets/1s8s/layer2_A.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="l4">
        <figure>
            <a href="/assets/1s8s/layer3_A.png">
                <figcaption>Layer 3</figcaption>
                <img class="l4" src='/assets/1s8s/layer3_A.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="l5">
        <figure>
            <a href="/assets/1s8s/layer4_A.png">
                <figcaption>Output</figcaption>
                <img class="l5" src='/assets/1s8s/layer4_A.png' alt='missing' />
            </a>
        </figure>
    </div>

</section>

# Sample Activations (8)

<section class="activationsection">
    <div class="l1">
        <figure>
            <a href="/assets/1s8s/layer0_B.png">
                <figcaption>Input</figcaption>
                <img class="l1" src='/assets/1s8s/layer0_B.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="l2">
        <figure>
            <a href="/assets/1s8s/layer1_B.png">
                <figcaption>Layer 1</figcaption>
                <img class="l2" src='/assets/1s8s/layer1_B.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="l3">
        <figure>
            <a href="/assets/1s8s/layer2_B.png">
                <figcaption>Layer 2</figcaption>
                <img class="l3" src='/assets/1s8s/layer2_B.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="l4">
        <figure>
            <a href="/assets/1s8s/layer3_B.png">
                <figcaption>Layer 3</figcaption>
                <img class="l4" src='/assets/1s8s/layer3_B.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div class="l5">
        <figure>
            <a href="/assets/1s8s/layer4_B.png">
                <figcaption>Output</figcaption>
                <img class="l5" src='/assets/1s8s/layer4_B.png' alt='missing' />
            </a>
        </figure>
    </div>

</section>