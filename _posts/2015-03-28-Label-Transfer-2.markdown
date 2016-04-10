---
layout: post
title:  "Label Transfer 2"
date:   2016-03-28
---

# Network architecture
    (100x100x3) input -> 20 x (3x3) -> deconv 20 x (3x3) -> (100x100x1) output

# Training details

- Training set: 800 synthetic images (plain water and water with rocks
- Test set: 200 synthetic images (plain water and water with rocks)
- Batch size: 64
- Training time: 1000 epochs took about 3 hours on the gpu cluster

# Training curve

<figure>
  <a href="/assets/transfer2/costs.png">
    <img class="preds" src='/assets/transfer2/costs.png' alt='missing' />
  </a>
</figure>


# Image results

The results look pretty good on both the synthetic data and the real videos. Here are some sample outputs after 1000 epochs:

Training set:
<figure>
  <a href="/assets/transfer2/999__preds.png">
    <img class="preds" src='/assets/transfer2/999__preds.png' alt='missing' />
  </a>
</figure>

Test set:
<figure>
  <a href="/assets/transfer2/999__testpreds.png">
    <img class="preds" src='/assets/transfer2/999__testpreds.png' alt='missing' />
  </a>
</figure>

# Video results (click for youtube video)

Sample output after 200 epochs:
<a href="https://www.youtube.com/watch?v=L0S6rrEj0KE" target="_blank"><img src="http://img.youtube.com/vi/L0S6rrEj0KE/0.jpg"
alt="training vid" width="480" height="360" border="10" /></a>


Sample output after 800 epochs:
<a href="https://www.youtube.com/watch?v=SBgB6J9RRA8" target="_blank"><img src="http://img.youtube.com/vi/SBgB6J9RRA8/0.jpg"
alt="training vid" width="480" height="360" border="10" /></a>


Sand example:
<a href="https://www.youtube.com/watch?v=4eVtPubrT6w" target="_blank"><img src="http://img.youtube.com/vi/4eVtPubrT6w/0.jpg"
alt="training vid" width="480" height="360" border="10" /></a>


Anchor example:
<a href="https://www.youtube.com/watch?v=CvrjXbmXOVE" target="_blank"><img src="http://img.youtube.com/vi/CvrjXbmXOVE/0.jpg"
alt="training vid" width="480" height="360" border="10" /></a>