Rackspace doc templates 
=========================

Use the templates in this library to create developer and user 
documentation that is compatible with the [Rackspace documentation 
build and deploy platform](https://github.com/deconst). 

##Sphinx templates

Documentation is authored and built locally using the Sphinx documentation generator with 
source files in restructured text format which is the same technology behind content 
delivered by using ReadtheDocs.

###User Guide template


###Developer Guide template

Sphinx documentation project to create a Developer Guide for a a service API like the 
[Cloud CDN API documentation](https://developer.rackspace.com/docs/cdn/v1/developer-guide/).
  
####Audience 
   
Application developers, operations, advanced users who want to use API services by 
using submitting API requests from the command line or by using CLI technologies.
  
####Contents 
  
   - Developer Guide
   - Getting Started with the API (cURL or CLI)
   - API Reference
   - Release Notes

##Jekyll templates

The Rackspace build and deploy platform also supports Jekyll projects for other types of documentation content. For sample projects, see the following repositories:

- [Developer blog](https://github.com/rackerlabs/docs-developer-blog)
- [Carina documentation](https://https://github.com/getcarina/getcarina.com)

##Build and deploy

  Build content locally by using the Sphinx build make utility to get output rendered 
  with the default Sphinx templates and interface. 

  To deliver Rackspace-branded documentation build your content with the following build 
  technologies.
   
  Build a local preview of Rackspace-branded content by using the 
  [Deconst local client](https://github.com/deconst/client]. 
  
  To build and deploy to a production server, contact the Developer documentation team 
  for information on build integration and wiring content into the Rackspace documentation 
  landing pages.

####Docbook templates (Deprecated)

Documentation is authored and build locally using DocBook, Oxygen editor, and the maven 
Jenkins tool chain. 

You can install DocBook templates by using the Python project in the DocBook folder 
to create the DocBook source and build files for authoring and delivering the content. The 
project provides resources for a full set of Rackspace API service documentation including 
a Getting Started Guide, Release Notes, and Developer Guide.  

The resulting project can be built and deployed to [docs.rackspace.com](https://docs.rackspace.com) or 
[docs-internal.rackspace.com](https://docs-internal.rackspace.com).
