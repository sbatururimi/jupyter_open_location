# jupyter_open_location
A set of terminal commands to fix the "execution error: doesn’t understand the “open location” message." after the update to MacOS 10.12.5

# Description
After the upgrade to MacOS 10.12.5, launching a jupyter notebook doesn't open automatically the url in Safari/Chrome, even when launched from an Anaconda's source environment.
In order to fix that, launch your terminal and then type the following set of commands:
```
// to create ~/.jupyter_notebook_config.py if it does not exist:
jupyter notebook --generate-config
// open jupyter_notebook_config.py in a text edit program(ex: Sublime)
open ~/.jupyter_notebook_config.py
```
Then in your text file program, set :
```
c.NotebookApp.browser = u'Safari'
```

For Google Chrome:
```
c.NotebookApp.browser = u'chrome'
```
Save and use now your jupyter notebook as before by directly opening the browser page when a notebook is launched.
