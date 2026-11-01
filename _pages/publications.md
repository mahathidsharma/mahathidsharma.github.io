---
layout: page
permalink: /publications/
title: Publications
description: Peer-reviewed publications, newest first.
nav: true
nav_order: 3
---

<div class="publications">

{% bibliography %}

</div>

<script>
  // Clicking anywhere outside an open Abstract / BibTeX box closes it.
  document.addEventListener("click", function (event) {
    document.querySelectorAll(".publications .hidden.open").forEach(function (panel) {
      if (panel.contains(event.target)) return;
      var scope = panel.parentElement;
      var trigger = scope ? scope.querySelector(".links") : null;
      if (trigger && trigger.contains(event.target)) return;
      panel.classList.remove("open");
    });
  });
</script>
