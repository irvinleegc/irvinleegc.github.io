---
layout: post
title: Markdown Syntax
cover: cover.jpg
date:   2017-01-09 12:00:00
categories: posts
---

### **Header and paragraph**
Use `` # `` to indicate header

**Example in Markdown:**
```Markdown
`#header1` 
`####header4####`  

`header2`  
`-------`  
```

#header 1  
####header4####  
header2  
-------  

**Example in HTML:**
``` HTML
<h2>header2</h2>
```
<h2>header2</h2>


**Example in Markdown:**
`Following paragraphs starts here.`
Following paragraphs starts here.

**Example in HTML:**
``` HTML
`<p>Following paragraphs</p> <p>starts here.</p>`
```
<p>Following paragraphs</p> <p>starts here.</p>

### **Emphasis**
Use single asterisk `` ` `` or single underscore ` _ `for _italic_.
Use double asterisks <code>``</code> or double underscores <code>__</code > for **bold**.
Use two tildes <code>~~ </code> for ~~strikethrough~~.

**Example in Markdown:**  
`*italic*` *italic*  `_italic_` _italic_  
`**bold**` **bold** `__bold__` __bold__
`` ~~ strike~~ `` ~~strike~~

**Example in HTML:**
``` HTML
``<em> italic </em>`` 
``<strong> bold </strong>`` 
```
<em> italic </em>
<strong> bold </strong>

But if you surround an `*` or `_` with spaces, it’ll be treated as a literal asterisk or underscore. To place an asterisk or underscore without the space, use the escape backslash character `\`

**Example in Markdown:**  
` This is an asterisk * and this is an underscore _ `  
This is an asterisk * and this is an underscore _  

`These are \*asterisks\* using backslash and these are \_underscores\_ using backslash and may contain **bold** and _italic_ `
These are \*asterisks\* using backslash and these are \_underscores\_ using backslash and **bold** and _italic_

### **Table**
Use pipe `|` to indicate column in table.  
Use minumal 3 dashes `---` to indicate header.  
Use colon `:` to indicate alignment.  

**Example in Markdown:**
<code>|No|Name|Team|
|---:|:---|:---:|
|1|John|A|
|2|\*Jane\*|B|
|3|Jake|\**F**|</code>

|No|Name|Team|
|---:|:---|:---:|
|1|John|A|
|2|*Jane*|B|
|3|Jake|**F**|


### **List**
Use multiple rows of `*` `+` `-`to indicate a bullet list.  
**Example in Markdown:**
<code>To do list:
 + learn markdown
 * write a post with markdown
 - write a blog with markdown</code>
To do list:
 + learn markdown
 * write a post with markdown
 - write a blog with markdown

**Example in HTML:**
```HTML
`` <ul><li>learn markdown</li>
<li>write a post with markdown</li>
<li>write a blog with markdown</li></ul>``
```
<ul><li>learn markdown</li>
<li>write a post with markdown</li>
<li>write a blog with markdown</li></ul>
 
Use multiple rows of numbers (in or our of sequence) to indicate a numbered list.  
**Example in Markdown:**  
<code>To do list:
 1. learn markdown
 5. write a post with markdown
 3. write a blog with markdown</code>  
 
To do list:
 1. learn markdown
 3. write a post with markdown
 3. write a blog with markdown

**Example in HTML:**
```HTML
<ol>
<li>learn markdown</li>
<li>write a post with markdown</li>
<li>write a blog with markdown</li>
</ol>
```
<ol>
<li>learn markdown</li>
<li>write a post with markdown</li>
<li>write a blog with markdown</li>
</ol>

### **Code**
To indicate codes, use backtick <code>`</code>

**Example in Markdown:**  
This is a \`main()\` function.  
This is a `main()` function.  

**Example in HTML:**  
```HTML
`This is a <code>main()</code> function.`
```
This is a <code>main()</code> function.  

Use double backticks to indicate a real a backtick `` ` ``. Any backtick within the double backticks will be treated as an actual backtick.

**Example in Markdown:**
<code>This is a \`\` \` \`\` backtick. </code>
This is a `` ` `` backtick.
<code> \`\` These are \`a bunch\` of \`b\`a\`c\`k\`t\`i\`c\`k\`s\`. \`\`</code>
`` These are `a bunch`of `b`a`c`k`t`i`c`k`s`. ``

**Example in HTML:**
This is a &#96; backtick.
<code>These are &#96;a bunch&#96; of &#96;b&#96;a&#96;c&#96;k&#96;t&#96;i&#96;c&#96;k&#96;s&#96;. </code>


To enable syntax highlight use tripple backticks <code>```</code> along with the language.

**Example in Markdown:**
<code>'''HTML
< a href=http:www.google.com>google.com`<`/a\>```
</code>
```HTML
< a href=http:www.google.com>google.com < /a\>
```

### **Quotes or citations**
Use `>` to indicate quotes / citations / indent.

**Example in Markdown:**
`> Quote of the day`
 > Quote of the day

### **Link**

URLs it self will automatically be converted into links, alternatively, we can create link using angle brackets `< >`.

**Example in Markdown:**
`http://www.google.com`
http://www.google.com

`www.google.com`
www.google.com

`[Google](www.google.com) inline link`
[Google](www.google.com) inline link

`[Google](www.google.com "Search Engine") inline link with title`
[Google](www.google.com "Search Engine") inline link with title

<code>Google link within number reference\[1]
\[1]: www.google.com </code>
Google link within number reference[1]

[1]: http://www.google.com

<code>\[Google] link within itself
\[Google]: www.google.com </code>
[Google] link within itself

[Google]: www.google.com

<code>\[anylink] as reference is case insensitive
\[AnYLink]: www.google.com </code>
[anylink] as reference is case insensitive

[AnYLink]: www.google.com

**Example in HTML:**
``<a href="http://www.google.com/">link</a>``
<a href="http://www.google.com/">link</a>


### **Email**
Create email address using angle brackets `< >`.

**Example in Markdown:**
`` email me at <email@address.com> ``
email me at <email@address.com>

### **Emoji :smile:**
<https://www.emoji.codes/>


### **Image**


### **Backslash Escape**
Use a backslash `\` before these special character to actually indicate that you are typing these characters.

\\ backslash  
\` backtick  
\* asterisk  
\_ underscore  
\{\} curly braces  
\[\] square brackets  
\(\) parentheses  
\# hash mark  
\+ plus sign  
\- minus sign (hyphen)  
\. dot  
\! exclamation mark  
