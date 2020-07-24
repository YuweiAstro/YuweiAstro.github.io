---
layout:       post
title:        "multi-lang test"
subtitle:     "subtest"
date:         2020-01-01 12:00:00
author:       "yuwei"
multilingual: true
tags:
    - test
---

<!-- Chinese Version -->
<div class="zh post-container">
    {% capture about_zh %}{% include posts/2020-07-24-test/zh.md %}{% endcapture %}
    {{ about_zh | markdownify }}
</div>

<!-- English Version -->

<div class="en post-container">
    {% capture about_en %}{% include posts/2020-07-24-test/en.md %}{% endcapture %}
    {{ about_en | markdownify }}
</div>

