This package contains co-citational network graphs for several keyword searches on the web of science. It allows readers to see how fields, in the aggregate, understand their own infrastructures of knowledge production.

It can be easily installed on any http server simply by uploading it as a package.

It can also be run on your own machine. Instructions for a Mac:
* Download and unzip this repository
* Open the application "Terminal"
* Open the downloaded folder in your file browser
* Navigate to that folder with "cd /PATH/TO/DIRECTORY" -- for instance, "cd ~/Downloads/clements_citation_graphs"
* Once in that folder in Terminal, run the command: "python -m SimpleHTTPServer"
* Open up a web browser and navigate to http://localhost:8000/
* You will see the html files that render these graphs

These graphs were generated with the following workflow:
* Run searches on web of science
* Export outputs (including citations!) in bibtex format
* Run the Refcliq analysis on it (this has become more difficult since the deprecation of Python 2)
* Open the .gexf file in Gephi
* Apply colors to the clusters using the Modularity Class parameter
* Run a force-directed layout algorithm on the .gexf file and save it
* Load the file in this pretty d3 format using one of the html files here as a template

To cut Gephi out of that workflow, you can render these graphs live with a little tweaking, as here: https://observablehq.com/@johnmulligan/typology-emotions-religion

