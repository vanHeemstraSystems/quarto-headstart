# 300 - Render and Preview

We’ll start out by rendering a simple example (```hello.qmd```) to a couple of formats. If you want to follow along step-by-step in your own environment, create a new file named ```hello.qmd``` and copy the following content into it.

<pre>
---
title: "Quarto Basics"
format:
  html:
    code-fold: true
jupyter: python3
---

For a demonstration of a line plot on a polar axis, see @fig-polar.

```{python}
#| label: fig-polar
#| fig-cap: "A line plot on a polar axis"

import numpy as np
import matplotlib.pyplot as plt

r = np.arange(0, 2, 0.01)
theta = 2 * np.pi * r
fig, ax = plt.subplots(
  subplot_kw = {'projection': 'polar'} 
)
ax.plot(theta, r)
ax.set_rticks([0.5, 1, 1.5, 2])
ax.grid(True)
plt.show()
```
</pre>

hello.qmd


To render and preview, execute the **Quarto: Render** command. You can alternatively use the ```Ctrl+Shift+K``` keyboard shortcut, or the **Render** button at the top right of the editor:

![image](https://user-images.githubusercontent.com/1499433/199038548-c81db7cf-0ef3-4ede-a7e3-0d20491ec62a.png)

**Note** that on the Mac you should use Cmd rather than Ctrl as the prefix for all Quarto keyboard shortcuts.

Additionally, there are commands available to render specific formats. Here is a complete list of the supported render commands:

- Quarto: Render
- Quarto: Render HTML
- Quarto: Render PDF
- Quarto: Render DOCX

The **Quarto: Render** command renders the default format of the currently active document. The other commands render specific formats (regardless of the document’s default format). The ```Ctrl+Shift+K``` keyboard shortcut will re-execute the most recently executed render command.
