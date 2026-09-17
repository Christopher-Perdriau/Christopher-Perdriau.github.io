---
title: "Contact"
permalink: /contact/
excerpt: "Email, LinkedIn, and Google Scholar."
---

The fastest way to reach me is email. My address is assembled below via JavaScript to cut down on spam-bot scraping; if you have JavaScript disabled, my LinkedIn and Google Scholar profiles both have working contact paths.

<p>
  <strong>Email:</strong>
  <span id="contact-email">
    <noscript>christopherperdriau99 [at] gmail [dot] com &mdash; enable JavaScript for a clickable link, or reach me via LinkedIn/Google Scholar below</noscript>
  </span>
</p>

<script>
  (function () {
    var user = "christopherperdriau99";
    var domain = "gmail.com";
    var address = user + "@" + domain;
    var el = document.getElementById("contact-email");
    var a = document.createElement("a");
    a.href = "mailto:" + address;
    a.textContent = address;
    a.setAttribute("aria-label", "Send email to " + address);
    el.textContent = "";
    el.appendChild(a);
  })();
</script>

- **LinkedIn:** [linkedin.com/in/christopher-perdriau](https://www.linkedin.com/in/christopher-perdriau-a79a59149/)
- **Google Scholar:** [scholar.google.com/citations?user=-cDZEO8AAAAJ](https://scholar.google.com/citations?user=-cDZEO8AAAAJ&hl=en)
