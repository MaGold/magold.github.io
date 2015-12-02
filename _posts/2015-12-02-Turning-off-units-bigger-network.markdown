---
layout: post
title:  "The effect of turning off units in the middle layer (6 layers)"
date:   2015-11-18
categories: mnist autoencoder
---



# Autoencoder Architecture

    784 -> 529 -> 225 -> 10 -> 225 -> 529 ->  784

Non-linearities are `relu`. Weights are not tied.

# Training

- batch size: 128
- learning rate: 0.001 using RMSProp
- loss function: mean squared error
- trained for 1000 epochs

# Reconstructions with all units on

<figure>
    <a href="/assets/turnoffbig/reconstructions.png">
        <img class="smallreconstructions" src='/assets/turnoffbig/reconstructions.png' alt='missing' />
    </a>
</figure>



# Reconstructions when 9/10 middle units set to 0

<section class="turnoffgrid">
    <div>
        <figure>
            <a href="/assets/turnoffbig/0_onekept.png">
                <img class="l1" src='/assets/turnoffbig/0_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoffbig/1_onekept.png">
                <img class="l2" src='/assets/turnoffbig/1_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoffbig/2_onekept.png">
                <img class="l3" src='/assets/turnoffbig/2_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoffbig/3_onekept.png">
                <img class="l1" src='/assets/turnoffbig/3_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
</section>

<section class="turnoffgrid">
    <div>
        <figure>
            <a href="/assets/turnoffbig/4_onekept.png">
                <img class="l2" src='/assets/turnoffbig/4_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoffbig/5_onekept.png">
                <img class="l3" src='/assets/turnoffbig/5_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoffbig/6_onekept.png">
                <img class="l1" src='/assets/turnoffbig/6_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoffbig/7_onekept.png">
                <img class="l2" src='/assets/turnoffbig/7_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
</section>

<section class="turnoffgrid">
    <div>
        <figure>
            <a href="/assets/turnoffbig/8_onekept.png">
                <img class="l3" src='/assets/turnoffbig/8_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoffbig/9_onekept.png">
                <img class="l1" src='/assets/turnoffbig/9_onekept.png' alt='missing' />
            </a>
        </figure>
    </div>
 </section>



# Reconstructions when 1/10 middle units set to 0

<section class="turnoffgrid">
    <div>
        <figure>
            <a href="/assets/turnoffbig/0_onegone.png">
                <img class="l1" src='/assets/turnoffbig/0_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoffbig/1_onegone.png">
                <img class="l2" src='/assets/turnoffbig/1_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoffbig/2_onegone.png">
                <img class="l3" src='/assets/turnoffbig/2_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoffbig/3_onegone.png">
                <img class="l1" src='/assets/turnoffbig/3_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
</section>

<section class="turnoffgrid">
    <div>
        <figure>
            <a href="/assets/turnoffbig/4_onegone.png">
                <img class="l2" src='/assets/turnoffbig/4_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoffbig/5_onegone.png">
                <img class="l3" src='/assets/turnoffbig/5_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoffbig/6_onegone.png">
                <img class="l1" src='/assets/turnoffbig/6_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoffbig/7_onegone.png">
                <img class="l2" src='/assets/turnoffbig/7_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
</section>

<section class="turnoffgrid">
    <div>
        <figure>
            <a href="/assets/turnoffbig/8_onegone.png">
                <img class="l3" src='/assets/turnoffbig/8_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
    <div>
        <figure>
            <a href="/assets/turnoffbig/9_onegone.png">
                <img class="l1" src='/assets/turnoffbig/9_onegone.png' alt='missing' />
            </a>
        </figure>
    </div>
 </section>
