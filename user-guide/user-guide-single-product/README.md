Userguide template for *single product*
=======================================
This directory contains a model of all the parts required
to construct one type of user guide.

Examples
--------
For example, the Cloud Orchestration Templates guide is only about
setting up templates for Cloud Orchestration;
one purpose of the guide is to help readers understand
the variety of options available within Cloud Orchestration.

This example is published at
https://developer.rackspace.com/docs/user-guides/orchestration/.

Doc source for this example is maintained at
https://github.com/rackerlabs/rs-heat-docs/.

Alternatives
------------
If this template is not a good match for the user guide you intend to create,
examine the other templates in /docs-templates/user-guide.

Customization instructions
--------------------------
Copy all the parts from this folder to your own GitHub repo,
then customize them to present your own content as noted here.

### Parts that are your content

**index.rst**

This is the starting point for a guide to
one product.
``index.rst`` shapes the guide
to help readers notice
important features of the product and learn to use them.

- Replace all occurrences of ``XXexampleXX``
  with something identifying this
  product.
  If you can, name the product consistently with the name for it that
  readers encounter elsewhere in their experiences at Rackspace,
  especially in control panels.

- Create a contact-us page with instructions for readers
  who have suggestions or questions (``:ref:``).

- Create pages or sections
  introducing the guide itself,
  introducing the product covered in the guide,
  introducing the use of product interfaces,
  introducing configuration options,
  introducing pre-production hardening steps,
  and introducing guidelines for normal operation (`` toctree::``).

  Make these consistent with the navigation structure you describe
  in ``_toc.rst``.

**/_images/**

- Store images here that you want to include anywhere
  in the guide.

  For example, if you have a drawing in ``/_images/cloudimagesharing.png``,
  you can include it anywhere in the guide with
  ``.. figure:: /_images/cloudimagesharing.png``.

  You can see this demonstrated at ``index.rst``.
  Remove the demonstration if you do not wish to include it in
  the published guide.

- If an image requires a source document for maintenance,
  include that source document in ``/_images/``.

  For example, cloudimagesharing.png was created at www.draw.io;
  you can change it there by opening cloudimagesharing.xml.

**/_common/**

- Store text fragments here that you want to include anywhere
  in the guide.

  For example, if you have a warning in ``/_common/warning-draft.txt``,
  you can include it anywhere in the guide with
  ``.. include:: /_common/warning-draft.txt``.

  You can see this demonstrated at ``index.rst``.
  Remove the demonstration if you do not wish to include it in
  the published guide.

### Parts that assemble your content

**conf.py**

- Update ``project = u'Rackspace XXexampleXX User Guide'`` to name this project.

- Update the ``extlinks`` list to provide full URLs abbreviated references for
  sites outside this guide that you link to repeatedly.

  Even if you change nothing else in ``extlinks``,
  change the definition of ``'git-repo'``
  to point to the doc source repository for this guide.

- Update ``html_short_title = 'XXexampleXX Guide'`` to name this guide.

- Update ``htmlhelp_basename = 'XXexampleXXGuidedoc'`` to name this document.

- Update ``latex_documents = [
  (master_doc, 'RackspaceXXexampleXXGuide.tex',
  u'Rackspace XXexampleXX Guide Documentation',
  u'Rackspace', 'manual'),]`` to create a LaTex document tree structure.

- Update ``man_pages = [
    (master_doc, 'rackspaceXXexampleXXuserguide', u'Rackspace XXexampleXX Guide Documentation',
    [author], 1)]`` to create a manual page structure.

**_toc.rst**

- Update ``XXexampleXX User Guide <self>`` to show the guide's title for the
  top of the left-hand navigation bar.

- Update the remainder of ``toc.rst`` to list sections in the order they should
  appear in the left-hand navigation bar.

**_deconst.json**

- Update ``"contentIDBase": "https://github.com/rackerlabs/XXexampleXX/"``
  to identify the GitHub repository containing this guide's doc source.

**.travis.yml**

- This file has credentials for production and staging servers,
  and for notifications in Slack.
  I don't know how to generate them.
