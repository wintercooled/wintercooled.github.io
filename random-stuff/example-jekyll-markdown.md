---
layout: page
title: Example Jekyll Markdown
permalink: /random-stuff/example-jekyll-markdown
---

# Example markdown used by this website

## The following demonstrates how 'markdown' is used by the site to present content. 

The above are examples of a page heading and a subheading. Most pages here start with these. To view the markdown that results in the formatting seen on this page you can use the **edit** button within Github to view this page's source.

Example standard paragraph text one.

Example standard paragraph text two.

### Example sub heading

Example standard paragraph text three.

If you are refering to an external concept such as 'markdown' use the single quote marks or consider adding it as a link, such as [markdown](https://en.wikipedia.org/wiki/Markdown). If you are refering to an internal reference such as a file name or object name within a page use **emphasis** instead. This should also be done the first time you refer to a concept introduced on the page, by way of explanation to ease page reading navigation.

##### Example of something you really want to be read. These should be used sparingly.

Use of a horizontal rule to seperate content:

* * *

Example [link](({{ site.url }}/random-stuff/index)) to another page within the site.

Example external [link](https://github.com/jekyll/minima).

* * * 

|Example table header one|Example table header two|
|--------|--------|
|Row 1 column 1|Row 1 column 2|
|Row 2 column 1|Row 2 column 2|
|Row 3 column 1|Row 3 column 2|

* * *

Example bullet point list:

* Bullet point one.

* Bullet point two.

* Bullet point three.

* * *

#### Note: An example note block. For minor emphasis and 'tips'. These can span multiple lines as long as you don't break the text with a carriage return.

Example use of `code formatting` within a block of normal text.

~~~~
Example standalone code block
...which can span many lines
~~~~

<div class="console-output">Example output from an executed code block, file content, file path etc.
</div>

Note: The syntax highlighter option for code blocks has been disabled within **_config.yml**. 

* * * 

Some formatting relies on using html:

<div class="console-output">Example output from an executed code block, file content, file path etc.
</div>

**1.**&nbsp;&nbsp;&nbsp;&nbsp;Example numbered list item one.

**2.**&nbsp;&nbsp;&nbsp;&nbsp;Example numbered list item two.

Example use of the **br** tag to force repeating line breaks:
<br/>
<br/>
<br/>
This may be needed as consecutive carriage returns in markdown are not rendered...



...as this text shows.

* * * 

Example embedded image using html:

<img class="" alt="alt text" src="{{ site.url }}/images/logo_big.png" />

* * * 

Example embedded image using inline-style and hover text: 

![alt text]({{ site.url }}/images/logo_big.png "Hover text inline")

* * * 

Example embedded image using reference-style and hover text: 

![alt text][logo]

[logo]: {{ site.url }}/images/logo_big.png "Hover text reference"

* * * 

Example use of a site variable: {{ site.twitter_link }}

You can create your own site variables by adding them to **_config.yml**. 

If you want to add Javascript to a page please refer to _include/header.html to see how this is done.

