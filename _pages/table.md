---
layout: fullwidth
title: Doctoral Students Funding Calendar (Table)
permalink: /table
datatable: true
---

<div class="bg-white rounded text-center p-3 mb-2">
    <h1 class="display-4 text-center mt-3 mb-2">
      {{page.title}}
    </h1>
    <a href="{{site.baseurl}}/" class="btn btn-primary">
        <i class="fa fa-home"></i>
        Home
    </a>
</div>
<table id="table" class="table table-bordered bg-light">
        <thead>
            <tr>
                <th>id</th>
                <th style="min-width: 100px">名称</th>
                <th style="min-width: 100px">実施機関</th>
                <th style="min-width: 100px">生活費<br>（年額）</th>
                <th style="min-width: 110px">研究費・開発費<br>（特記なき場合は年額）</th>
                <th style="min-width: 100px">期間</th>
                <th style="min-width: 100px">対象者</th>
                <th style="min-width: 100px">対象分野</th>
                <th style="min-width: 60px">採用予定数・規模</th>
                <th style="min-width: 100px">継続性</th>
                <th style="min-width: 70px">申請締め切り時期</th>
                <th style="min-width: 70px">所得の扱い</th>
                <th style="min-width: 100px">副収入の制限</th>
                <th style="min-width: 100px">備考</th>
            </tr>
        </thead>
        <tbody>
            {%- for item in site.data.category["DoctorFunding"] -%}
            {%- assign program = site.data.program[item] -%}
            <tr{% if program.ended %} class="text-secondary"{% endif %}>
                <td>{{ forloop.index }}</td>
                <td>
                    <a href="{{ program.url }}" target="_blank" rel="noopener noreferrer">
                        {{ program.full-name }}{% if program.ended %}（終了）{% elsif program.recruitment_closed %}（通常新規募集終了・支援継続中）{% endif %}
                    </a>
                </td>
                <td>{{ program.organizer }}</td>
                <td>{{ program.living_funding }}</td>
                <td>{{ program.research_funding }}{% if program.research_funding_unit %}<br><small>（{{ program.research_funding_unit }}）</small>{% endif %}</td>
                <td>{{ program.duration }}</td>
                <td><small>{{ program.eligible_person }}</small></td>
                <td><small>{{ program.eligible_area }}</small></td>
                <td>{{ program.accepted_num }}</td>
                <td>{{ program.continuity }}</td>
                <td>{{ program.deadline }}</td>
                <td>{{ program.income_category }}</td>
                <td><small>{{ program.other_income }}</small></td>
                <td><small>{{ program.note }}</small></td>
            </tr>
            {%- endfor -%}
        </tbody>
</table>

