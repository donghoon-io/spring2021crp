---
layout: page
title: 이별 게시판
permalink: /breakup
comments: true
---

<div class="mainheading">
    <h1 class="sitetitle">이별 게시판</h1>
    <p class="lead">
        이별 경험을 공유하는 게시판입니다
    </p>
</div>

{% assign posts = site.data.breakup.posts%}

<!-- Featured
================================================== -->
<section class="featured-posts">
    <div class="section-title">
        <h2><span>추천 게시글</span></h2>
    </div>
    <div class="row">

    {% for post in site.posts %}

        {% if post.featured == true %}

            {% include featuredbox.html %}

        {% endif %}

    {% endfor %}

    </div>
</section>
<!-- Posts Index
================================================== -->
<section class="recent-posts">

    <div class="section-title">

        <h2><span>모든 글</span></h2>

    </div>

    <div class="row listrecent">

        {% for post in posts %}

        {% include postbox.html %}

        {% endfor %}

    </div>

</section>