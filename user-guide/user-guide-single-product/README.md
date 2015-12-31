Userguide template for *single product*
=======================================
This directory contains a model of all the parts required
to construct one type of user guide.

Use the details in this README to help you develop your own guide
based on this model.
These are the high-level steps to take you from the model
to a publishable guide:

- copy the entire /user-guide-single-product/ directory
  to wherever you want to work with it
- install Sphinx and its prereqs
- ``make html`` to confirm that you can build
- customize your content
- ``make html`` to confirm that your customizations build
- merge your customized content into the master branch of your GitHub repository,
  signaling that you are ready to have it published

Examples
--------
**Nothing built from this template has been published yet.
Single-product Getting Started guides in the Knowledge Center,
such as https://www.rackspace.com/knowledge_center/article/getting-started-with-rackspace-intelligence,
are candidates for reformatting to this model.**

For example, the XXexampleXX guide is only about
XXexampleXX (still looking for the first published example);
one purpose of the guide is to help readers understand
the variety of options available within XXexampleXX.

This example is published at
*nowhere yet*.

Doc source for this example is maintained at
*nowhere yet*.

Alternatives
------------
If this template is not a good match for the user guide you intend to create,
examine the other templates in /docs-templates/user-guide/.

Customizing your guide
----------------------
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

- Create pages or sections
  introducing the guide itself,
  introducing the product covered in the guide,
  introducing the use of product interfaces,
  introducing configuration options,
  introducing pre-production hardening steps,
  and introducing guidelines for normal operation (`` toctree::``).

  Make these consistent with the navigation structure you describe
  in ``_toc.rst``.

**contactus.rst**

- Customize a contact-us page (/XXexampleXX-guide-intro/contactus.rst)
  with instructions for readers
  who have suggestions or questions (``:ref:``).  

**bestpractice.rst**

- Customize a best-practices page (/XXexampleXX-ops/bestpractice.rst)
  with advice about choosing wisely among available options.
  If you publish that advice elsewhere, such as in a blog, link to that here.

**keepup.rst**

- Customize a keeping-up page (/XXexampleXX-ops/keepup.rst)
  with advice about maintaining awareness of change.
  If you provide release notes, a news feed, a blog,
  or some other means of notifying
  users of changes and new ideas, link to that here.

**limits.rst**

- Customize a limits page (/XXexampleXX-ops/limits.rst)
  with details about rate limits, absolute limits, spending limits,
  or any other usage rules that can cause otherwise-valid operations to fail.
  If you provide a method for users to query or change their limits,
  explain or link to that here.

**somethingnew.rst**

- Customize a something-new page (/XXexampleXX-ops/somethingnew.rst)
  with details about how first-time use differs from ongoing operation.

**support.rst**

- Customize a support page (/XXexampleXX-ops/support.rst)
  with instructions about how to get help from Rackspace.
  If support can involve fees or is limited to specific hours or is controlled by
  a Service Level Agreement (SLA) or is only available to customers who have
  signed up for it, explain that here.

**troubleshoot.rst**

- Customize a troubleshooting page (/XXexampleXX-ops/troubleshoot.rst)
  with instructions about how to investigate and resolve problems.

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

**everywhere**

- Look for occurrences of ``XXexampleXX`` and replace those with
  filenames and content
  appropriate for this guide.

- Replace general-purpose sample content,
  borrowed from other user guides, with content
  directly relevant to this guide.

  For example, replace the problem-solving guidance in troubleshoot.rst
  with specific suggestions for solving problems with *this* product.

### Parts that assemble your content

**conf.py**

- Update ``project = u'Rackspace XXexampleXX User Guide'`` to name this project.

- Update the ``extlinks`` list to provide full URLs and abbreviated references for
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

Building your guide
-------------------
With sphinx installed in a virtual environment for your terminal session
(as described at
https://github.com/rackerlabs/docs-core-infra-user-guide/blob/master/README.md),
do this in your terminal session:

- ``cd`` to your local copy of the guide's doc source repository
- ``make html``

This builds your RST source into HTML in your local copy of the doc
source directory.

In your local copy of the doc source repository,
open ``/_build/html/index.html`` to see a rough approximation of the guide's
published form. This approximation is close enough to allow you to confirm basic
integrity (links work, images are included) but omits most formatting.

To see a local copy of the guide formatted as it will be
when published at developer.rackspace.com, install and use the deconst client
as instructed at https://github.com/deconst/client/blob/master/README.md.

Publishing your guide
---------------------
For initial setup, contact devdoc@rackspace.com to ask for help.
Pre-publication help is likely to come in two forms:
- with the DevEx team, establishing a connection between your guide's
  GitHub repository
  and the deconst engine that builds source into publishable documents
- with the DevDoc team, editing the guide to ensure it meets standards for
  Rackspace technical documentation and establishing an editorial review process
  for ongoing development of the guide

After your guide is published at developer.rackspace.com/docs/user-guides/,
changes to the master branch of the guide's doc source repository in GitHub
are tracked; merging a pull request into the master branch
causes the guide to be rebuilt and republished.
