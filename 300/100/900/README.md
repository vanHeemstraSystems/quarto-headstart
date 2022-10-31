# 900 - Code Cells

Code cells contain executable code to be run during render, with the output (and optionally the code) included in the rendered document.

<pre>
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

You are likely familiar with the Matplotlib code given here. However, there are some less familiar components at the top of the code cell: ```label``` and ```fig-cap``` options. Cell options are written in YAML using a specially prefixed comment (```#|```).

In this example, the cell options are used to make the figure cross-reference-able. Try changing the ```fig-cap``` and/or the code then re-rendering to see the updated preview.

There are a wide variety of [cell options](https://quarto.org/docs/reference/cells/cells-jupyter.html) that you can apply to tailor your output. We’ll delve into these options in the next tutorial.

**Note**: One particularly useful cell option for figures is ```fig-alt```, which enables you to add alternative text to images for users with visual impairments. See Amy Cesal’s article on [Writing Alt Text for Data Visualization](https://medium.com/nightingale/writing-alt-text-for-data-visualization-2a218ef43f81) to learn more.
