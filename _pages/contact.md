---
title: "Contact"
permalink: /contact/
excerpt: "Email, GitHub, and Google Scholar."
---

The fastest way to reach me is email. My address is assembled below via JavaScript to cut down on spam-bot scraping; if you have JavaScript disabled, my GitHub and Google Scholar profiles both have working contact paths.

<p>
  <strong>Email:</strong>
  <span id="contact-email">
    <noscript>enable JavaScript to reveal, or reach me via GitHub/Google Scholar below</noscript>
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

- **GitHub:** [github.com/Christopher-Perdriau](https://github.com/Christopher-Perdriau)
- **Google Scholar:** [scholar.google.com/citations?user=-cDZEO8AAAAJ](https://scholar.google.com/citations?user=-cDZEO8AAAAJ&hl=en)
