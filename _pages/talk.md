---
layout: page
title: 잡담 게시판
permalink: /talk
comments: true
---

<div class="mainheading">
    <h1 class="sitetitle">잡담 게시판</h1>
    <p class="lead">
        잡담을 나누는 게시판입니다
    </p>
</div>

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

        {% for post in site.posts %}

        {% include postbox.html %}

        {% endfor %}

    </div>

</section>

<!-- Pagination
================================================== -->
<div class="bottompagination">
<div class="pointerup"><i class="fa fa-caret-up"></i></div>
<span class="navigation" role="navigation">
    {% include pagination.html %}
</span>
</div>