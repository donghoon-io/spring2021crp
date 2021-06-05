---
layout: page
title: 정보 게시판
permalink: /info
comments: true
---

<div class="mainheading">
    <h1 class="sitetitle">정보 게시판</h1>
    <p class="lead">
        AI SEE YOU에 관한 정보를 공유하는 게시판입니다
    </p>
</div>

{% assign posts = site.data.info.posts %}

<!-- Featured
================================================== -->
<section class="featured-posts">
    <div class="section-title">
        <h2><span>추천 게시글</span></h2>
    </div>
    <div class="row">

    {% for post in site.categories.info %}

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