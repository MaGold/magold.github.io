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

- batch size: 128
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



# Reconstructions when 9/10 middle units set to 0

<section class="turnoffgrid">
    <div>
        <figure>
            <a href="/assets/turnoff/0_onekept.png">
                <img class="l1" src='/assets/turnoff/0_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/1_onekept.png">
                <img class="l2" src='/assets/turnoff/1_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/2_onekept.png">
                <img class="l3" src='/assets/turnoff/2_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/3_onekept.png">
                <img class="l1" src='/assets/turnoff/3_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
</section>

<section class="turnoffgrid">
    <div>
        <figure>
            <a href="/assets/turnoff/4_onekept.png">
                <img class="l2" src='/assets/turnoff/4_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/5_onekept.png">
                <img class="l3" src='/assets/turnoff/5_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/6_onekept.png">
                <img class="l1" src='/assets/turnoff/6_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/7_onekept.png">
                <img class="l2" src='/assets/turnoff/7_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
</section>

<section class="turnoffgrid">
    <div>
        <figure>
            <a href="/assets/turnoff/8_onekept.png">
                <img class="l3" src='/assets/turnoff/8_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/9_onekept.png">
                <img class="l1" src='/assets/turnoff/9_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
 </section>



# Reconstructions when 1/10 middle units set to 0

<section class="turnoffgrid">
    <div>
        <figure>
            <a href="/assets/turnoff/0_onegone.png">
                <img class="l1" src='/assets/turnoff/0_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/1_onegone.png">
                <img class="l2" src='/assets/turnoff/1_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/2_onegone.png">
                <img class="l3" src='/assets/turnoff/2_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/3_onegone.png">
                <img class="l1" src='/assets/turnoff/3_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
</section>

<section class="turnoffgrid">
    <div>
        <figure>
            <a href="/assets/turnoff/4_onegone.png">
                <img class="l2" src='/assets/turnoff/4_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/5_onegone.png">
                <img class="l3" src='/assets/turnoff/5_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/6_onegone.png">
                <img class="l1" src='/assets/turnoff/6_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/7_onegone.png">
                <img class="l2" src='/assets/turnoff/7_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
</section>

<section class="turnoffgrid">
    <div>
        <figure>
            <a href="/assets/turnoff/8_onegone.png">
                <img class="l3" src='/assets/turnoff/8_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoff/9_onegone.png">
                <img class="l1" src='/assets/turnoff/9_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
 </section>
