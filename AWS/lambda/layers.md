# Dealing with Layers

## Python
### relevant links
* [General Layer Docs](https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html)
* [Lambda compatibility](https://aws.amazon.com/premiumsupport/knowledge-center/lambda-python-package-compatible/)
* [PyPi (python package distributor)](https://pypi.org/)
* [Example PyPi binary project](https://pypi.org/project/psycopg2-binary/)

### General Procedure
* Download the precompiled manylinux1_x86_64 version of the needed modules
* Prep a new folder tree with 'python/lib/python{version}/site-packages/'
  * ex: python/lib/python3.8/site-packages
  * you could probably include multiple versions worth in the lib directory
* uncompress the precompiled wheels into the proper version site-packages
* zip the python library into a zip folder named after the layer
* Python2 just uses python/ I believe, but why would you use python2
