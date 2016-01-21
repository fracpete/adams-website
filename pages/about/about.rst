.. title: About
.. slug: about
.. date: 2015-12-18 14:50:32 UTC+13:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
.. author: FracPete

.. contents::

The core of ADAMS is the *workflow engine*, which follows the philosophy of *less
is more*. Instead of letting the user place operators (or actors in ADAMS terms)
on a canvas and then manually connect inputs and outputs, ADAMS uses a
tree-like structure. This structure and the control actors define how the
data is flowing in the workflow, no explicit connections necessary. The
tree-like structure stems from the internal object representation and the
nesting of sub-actors within actor-*handlers*.


Features
========

.. csv-table::
  :header: "Feature","Available"

  "Machine learning/data mining","WEKA_, WEKA webservice, MOA_, MEKA_, parameter optimization, experiment generation on-the-fly, setup generators, time series"
  "Data processing","WEKA_, `R-Project <R_>`_, XML, XSLT, XPath, HTML, JSON"
  "Streaming","MOA_, Twitter (record/replay)"
  "Spreadsheets","MS Excel (r/w), ODF_ (r/w), CSV (r/w), Gnumeric_ (r/w)"
  "Databases","`MS Access <MSAccess_>`_, MySQL_, SQLite_, JDBC_"
  "Imaging","ImageJ_, JAI_, BoofCV_, ImageMagick_, Gnuplot_, LIRE_, OCR (tesseract_), Barcodes (Zxing_)"
  "Graphics output","BMP, JPG, PNG, TIF, PDF, RAW (dcraw_, ufraw_)"
  "Visualization","Scatter and line plots, Control charts, Images, GIS (OpenStreetMap_)"
  "Scripting","Groovy_, Jython_"
  "Documentation","DocBook_, HTML"
  "Web","HTTP, FTP, SFTP, SSH, Email, `Webservices <CXF_>`_"
  "Other","de/-compression (tar, zip, bzip2, gzip, lzma), Java code generation"

.. _WEKA: http://www.cs.waikato.ac.nz/ml/weka/ 
.. _MOA: http://moa.cms.waikato.ac.nz/
.. _MEKA: http://meka.sourceforge.net/
.. _R: http://www.r-project.org/
.. _ODF: http://en.wikipedia.org/wiki/OpenDocument
.. _Gnumeric: http://www.gnumeric.org/
.. _Twitter: http://twitter4j.org/
.. _MSAccess: http://jackcess.sourceforge.net/
.. _MySQL: http://www.mysql.com/
.. _SQLite: https://sqlite.org/
.. _JDBC: https://en.wikipedia.org/wiki/Java_Database_Connectivity
.. _ImageJ: http://imagej.nih.gov/ij/
.. _JAI: http://en.wikipedia.org/wiki/Java_Advanced_Imaging
.. _BoofCV: http://boofcv.org/
.. _ImageMagick: http://www.imagemagick.org/
.. _Gnuplot: http://gnuplot.info/
.. _LIRE: http://code.google.com/p/lire/
.. _tesseract: https://code.google.com/p/tesseract-ocr/
.. _Zxing: https://github.com/zxing/zxing
.. _dcraw: http://www.cybercom.net/~dcoffin/dcraw/
.. _ufraw: http://ufraw.sourceforge.net/index.html
.. _OpenStreetMap: http://www.openstreetmap.org/
.. _Groovy: http://groovy.codehaus.org/
.. _Jython: http://jython.org/
.. _DocBook: http://www.docbook.org/
.. _CXF: http://cxf.apache.org/


Example flow
============

.. image:: ../../images/flow_snippet.png

* Horizontal and vertical indicators show how the data flows
* Each actor has its own icon, since the name can be changed arbitrarily
* Four types of actors: standalone (red; no input, no output), source (orange;
  only output), transformer (green; input and output) and sink (greyl; only
  input)
* Control actors, i.e., actors that determine the flow of data or flow execution are blue
* Actors with parameters usually show a so-called quick info on the right-hand
  side of the name, to give the user an idea how the actor is parametrized
  without having to open up the dialog with the options.