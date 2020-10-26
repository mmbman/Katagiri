<a name="0"></a>
# Tools

The Katagiri Transcripts website is created in Markdown, using BBEdit, and hosted on GitHub Pages.

## BBEdit Find/Replace Patterns 

These are the find/replace grep or regex patterns that I’m using in BBEdit, to aid in maintaining the references. Note: these are not foolproof; they must be used intelligently and with caution. Still, who knows, maybe including these here will help someone some day.

Pattern Name | Search Pattern | Replace Pattern 
---------------- | ----------------- | -------------------
occurrences | (?<!#|\]\()\b(zazen)\b | [\1](glossary#zazen)
first occurrences | \b(zazen)\b(.*)	 | [\1](glossary#zazen)\2

