# 200 - Basic Workflow

Quarto ```.qmd``` files contain a combination of markdown and executable code cells. Here’s what it might look like in VS Code to edit and preview a ```.qmd``` file:

![image](https://user-images.githubusercontent.com/1499433/199030032-56451e02-9ecb-4546-8837-e9060e1ec94a.png)

The document on the left is *rendered* into the HTML version you see on the right. This is the basic model for Quarto publishing—take a source document and render it to a variety of [output formats](https://quarto.org/docs/output-formats/all-formats.html), including HTML, PDF, MS Word, etc.

The tutorials will make use of the ```matplotlib``` and ```plotly``` Python packages—the commands you can use to install them are given in the table below.

| Platform | Commands | Commands behind a Proxy |
| -- | -- | -- |
| Mac/Linux	| python3 -m pip install jupyter matplotlib plotly | python3 -m pip install --proxy http://user:password@proxyserver:port jupyter matplotlib plotly |
| Windows	| py -m pip install jupyter matplotlib plotly| py -m pip install --proxy http://user:password@proxyserver:port jupyter matplotlib plotly |

**Note** that while this tutorial uses Python, using Julia (via the [IJulia](https://julialang.github.io/IJulia.jl/stable/) kernel) is also well supported. See the article on [Using Julia](https://quarto.org/docs/computations/julia.html) for additional details.


Verify if quarto has been installed successfully by running below command in a terminal inside Visual Studio Code:

```
$ quarto check
```

In case you get a prompt as follows: "WARNING: Specified QUARTO_PYTHON 'python' does not exist." do the following:

Step 1) Add a file ```_environment.local``` to the root directory of where you wnat to run the Quarto command (e.g. next to the .qmd files).

Step 2) Add the following line of text to the ```_environment.local``` file from the previous step:

```
QUARTO_PYTHON="FULL_PATH_TO_YOUR_PYTHON_EXECUTABLE"
```

Step 3) Replace FULL_PATH_TO_YOUR_PYTHON_EXECUTABLE by the actual full path to your Python executable (e.g., D:\python\python.exe).

Step 4) Close and reopen Visual Studio Code to initiate the environment variable.

Step 5) Re-run the following command to verify if QUARTO_PYTHON has now been successfully set:

```
$ quarto check
```
If still unable to find Python in Visual Studio Code, do the following:

Step 1) In VS Code, open the Settings with (Ctrl+,) then search settings for "Interpreter." There will an option for "Python: Default Interpreter Path." 

Step 2) Set the location of your python.exe file. 

Step 3) Open a new VS terminal with (Ctrl+Shift+`) to test the python command; you may need to restart VS Code.

I had trouble with VS being unable to locate python even though I could run python commands from any terminal opened from my computer (Windows Logo Key + cmd + Enter). I noticed that the Scripts folder was not installed on my python install, so I reinstalled python and followed the above steps. It worked for me.

VS Code has a python tutorial as well which includes a Select a Python Interpreter section (https://code.visualstudio.com/docs/python/python-tutorial).
