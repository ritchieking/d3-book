Chapter 7: Loading and Filtering External Data
==========

##Files

Name | Description
---|---------
`index.html` | The index file that creates the example bar chart in D3 by grabbing data from an external data file
`allData.csv` | An external data file containing all of the age distribution data in comma-seperated values format

##More Information

As mentioned in the text, you'll need to create a local server on your machine to be able to request data from external resources, like `allData.csv`. You can do this really easily with Python. If you're on a Mac, Python comes pre-installed, but if you're on a Windows or Linux machine, you'll need to [download it here](https://www.python.org/download).

Once you have Python installed, you can create a local server by opening up your terminal or command line, navigating to the directory where your project is, and entering in the following:
    
__For Python version 3 and up__

    python -m http.server 8888 &

__Earlier versions__

    python -m SimpleHTTPServer 8888 &

