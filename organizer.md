---
layout: page
title: 運営者情報
permalink: /organizer/
---

DISTは、DIST実行委員会によって企画・運営されています。実行委員会は、主宰と有志のスタッフで組織されており、その全員が無償で協力しています。人件費、交通費など、あらゆる名目での対価を受け取っていません。

# スタッフ紹介

{% for item in site.staff %}
   {% capture staff_count %}{{ staff_count | plus: 1 }}{% endcapture %}
{% endfor %}

DIST実行委員会は、{{ staff_count }}名のスタッフによって支えられています。

<ul class="staff__list">
	{% for item in site.staff %}
	<li class="staff__list-item">
		<a href="https://twitter.com/{{ item.twitterId }}" target="_blank" class="hint--bottom-right hint--multiline" data-hint="{{ item.comment }}">
			<div style="background-image: url(/images/individual/staff/staff__icon--{{ item.twitterId }}.png);" class="staff__icon"></div>
			<div class="staff__info">
				<span class="staff__name">{{ item.name.ja }}</span>
				<span class="staff__job">{{ item.job }}（{{ item.belong }}）</span>
			</div>
		</a>
	</li>
	{% endfor %}
</ul>

# スタッフになりたい！

以下のフォームよりお問い合わせください。

<div class="button">
	<a href="https://docs.google.com/forms/d/1_4hUpr-w4a4TJ-VSvra036B5TLr8qyqPu_rQyEAZTCE/viewform" target="_blank"><div class="button__label">お問い合わせフォーム</div></a>
</div>