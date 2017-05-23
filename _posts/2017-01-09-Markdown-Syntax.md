---
layout: post
title: Markdown Syntax
cover: cover.jpg
categories: [syntax]
google_analytics: TRUE
comments: TRUE
---

### **Header**  
Use `` # `` to indicate header  
**Example in Markdown:**  
```Markdown
# header1  
#### header4 ####  
header2
-------  
```
**Output:**  
# header1  
#### header4 ####  
header2
-------  

**Example in HTML:**
``` HTML
<h2>header2</h2>
```
**Output:**  
<h2>header2</h2>

-------------------  

### **Line Break**
To add line break, use two consequtive blanks at the end of the line.  
**Example in Markdown:**  
```Markdown
Same 
line  

Following paragraphs  
starts here.  
```
**Output:**  
Same 
line  

Following paragraphs  
starts here.  

**Example in HTML:**  
``` HTML
<p>Following paragraphs</p> <p>starts here.</p>
```
**Output:**  
<p>Following paragraphs</p> <p>starts here.</p>
    
-------------------  

### **Emphasis**  
Use single asterisk `` * `` or single underscore `` _ `` for _italic_.  
Use double asterisks <code>**</code> or double underscores `__` for **bold**.  
Use two tildes <code>~~</code> for ~~strikethrough~~.  

**Example in Markdown:**  
```Markdown
*italic* _italic_ **bold** __bold__ ~~strike~~
```
**Output:**  
 *italic* _italic_ **bold** __bold__ ~~strike~~

**Example in HTML:**
``` HTML
<em> italic </em>
<strong> bold </strong>
```
**Output:**  
<em> italic </em>
<strong> bold </strong>

But if you surround an `*` or `_` with spaces, it’ll be treated as a literal asterisk or underscore. To place an asterisk or underscore without the space, use the escape backslash character `\`.

**Example in Markdown:**  
```Markdow
This is an asterisk * and this is an underscore _
These are \*asterisks\* using backslash and these are \_underscores\_ using backslash and may contain **bold** and _italic_
```
**Output:**  
This is an asterisk * and this is an underscore _  
These are \*asterisks\* using backslash and these are \_underscores\_ using backslash and may contain **bold** and _italic_  

-------------------  

### **Table**
Use pipe `|` to indicate column in table.  
Use minimum 3 dashes `---` to indicate header.  
Use colon `:` to indicate alignment.  

**Example in Markdown:**
```Markdown
|No|Name|Team|
|---:|:---|:---:|
|1|John|A|
|2|Jane|B|
|3|Jake|F|
```
**Output:**  
|No|Name|Team|
|---:|:---|:---:|
|1|John|A|
|2|Jane|B|
|3|Jake|F|

-------------------  

### **List**
Use multiple rows of `*` `+` `-`to indicate a bullet list.  
**Example in Markdown:**
```Markdown
To do list:  
 + learn markdown  
 * write a post with markdown  
     + write the first paragraph
     * write the last paragragh
 - write a blog with markdown  
```
**Output:**  
To do list:  
 + learn markdown  
 * write a post with markdown  
     + write the first paragraph
     * write the last paragragh
 - write a blog with markdown  

**Example in HTML:**
```HTML
<ul>
<li>learn markdown</li>
<li>write a post with markdown</li>
<li>write a blog with markdown</li>
</ul>
```
**Output:**  
<ul>
<li>learn markdown</li>
<li>write a post with markdown</li>
<li>write a blog with markdown</li>
</ul>
 
Use multiple rows of numbers (in or our of sequence) to indicate a numbered list.  
**Example in Markdown:**  
```Markdown
To do list:  
 1. learn markdown  
 5. write a post with markdown  
 3. write a blog with markdown  
 ```
**Output:**  
To do list:  
 1. learn markdown  
 5. write a post with markdown  
 3. write a blog with markdown  

-------------------  

**Example in HTML:**
```HTML
<ol>
<li>learn markdown</li>
<li>write a post with markdown</li>
<li>write a blog with markdown</li>
</ol>
```
**Output:**  
<ol>
<li>learn markdown</li>
<li>write a post with markdown</li>
<li>write a blog with markdown</li>
</ol>

-------------------  

### **Code**
To indicate codes, use backtick <code>`</code>.

**Example in Markdown:**  
``` Markdown
This is a `main()` function.  
```
**Output:**  
This is a `main()` function.  

**Example in HTML:**  
```HTML
This is a <code>main()</code> function.
```
**Output:**  
This is a <code>main()</code> function.  

Use double backticks to indicate a real a backtick `` ` ``.  
Any backtick within the double backticks will be treated as an actual backtick.

**Example in Markdown:**  
```Markdown
This is a `` ` `` backtick.
`` These are `a bunch` of `b`a`c`k`t`i`c`k`s`. ``
```
**Output:**  
This is a `` ` `` backtick.  
`` These are `a bunch` of `b`a`c`k`t`i`c`k`s`. ``  

**Example in HTML:**  
```HTML
This is a &#96; backtick. <br/>
These are &#96;a bunch&#96; of &#96;b&#96;a&#96;c&#96;k&#96;t&#96;i&#96;c&#96;k&#96;s&#96;.
```
**Output:**  
This is a &#96; backtick. <br/>
These are &#96;a bunch&#96; of &#96;b&#96;a&#96;c&#96;k&#96;t&#96;i&#96;c&#96;k&#96;s&#96;.


-------------------  

### **Code snippet**
To enable code snippet use tripple backticks <code>```</code> or or tripple tidles <code>~~~</code>. Indicating the language after tripple backticks will enable syntax highlight.  

**Example in Markdown:**  
```Markdown
&#96;&#96;&#96;HTML
<a href=http:www.google.com>google.com </a>
<ol>
<li>learn markdown</li>
<li>write a post with markdown</li>
<li>write a blog with markdown</li>
</ol>
&#96;&#96;&#96;
```

~~~
<a href=http:www.google.com>google.com </a>
<ol>
<li>learn markdown</li>
<li>write a post with markdown</li>
<li>write a blog with markdown</li>
</ol>
~~~


**Output:**  
```HTML
<a href=http:www.google.com>google.com </a>
<ol>
<li>learn markdown</li>
<li>write a post with markdown</li>
<li>write a blog with markdown</li>
</ol>
```

~~~
<a href=http:www.google.com>google.com </a>
<ol>
<li>learn markdown</li>
<li>write a post with markdown</li>
<li>write a blog with markdown</li>
</ol>
~~~
-------------------  

### **Quotes or citations**
Use `>` to indicate quotes / citations / indent.  

**Example in Markdown:**
```Markdown
> Quote of the day
```
**Output:**  
> Quote of the day

**Example in HTML:**
```HTML
<blockquote>
Quote of the day
</blockquote>
```
**Output:**  
<blockquote>
Quote of the day
</blockquote>

-------------------  

### **Link**

URL itself will automatically be converted into link, alternatively, we can create link using `[]()`.

**Example in Markdown:**  
```Markdown
http://www.google.com  
www.google.com  
[Google](www.google.com) inline link  
[Google](www.google.com "Search Engine") inline link with title  
Google link within number reference[1]  

[1]: http://www.google.com

[Google] link within itself  

[Google]: www.google.com

[Anylink] as reference is case insensitive  

[AnYLink]: www.google.com
```
**Output:**  
http://www.google.com  
www.google.com  
[Google](www.google.com) inline link  
[Google](www.google.com "Search Engine") inline link with title  
Google link within number reference[1]  

[1]: http://www.google.com

[Google] link within itself  

[Google]: www.google.com

[Anylink] as reference is case insensitive  

[AnYLink]: www.google.com

**Example in HTML:**  
```HTML
<a href="http://www.google.com/">Google</a> inline link <br />
<a href="http://www.google.com/" title="Search Engine">Google</a> inline link with title <br />
```
**Output:**  
<a href="http://www.google.com/">Google</a> inline link <br />
<a href="http://www.google.com/" title="Search Engine">Google</a> inline link with title <br />

-------------------  

### **Footnote**  
Create footnote using `[^]`.  
**Example in Markdown:**
```Markdown
Terms and Conditions[^1] apply.  

[^1]: Just kidding.
```
**Output:**  
Terms and Conditions[^1] apply.  

[^1]: Just kidding.

### **Abbreviations**  
Mouse over abbreaviation to show the full form.  
**Example in Markdown:**  
```Markdown
T&C apply.

[T&C]: Terms and Conditions
```
**Output:**  
T&C apply.  

*[T&C]: Terms and Conditions  

-------------------  

### **Email**  
Create email address using angle brackets `< >`.  

**Example in Markdown:**
```Markdown
email me at <email@address.com>
```
**Output:**  
email me at <email@address.com>  

-------------------  

### **Emoji :smile:**
<https://www.emoji.codes/>

-------------------  

### **Image**
**Example in Markdown:**
```Markdown
[![Image Alt Text](/path/to/image)](path/to/linked/page)
```

-------------------  

### **Backslash Escape**
Use a backslash `\` before these special character to actually indicate that you are typing these characters.

**Example in Markdown:**
```Markdown
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
```
**Output:**  
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

-------------------  
