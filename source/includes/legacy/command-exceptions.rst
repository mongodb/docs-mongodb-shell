For commands where the output includes ``{ ok: 0 }``, ``mongosh``
returns an exception and doesn't return the raw output from the server.

.. note::

   In the legacy ``mongo`` shell, when a command's output included ``{
   ok: 0 }``, the behavior differs between commands. ``mongosh``
   always returns a consistent exception.
