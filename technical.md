---
title: Technical
description: 
---

[List](list#technical)

The [Katagiri Transcripts](https://katagiritranscripts.net) website is written in [Markdown](https://guides.github.com/features/mastering-markdown/) using [BBEdit for Mac](https://www.barebones.com/products/bbedit/), and is hosted on [GitHub Pages](https://pages.github.com).

PDF export is provided using the [BBStylish](https://nostodnayr.net/projects/bbstylish/) template for BBEdit.

Text to speech support is provided by [NaturalReaders](https://www.naturalreaders.com/online/).

## BBEdit Find/Replace Patterns

These are the find/replace grep or regex [patterns](https://www.barebones.com/support/technotes/PatternPlaygrounds.html) that I’m using in BBEdit, to aid in maintaining the references. Note: these are not foolproof; they must be used intelligently and with caution. Still, who knows, maybe including these here will help someone some day.

Pattern Name | Search Pattern | Replace Pattern 
---------------- | ----------------- | -------------------
first occurrences		|	`(?<!#|\]\()\b(zazen)\b(?s)(.*?##)`	| `[\1](glossary#zazen)\2`
first occurrences	plural		|	`(?<!#|\]\()\b(buddha(s?))\b(?s)(.*?##)`	| `[\1](glossary#buddha)\3`
occurrences					|	`(?<!#|\]\()\b(zazen)\b`	|	`[\1](glossary#zazen)`
unlinked occurrences:	|	`(?<![\[#-])\b(zazen)\b(?![\]-])`	|	`[\1](glossary#zazen)`
links by text					|	`\[(zazen)\]\(.*?\)`			|	`\1`
links by reference		|	`\[([^\[\]\(\)\n]*?)\]\(glossary#zazen\)`		|	`\1`
all links 						|	`\[[^\]\n]*\]\([^\)\n]*\)`		|
all non-link brackets	|	`\[[^\]\n]*\](?!\()`				|
all brackets					|	`\[(.*?)\](?=\(?)`				|
all brackets 2				|	`\[[^\]\n]*\]`					|
`(T|t)athagata(s?)`			|	`\b(T|t)athagata(s?)\b`	| `\1athāgata\2`

## BBEdit Clippings

---------------- | ----------------- | -------------------
Glossary Link With Selection	|	`[#SELECT#](glossary##SELECT#)#INSERTION#`
Markdown Link Insert	|	`[#SELECT#](#CLIPBOARD#)#INSERTION#`

[List](list#technical)

