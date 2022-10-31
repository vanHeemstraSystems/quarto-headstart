# 200 - Basic Workflow

Quarto ```.qmd``` files contain a combination of markdown and executable code cells. Here’s what it might look like in VS Code to edit and preview a ```.qmd``` file:

![image](https://user-images.githubusercontent.com/1499433/199030032-56451e02-9ecb-4546-8837-e9060e1ec94a.png)

The document on the left is *rendered* into the HTML version you see on the right. This is the basic model for Quarto publishing—take a source document and render it to a variety of [output formats](https://quarto.org/docs/output-formats/all-formats.html), including HTML, PDF, MS Word, etc.

The tutorials will make use of the ```matplotlib``` and ```plotly``` Python packages—the commands you can use to install them are given in the table below.

| Platform | Commands |
| -- | -- |
| Mac/Linux	| python3 -m pip install jupyter matplotlib plotly |
| Windows	| py -m pip install jupyter matplotlib plotly|

