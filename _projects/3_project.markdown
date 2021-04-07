---
layout: page
title: melon arena
description: Music tag recommendation
img: /assets/img/p2.jpg
importance: 3
---

Conducted a music playlist tag recommendation with basic recommendation algorithms as a part of DAI5001 graduate lecture. 

* Content based filtering (CBF) to calculate the similarity between tags in playlists. We employed word to vector (w2v) to calculate the cosine similarity between tags within playlists. For example, the tag which have the high cosine similarity with the w2v feature of the "stress" tag is recommended.  


* Collaborative filtering (CF) is used to find out latent variables to convert user-item sparse matrix into low dimensional dense matrix of user-latent variable and latent variable-item matrices. 
    * We used non-negative matrix factorization (NMF) to make low dimensional matrices.
    * We used alternating least squares (ALS) method to do the matrix factorization. 




<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/ply.PNG' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/nmf.PNG' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/als_ex.PNG' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    Left: The playlist example to predict the highlighted as purple tags. Middle: How to do non-negative matrix factorization. Right: Result example of ALS.
  </div>
    








