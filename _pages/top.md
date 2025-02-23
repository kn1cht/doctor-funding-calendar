---
layout: default
title: Doctoral Students Funding Calendar
permalink: /
---

{%- assign category = "DoctorFunding" -%}

<div class="container bg-white rounded p-4">
  <div class="row justify-content-center">
    <h1 class="display-4 text-center mt-3 mb-2">
      {{page.title}}
    </h1>
  </div>
</div>

<!-- Calendars in Category -->
{% include calendar.html category=category title="申請時期（目安）" %}

<div class="container bg-white rounded mt-5 mb-10 pt-3 pb-3">
  <div class="row justify-content-center">
    <div class="col-9 p-3">
      <p class="text-center">
        {{ site.message1 }}
      </p>
      <h4 class="text-center">掲載方針</h4>
      <p>
        博士課程の学生が利用できる金銭的な研究支援事業を中心に掲載します。<br>
        掲載対象外としたものの例を示します。
        <ul>
          <li>博士課程在学者を対象に含まないもの（例：日本学術振興会特別研究員PD）</li>
          <li>
            奨学金（研究支援とは意味合いが異なる場合が多いため。
            <a href="https://washimaru-univ.com/minkankyufu-d-2022/" target="_blank" rel="noopener noreferrer">
            博士課程学生が利用できる各種民間奨学金の情報をまとめたページ</a>や、
            <a href="https://xplane.jp/application-prep-scholarship-list/" target="_blank" rel="noopener noreferrer">
            海外留学を対象とする奨学金の情報をまとめたページ</a>があります）
          </li>
          <li>海外留学支援を目的としたもの</li>
          <li>所属先によって支援内容に共通性がないもの（例：各大学独自のRA・フェローシップ。これらを含めだすとキリがないので……）</li>
          <li>臨時のもの（例：学生等の学びを継続するための緊急給付金）</li>
        </ul>
      </p>
      <h4 class="text-center">表形式で閲覧する</h4>
      <p>
          <a href="{{site.baseurl}}/table">データを表形式でもご覧になれます。</a>より詳細な比較にお使いください。
      </p>
      <h4 class="text-center">ご指摘・ご要望</h4>
      <p>
        本ページの内容はGitHubで管理しております。ご指摘やご要望は、IssueやPull Requestでぜひお寄せください。
      </p>
      <a href="https://github.com/kn1cht/doctor-funding-calendar/issues" class="btn btn-light" target="_blank" rel="noopener noreferrer">
        <i class="fab fa-github" aria-hidden="true"></i>
        GitHubで編集を提案
      </a>
    </div>
  </div>
</div>

<div class="container bg-white rounded mt-5 mb-10 p-4">
  <div class="row justify-content-center">
    <div class="col-9 text-center p-3">
      {% include list.html category=category %}
    </div>
  </div>
</div>

<!-- Funding Program Information with submission dates -->
{%- for item in site.data.category[category] -%}
{%- assign conf = item -%}
{% include program.html name=conf %}
{%- endfor -%}

<div class="container bg-white rounded p-4 mb-4">
  <div class="row justify-content-center">
    <div class="col-9 text-center p-3">
      {% include list.html category=category %}
    </div>
  </div>
</div>
