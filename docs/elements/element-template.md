---
layout: default
published: false
---

<!-- page specific stylesheet needs to be inline to the page so ajax injects it. -->
<link rel="stylesheet" href="/css/elementpage.css">

{% assign element = site.data.elements[page.element] %}

<!-- <doc-page></doc-page> -->

<component-docs></component-docs>

<script>
  (function() {

    function initDoc() {
      var elementDoc = {{element | jsonify}};
      document.querySelector('component-docs').data = elementDoc;  
    }
    initDoc();

  })();
</script>
