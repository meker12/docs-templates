
###Rackspace doc templates

Use the templates in this library to create developer and user 
documentation that is compatible with the [Rackspace documentation 
build and deploy platform](https://github.com/deconst). 

####Sphinx templates

Documentation is authored and built locally using the Sphinx documentation generator with 
source files in restructured text format which is the same technology behind content 
delivered by using ReadtheDocs.

**User Guide template**

Sphinx documentation project to create a User for a Rackspace service or product offering.

- Audience: Service consumers that want to use the product through the Cloud Control panel.
   
- Contents:

**Developer Guide template**

Sphinx documentation project to create a Developer Guide for a a service API like the 
[Cloud CDN API documentation](https://developer.rackspace.com/docs/cdn/v1/developer-guide/).

- Audience:  Application developers, operations, advanced users who want to use API services by 
  using submitting API requests from the command line or by using CLI technologies.
  
- Contents: A single-page html content architecture with the following sections: 
  - Developer Guide
  - Getting Started with the API (cURL or CLI)
  - API Reference
  - Release Notes

####Jekyll templates

The Rackspace build and deploy platform also supports Jekyll projects for other types of documentation content. For sample projects, see the following repositories:

- [Developer blog](https://github.com/rackerlabs/docs-developer-blog)
- [Carina documentation](https://https://github.com/getcarina/getcarina.com)

##Build and deploy

You can build deliverables based on these templates using any of the following options:

- Local builds with default Sphinx template.
  Use the Sphinx build make utility to get output rendered 
  with the default Sphinx templates and interface. 

- Local preview with Rackspace branding and UX.
  Install and use the [Deconst local client](https://github.com/deconst/client).

- For server builds and production deployment, contact the Developer documentation team for information on build 
  integration options and how to wire content into the [Docs landing page](https://developer.rackspace.com/docs/) on 
  developer.rackspace.com. 
  
  The process to add a deliverable to production, requires the following resources:

  - _deconst.json file that defines the contentID for the project. (*Example:* [Cloud Files _deconst.json](https://github.com/rackerlabs/docs-cloud-files/blob/master/rst/dev-guide/_deconst.json)) 
  
  - build configuration script  (*Example:* [Cloud files cibuild](https://github.com/rackerlabs/docs-cloud-files/tree/master/script))
  
  - Build integration script for Travis or another CI tool.  (*Example:* [Cloud Files](https://github.com/rackerlabs/docs-cloud-files/blob/master/.travis.yml))
  
  - Configure the content and routes in the [Control Repository](https://github.com/rackerlabs/nexus-control) config directory.  This step also specifies the templates to apply to the content.
   

####Docbook templates (Deprecated)

Documentation is authored and build locally using DocBook, Oxygen editor, and the maven 
Jenkins tool chain. 

You can install DocBook templates by using the Python project in the DocBook folder 
to create the DocBook source and build files for authoring and delivering the content. The 
project provides resources for a full set of Rackspace API service documentation including 
a Getting Started Guide, Release Notes, and Developer Guide.  

The resulting project can be built and deployed to [docs.rackspace.com](https://docs.rackspace.com) or 
[docs-internal.rackspace.com](https://docs-internal.rackspace.com).
