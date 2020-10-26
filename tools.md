<a name="0"></a>
# Tools

The [Katagiri Transcripts](https://katagiritranscripts.net) website is created in [Markdown](https://guides.github.com/features/mastering-markdown/) using [BBEdit for Mac](https://www.barebones.com/products/bbedit/), and is hosted on [GitHub Pages](https://pages.github.com).

## BBEdit Find/Replace Patterns

These are the find/replace grep or regex [patterns](https://www.barebones.com/support/technotes/PatternPlaygrounds.html) that I’m using in BBEdit, to aid in maintaining the references. Note: these are not foolproof; they must be used intelligently and with caution. Still, who knows, maybe including these here will help someone some day.

Pattern Name | Search Pattern | Replace Pattern 
---------------- | ----------------- | -------------------
occurrences					|	`(?<!#|\]\()\b(zazen)\b`	|	`[\1](glossary#zazen)`
first occurrences			|	`(?<!#|\]\()\b(zazen)\b(.*)`	| `[\1](glossary#zazen)\2`
unlinked occurrences:	|	`(?<![\[#-])\b(zazen)\b(?![\]-])`	|	`[\1](glossary#zazen)`
links by text:				|	`\[(zazen)\]\(.*?\)`			|	`\1`
links by reference:		|	`\[([^\[\]\(\)\n]*?)\]\(glossary#zazen\)`		|	`\1`
all links: 						|	`\[[^\]\n]*\]\([^\)\n]*\)`		|
all non-link brackets:	|	`\[[^\]\n]*\](?!\()`				|
all brackets:					|	`\[(.*?)\](?=\(?)`				|
all brackets 2:				|	`\[[^\]\n]*\]`					|
