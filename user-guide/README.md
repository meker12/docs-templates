Templates to assist in creating user guides
===========================================

These are starting points for user guides that will be
constructed and published elsewhere:

* construct the guide's doc source in a GitHub repository
* publish the guide at developer.rackspace.com/user-guides/

Choosing a template
-------------------
User guides may have several basic outlines depending on their scope and purpose.
Find a template here that is close to meeting your needs;
copy it to your own GitHub repo and adapt it to present your content to your users.

If you use a different outline to create a user guide
and you can contribute that as a template here for others to use,
please do so.

*Template status as of 2015-12-30*

- user-guide-fragments

  - *not intended to build; usable*
  - details in README at https://github.com/rackerlabs/docs-templates/blob/master/user-guide/user-guide-fragments/README.md

- user-guide-product-family

  - *unfinished: published Cloud Core Infrastructure guide will be basis*
  - details in README at https://github.com/rackerlabs/docs-templates/blob/master/user-guide/user-guide-product-family/README.md

- user-guide-product-feature

  - *builds: usable*
  - details in README at https://github.com/rackerlabs/docs-templates/blob/master/user-guide/user-guide-product-feature/README.md

- user-guide-product-plus-prereqs

  - *unfinished: unpublished Auto Scale DIY will be basis*
  - details in README at https://github.com/rackerlabs/docs-templates/blob/master/user-guide/user-guide-product-plus-prereqs/README.md

- user-guide-single-product

  - *builds: usable*
  - details in README at https://github.com/rackerlabs/docs-templates/blob/master/user-guide/user-guide-single-product/README.md

Finding examples
----------------
Examining how other guides are constructed
is an excellent way to learn how to construct your own.

Doc source for user guides:
* https://github.com/rackerlabs?utf8=%E2%9C%93&query=user-guide
* https://github.com/rackerlabs/rs-heat-docs/
* if you know of others, list them here

Published user guides:
* https://developer.rackspace.com/docs/user-guides/
* https://developer.rackspace.com/docs/user-guides/orchestration/

Beginning to build your guide
-----------------------------
Two files establish the structure for publishing your guide,
building from its RST source in your GitHub repo
into a public-facing user guide at developer.rackspace.com/user-guides/:

* ``index.rst`` describes the toctree of other elements to assemble into the guide;
  for example, sections stored in separate files are included
  in the order specified by the ``toctree``directive in ``index.rst``.

* ``conf.py`` provides assembly instructions to Sphinx;
  for example, links outside the guide can be abbreviated
  as established by the ``extlinks`` dictionary in ``conf.py``.

Other details can vary depending on circumstances,
but you must have a valid index.rst and conf.py to begin assembling a guide.
For help identifying what to change for the type of guide you want to build,
follow the instructions in the README.md in the appropriate directory.

Getting help
------------
If you need help using these templates,
post an issue in this repo
at https://github.com/rackerlabs/docs-templates/issues.
