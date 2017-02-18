---
layout: post
title: Progress Bar
permalink: /progress-bar/
categories: components
nav: components
published: false

---

## Definition

- The percentage of fill that the bar has is equal to the percentage completion of the background process
- A determinate progress is preferable to indeterminate, because it shows the user an exact percentage of process completion
- It's preferable to allow the user to see content as it becomes available, rather than wait with a blank view


-----

### Visual
<h3>Indeterminate</h3>
<div class="weave-progress">
  <div class="weave-progress__indeterminate"></div>
</div>

<br>
<h3>Determinate</h3>
<div class="weave-progress">
  <div class="weave-progress__determinate" style="width: 70%"></div>
</div>

### Markup

```html
<h3>Indeterminate</h3>
<div class="weave-progress">
  <div class="weave-progress__indeterminate"></div>
</div>

<h3>Determinate</h3>
<div class="weave-progress">
  <div class="weave-progress__determinate" style="width: 70%"></div>
</div>
```
