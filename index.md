---
title: "Kramdown Options test"
layout: default
---

# Kramdown Options Test

* TOC
{:toc}

I've been having problems making GitHub Pages, Jekyll and Kramdown to work. This is a GitHub Pages project to demonstrate the issues.

## Table of contents levels
According to the [Kramdown documentation](http://kramdown.gettalong.org/options.html#option-toc-levels) I should be able to adjust the level of TOC with the option `toc_levels`.
However I've tried adding the following to my `_config.yml` but without luck when GitHub Pages generates the static files:

```
kramdown:
  toc_levels: 1..2
``` 

### This is a subheader
This subheader should not appear in the table of contents above

### This is another subheader
Should also not appear in TOC

#### Even deeper subheader
Should definitely not appear in TOC
