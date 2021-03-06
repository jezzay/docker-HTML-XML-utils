#docker-HTML-XML-utils

Automated Docker build of [HTML-XML-utils](http://www.w3.org/Tools/HTML-XML-utils) 

HTML-XML-utils provides a number of simple utilities for manipulating HTML and XML files.


Automated build available on [Docker Hub](https://hub.docker.com/r/jezzay/html-xml-utils/) and can be pulled with ```docker pull jezzay/html-xml-utils```

##Usage


Individual tools can be invoked by using ```docker run jezzay/html-xml-utils [tool name] [arguments]```

For example, ```cat index.html | docker run -i jezzay/html-xml-utils hxnormalize``` would run ```hxnormalize``` over the contents of Standard Input


Note the [-i option](https://docs.docker.com/engine/reference/run/#foreground) when using docker run to keep STDIN open. 

Using ```jezzay/html-xml-utils``` as a base Docker image allows access to all the installed tools in your container. 

ie using ```FROM jezzay/html-xml-utils``` in your Dockerfile.  


##Available tools:

- asc2xml		-  convert from UTF-8 to &#nnn; entities
- xml2asc		-  convert from &#nnn; entities to UTF-8
- hxaddid  		- add ID's to selected elements
- hxcite  		- replace bibliographic references by hyperlinks
- hxcite-mkbib  - expand references and create bibliography
- hxclean  		- apply heuristics to correct an HTML file
- hxcopy  		- copy an HTML file while preserving relative links
- hxcount 		- count elements and attributes in HTML or XML files
- hxextract  	- extract selected elements
- hxincl  		- expand included HTML or XML files
- hxindex  		- create an alphabetically sorted index
- hxmkbib  		- create bibliography from a template
- hxmultitoc 	- create a table of contents for a set of HTML files
- hxname2id 	- move some ID= or NAME= from A elements to their parents
- hxnormalize   - pretty-print an HTML file
- hxprune  		- remove marked elements from an HTML file
- hxnum         - number section headings in an HTML file
- hxpipe        - convert XML to a format easier to parse with Perl or AWK
- hxprintlinks  - number links & add table of URLs at end of an HTML file
- hxref         - generate cross-references
- hxremove      - remove selected elements from an XML file
- hxselect      - extract elements that match a (CSS) selector
- hxtabletrans  - transpose an HTML or XHTML table
- hxtoc         - insert a table of contents in an HTML file
- hxuncdata     - replace CDATA sections by character entities
- hxunent       - replace HTML predefined character entities to UTF-8
- hxunpipe      - convert output of pipe back to XML format
- hxunxmlns     - replace "global names" by XML Namespace prefixes
- hxwls         - list links in an HTML file
- hxxmlns       - replace XML Namespace prefixes by "global names"
