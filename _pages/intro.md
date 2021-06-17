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

{% assign posts = site.data.intro.posts %}

<!-- Posts Index
================================================== -->

<section class="recent-posts">


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