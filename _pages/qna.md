---
layout: page
title: Q&A
permalink: /qna
comments: true
---

<div class="mainheading">
    <h1 class="sitetitle">QnA 게시판</h1>
    <p class="lead">
        AI SEE YOU에 관한 질의응답을 하는 게시판입니다
    </p>
</div>

{% assign posts = site.data.qna.posts %}

<!-- Featured
================================================== -->
<section class="featured-posts">
    <div class="section-title">
        <h2><span>추천 게시글</span></h2>
    </div>
    <div class="row">

    {% for post in site.categories.qna %}

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

<table class="table table-hover" style="width: 100%; font-size: 15px;">
    <colgroup>
       <col span="1" style="width: 5%;">
       <col span="1" style="width: 55%;">
       <col span="1" style="width: 15%;">
       <col span="1" style="width: 25%;">
    </colgroup>
    <thead style="background-color: #99999915">
    <tr>
    <th style="text-align: center;">#</th>
    <th style="text-align: center;">제목</th>
    <th style="text-align: center;">글쓴이</th>
    <th style="text-align: center;">날짜</th>
    </tr>
    </thead>


    {% for post in posts %}
    <tbody>
    <tr>
    <td style="text-align: center;">{{forloop.index}}</td>
    <td style="text-align: center;">{{post.title}}</td>
    <td style="text-align: center;">익명</td>
    <td style="text-align: center;">{{ post.date | date: '%m월 %d일' }}</td>
    </tr>
    </tbody>
    {% endfor %}

    </table>


</section>