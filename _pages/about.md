---
layout: about
title: About
permalink: /
subtitle: 

profile:
  align: right
  image: yihanliu.jpg  # CHANGE THIS: Put your profile photo in assets/img/ folder and change filename here
  image_circular: true # crops the image to make it circular (set to false for square image)
  more_info: >
    <p style="font-size: 16px; font-family: Roboto, sans-serif;">Incoming M.S. @ NKU</p>
    <p style="font-size: 16px; font-family: Roboto, sans-serif;">youngninahan [at] gmail [dot] com</p>

news: true # includes a list of news items (add news in _news folder)
selected_papers: true # includes a list of papers marked as "selected={true}" (add papers in _bibliography/papers.bib)
social: true # includes social icons at the bottom of the page
---

<!-- ========================================== -->
<!-- MAIN CONTENT: Write your bio/introduction here -->
<!-- This is the main text that appears on your homepage -->
<!-- You can use HTML tags like <a href="...">link</a> for links -->
<!-- ========================================== -->

I am a senior undergraduate student in the School of Artificial Intelligence, Chongqing University of Posts and Telecommunications (expected graduation: June 2027). I will pursue my Master's degree at the Media Computing Lab, Nankai University, supervised by <a href="https://dengpingfan.github.io/pages/People.html">Prof. Deng-Ping Fan</a>. My research interests lie in Sim2Real and Embodied AI.

Wish you a happy day!

<!-- ========================================== -->
<!-- EXPANDABLE SECTION (Optional) -->
<!-- This section is hidden by default and shows when user clicks the button -->
<!-- You can delete this entire section if you don't need it -->
<!-- ========================================== -->

<button class="btn btn-sm btn-outline-primary bio-toggle" type="button" data-text-collapsed="Show more about my background" data-text-expanded="Show less">Show more about my background</button>

<div class="bio-more bio-hidden" markdown="1">
Updating...
</div>

<!-- ========================================== -->
<!-- STYLE AND SCRIPT FOR EXPANDABLE SECTION -->
<!-- Keep this code - it makes the expand/collapse button work -->
<!-- ========================================== -->

<style>
  .bio-hidden {
    display: none;
  }
  .bio-toggle {
    margin: 0.5rem 0;
  }
</style>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    document.querySelectorAll(".bio-toggle").forEach(function (btn) {
      btn.addEventListener("click", function () {
        const expand = btn.getAttribute("data-expanded") !== "true";
        document.querySelectorAll(".bio-more").forEach(function (el) {
          el.classList.toggle("bio-hidden", !expand);
        });
        btn.setAttribute("data-expanded", expand ? "true" : "false");
        btn.textContent = expand ? btn.dataset.textExpanded : btn.dataset.textCollapsed;
      });
    });
  });
</script>
