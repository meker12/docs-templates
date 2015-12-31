.. Describe one action that one service can perform.
   Link to detailed explanations of how to perform that action through
   any available interfaces.

Rebuild
-------
The rebuild action rebuilds a server on the same physical host with
a selected base image or saved snapshot. The image that you select must be
within the same operating system family (Windows or Linux).
Your public and ServiceNet IP addresses are retained.
All data and disk formatting is lost.

.. seealso::

   Learn how to perform this action with the interface of your choice:

   .. hlist::
      :columns: 3

      * :kc-article:`Cloud Control Panel
        <managing-your-server-rebuild-a-cloud-server>`.
      * :rax-dev-docs:`Rackspace CLI
        </rack-cli/services/servers/#rebuild>`.
      * :rax-api:`your own software
        <api-ref.html#rebuildServer>`.
