---
title: The Mandelbrot Project
layout: page
feature_image: "https://upload.wikimedia.org/wikipedia/commons/2/21/Mandel_zoom_00_mandelbrot_set.jpg"
---
<script>
window.setIframeHeight = function resizeIframe() {
    const objt = document.getElementById("survey_iframe")
    obj.style.height = obj.contentWindow.document.body.scrollHeight + 'px';
  }
</script>
<iframe style="width: 100%; height: 600px" id="survey_iframe" onload="window.setIframeHeight()" src="/survey"/>  