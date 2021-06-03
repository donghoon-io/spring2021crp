---
layout: page
title: 가입인사
permalink: /intro
comments: true
---

<div class="mainheading">
    <h1 class="sitetitle">가입인사</h1>
    <p class="lead">
        가입인사를 나눠보세요!
    </p>
</div>

<section class="recent-posts">

    <div class="section-title">

        <h2><span>가입인사</span></h2>

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