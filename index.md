---
title: "Kramdown Options test"
layout: default
---

# Kramdown Options Test

I've been having problems making GitHub Pages, Jekyll and Kramdown to work in another repo. This is a GitHub Pages project to demonstrate the issues.

# Status:

* ALD and IAL
* parse markdown in html block
* toc_levels - works in this repo!
* hard_wrap - works in this repo!
* transliterated_header_ids - **does not work!**


# Table of Contents 

* TOC
{:toc}


## ALD and IAL
{: .soneClass }

Testing [attribute list definitions](http://kramdown.gettalong.org/syntax.html#attribute-list-definitions) and [inline attribute lists](http://kramdown.gettalong.org/syntax.html#inline-attribute-lists){:rel='something'} .



## Parse markdown in html block

According to [kramdown Syntax](http://kramdown.gettalong.org/syntax.html#html-blocks), markdown within a HTML-block (within a Markdown-file) should be parsed if the attribute `markdown` is set.

### Test

<div markdown="1">
Hello **world**! How _are_ you today?
</div>



## Problem with Table of contents levels
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

## Problem with hard_wrap

Kramdown, the Markdown converter, supports interpretting line breaks literally with [the option hard_wrap](http://kramdown.gettalong.org/options.html#option-hard-wrap)

However, when added to the _config.yml-file:

    kramdown:
       hard_wrap: true

no `<br/>` are added to the generated HTML

If I write a paragraph
on serveral lines
in the markdown file
will I get `<br /`>
for every new line?

Or will it end up without HTML markup for newlines?

One way to trigger `<br />` is to put  
two spaces  
after each line  
(or maybe three)   
but they can be  
a litte bit hard to see.

Another solution is to simply write \<br /> for every <br />
line <br />
I <br/>
want.

## Transliterate header ids

When set to true, I should be able to have translitterated header ids...

### Header with åäö 

The above header uses typical swedish characters...

# More of the same 
Just for demonstrating purposes. Is "smart quotes" enabled by the way?

# parse_block_html

<div> 
<div>

## Header inside div inside div

</div>
</div>
