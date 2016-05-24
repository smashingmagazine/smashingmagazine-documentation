# Prism.js – Smashing Syntax Highlighting

## [!] Changes in `prism.js`-script

I've removed the following code block completely:

```js
document.addEventListener&&!r.hasAttribute("data-manual")&&document.addEventListener("DOMContentLoaded",n.highlightAll)
```

and called the `Prism.highlightAll()` and the bottom of the script file. We're loading the script now async and on DOMContentLoaded, so the JS-execution of highlighting the code can be done directly in script. 

## What languages are supported now?

In alphabetical order:

- Apache Configuration
- C
- C++
- C-Like
- CSS
- Git
- Go
- HTTP
- JSON
- LESS
- Make
- Markdown
- Markup (HTML)
- NGINX Configuration
- Objective-C
- Perl
- PHP
- Powershell
- Python
- Sass
- Scss
- SQL
- Stylus
- YAML

## How to use Prism in articles

Here the basic markup you need to have in place for Prism to highlight the code example

```
<pre><code class="language-*">
  Some Code goes here
</code></pre>
```

The asterisk stands for any type of language used inside the code example.

## Languages and their classes

|Language|Classname|
|---|---|
|Apache|language-apacheconf|
|C|language-c|
|C++|language-cpp|
|C-like|language-clike|
|CSS|language-css|
|Git|language-git|
|Go|language-go|
|HTTP|language-http|
|JSON|language-json|
|LESS|language-less|
|Make|language-makefile|
|Markdown|language-markdown|
|Markup|language-markup|
|NGINX|language-nginx|
|Objective-C|language-objectivec|
|Perl|language-perl|
|PHP|language-php|
|Powershell|language-powershell|
|Python|language-python|
|Sass|language-sass|
|Scss|language-scss|
|SQL|language-sql|
|Stylus|language-stylus|
|YAML|language-yaml|
