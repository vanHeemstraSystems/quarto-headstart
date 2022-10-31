# 700 - YAML Options

At the top of the file there is a YAML block with document level options.

<pre>
---
title: "Quarto Basics"
format:
  html:
    code-fold: true
jupyter: python3
---
</pre>

Try changing the ```code-fold``` option to ```false```:

<pre>
---
title: "Quarto Basics"
format:
  html:
    code-fold: false
jupyter: python3
---
</pre>

Then re-render the document (again, no need to save before rendering). You’ll notice that the code is now shown above the plot, where previously it was hidden with a **Code** button that could be used to show it.
