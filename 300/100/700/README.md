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

![image](https://user-images.githubusercontent.com/1499433/199122613-0af71864-5a1c-4942-9e76-2bac07fd1ff3.png)

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

![image](https://user-images.githubusercontent.com/1499433/199122896-e7ac593a-047e-4787-984f-72b5fc84094f.png)
