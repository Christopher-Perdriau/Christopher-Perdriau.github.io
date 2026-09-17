---
title: "Contact"
permalink: /contact/
excerpt: "Email and Google Scholar."
---

The fastest way to reach me is email. My address is assembled below via JavaScript to cut down on spam-bot scraping; if you have JavaScript disabled, my Google Scholar profile has a working contact path.

<p>
  <strong>Email:</strong>
  <span id="contact-email">
    <noscript>enable JavaScript to reveal, or reach me via Google Scholar below</noscript>
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

- **Google Scholar:** [scholar.google.com/citations?user=-cDZEO8AAAAJ](https://scholar.google.com/citations?user=-cDZEO8AAAAJ&hl=en)
