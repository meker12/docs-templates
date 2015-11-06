Userguide template for *product family*
=======================================
This directory contains a model of all the parts required
to construct one type of user guide.

Examples
--------
For example, the Cloud Core Infrastructure Services guide discusses
several products as complementary members of a set;
one purpose of the guide is to help readers
choose from within the set the most appropriate product or products
for their use case.

This example is published at
https://developer.rackspace.com/docs/user-guides/infrastructure/.

Doc source for this example is maintained at
https://github.com/rackerlabs/docs-core-infra-user-guide.

Alternatives
------------
If this template is not a good match for the user guide you intend to create,
examine the other templates in /docs-templates/user-guide.

Customization instructions
--------------------------
Copy all the parts from this folder to your own GitHub repo,
then customize them there to present your own content.

**index.rst**
This is the starting point for a guide to
a group of three imaginary related products.
Members of the group may be useful for similar purposes,
so ``index.rst`` shapes the guide
to help readers notice
points of difference and similarity and choose appropriately among them.

- Replace all occurrences of ``XXexampleXX``
  with something identifying this
  group of related products: compute? storage? network?
  database? security?
  If you can, name the group consistently with groups
  readers encounter elsewhere in their experiences at Rackspace, especially in the Rackspace Cloud Control Panel.

- Replace all occurrences of ``XXexample01XX``
  with something identifying the first member of the group.
  If you can, name this member consistently with the name used for it elsewhere at Rackspace, especially in the Rackspace Cloud Control Panel.

- Replace all occurrences of ``XXexample02XX``
  with something identifying the first member of the group.
  If you can, name this member consistently with the name used for it elsewhere at Rackspace, especially in the Rackspace Cloud Control Panel.

- Replace all occurrences of ``XXexample03XX``
  with something identifying the first member of the group.
  If you can, name this member consistently with the name used for it elsewhere at Rackspace, especially in the Rackspace Cloud Control Panel.

- If needed, expand the table
  to include additional members of the group.

- For all members of the group:
  - Store a copy of the official logo in ``/_images/``
    and include it in the table from there
    (``.. image::``).
  - Use alternate text to identify the product represented by the logo
    (``:alt:``).
  - Under the logo, include a brief verbal introduction to the product.
  - Create sections introducing product concepts, product actions, and any
    interfaces capable of interacting with the product
    (probably GUI, CLI, and API) (``:ref:``).

- For the guide:
  - Create a contact-us page (``:ref:``) and pages or sections
    introducing the guide itself,
    introducing the group of products covered in the guide,
    introducing the use of product interfaces,
    introducing configuration options,
    introducing pre-production hardening steps,
    and introducing guidelines for normal operation (`` toctree::``).

**conf.py**

MORE COMING SOON
