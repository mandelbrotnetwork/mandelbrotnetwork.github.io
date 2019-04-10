---
title: The Mandelbrot Project
layout: page
feature_image: "https://upload.wikimedia.org/wikipedia/commons/2/21/Mandel_zoom_00_mandelbrot_set.jpg"
---
<script id="container_script">
  const ifrm = document.createElement('iframe')
  ifrm.onload = function resizeIframe() {
    // Select the node that will be observed for mutations
    var targetNode = ifrm.contentWindow.document.body;

    // Options for the observer (which mutations to observe)
    var config = { attributes: true, childList: true, subtree: true };

    // Callback function to execute when mutations are observed
    var callback = function(mutationsList, observer) {
          ifrm.style.height = ifrm.contentWindow.document.body.scrollHeight + 'px';
    };

    // Create an observer instance linked to the callback function
    var observer = new MutationObserver(callback);

    // Start observing the target node for configured mutations
    observer.observe(targetNode, config);

  }
  ifrm.style.width = 100 + '%'
  ifrm.src = location.href + 'survey/'
  document.getElementById('container_script').parentElement.appendChild(ifrm)
</script>