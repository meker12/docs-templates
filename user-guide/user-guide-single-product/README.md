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
then customize them there to present your own content.

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

**conf.py**

MORE COMING SOON
