---
layout: post
title:  "The effect of turning off units in the middle layer"
date:   2015-11-18
categories: mnist autoencoder
---



# Autoencoder Architecture

    784 -> 225 -> 10 -> 225 -> 784

Non-linearities are `relu`. Weights are not tied.

# Training

- batch size: 256
- learning rate: 0.001 using RMSProp
- loss function: mean squared error
- trained for 100 epochs

# Filters (first layer)

<figure>
    <a href="/assets/turnoff/layer1_filters.png">
        <img class="bigfilters" src='/assets/turnoff/layer1_filters.png' alt='missing' />
    </a>
</figure>

# Reconstructions with all units on

<figure>
    <a href="/assets/turnoff/reconstructions.png">
        <img class="smallreconstructions" src='/assets/turnoff/reconstructions.png' alt='missing' />
    </a>
</figure>



# Reconstructions when all but one middle units are set to 0

<section class="turnoffgrid">
    <div>
        <figure>
            <a href="/assets/turnoff/0_blackout.png">
                <img class="l1" src='/assets/turnoff/0_blackout.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/1_blackout.png">
                <img class="l2" src='/assets/turnoff/1_blackout.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/2_blackout.png">
                <img class="l3" src='/assets/turnoff/2_blackout.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/3_blackout.png">
                <img class="l1" src='/assets/turnoff/3_blackout.png' alt='missing' />
            </a>
        </figure>
    </div>
</section>

<section class="turnoffgrid">
    <div>
        <figure>
            <a href="/assets/turnoff/4_blackout.png">
                <img class="l2" src='/assets/turnoff/4_blackout.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/5_blackout.png">
                <img class="l3" src='/assets/turnoff/5_blackout.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/6_blackout.png">
                <img class="l1" src='/assets/turnoff/6_blackout.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/7_blackout.png">
                <img class="l2" src='/assets/turnoff/7_blackout.png' alt='missing' />
            </a>
        </figure>
    </div>
</section>

<section class="turnoffgrid">
    <div>
        <figure>
            <a href="/assets/turnoff/8_blackout.png">
                <img class="l3" src='/assets/turnoff/8_blackout.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/9_blackout.png">
                <img class="l1" src='/assets/turnoff/9_blackout.png' alt='missing' />
            </a>
        </figure>
    </div>
 </section>
<!--
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

-->