Installation With a ``.zip`` Archive
------------------------------------

Steps
~~~~~

.. procedure::
   :style: normal

   .. step:: Open the MongoDB Shell download page.

      .. include:: /includes/install/all-open-download.rst

   .. step:: Download ``mongosh``.

      Download the appropriate version of ``mongosh`` for your operating
      system. MongoDB provides versions of ``mongosh`` for Intel and ARM 
      architectures. 

   .. step:: Extract ``mongosh``.

      Go to the directory that contains the ``mongosh`` ``.zip``
      archive, then unpack the ``.zip`` file. 
      
      If your computer is Intel based, run:
      
      .. code-block:: sh

         unzip mongosh-{+version+}-darwin-x64.zip

      If your computer is ARM based (M1 or M2), run:
      
      .. code-block:: sh

         unzip mongosh-{+version+}-darwin-arm64.zip

      The extracted archive has a ``bin`` folder that contains two files,
      ``mongosh`` and ``mongosh_crypt_v1.dylib``.

      If your web browser automatically extracts the archive as part of the
      download, or if you extract the archive without using the ``unzip``
      command, you may need to make the binary executable. 
      
      To make the binary executable, run the following command in the
      directory where you extracted the archive:

      .. code-block:: sh

         chmod +x bin/mongosh

   .. step:: Add ``mongosh`` to your ``PATH``.

      .. include:: /includes/install/add-to-path.rst

   .. step:: Authorize macOS to run ``mongosh``.

      macOS may prevent ``mongosh`` from running after installation. If
      you receive a security error when starting ``mongosh`` indicating
      that the developer could not be identified or verified, perform
      the following actions:

      a. Open *System Preferences*.
      
      #. Select the *Security and Privacy* pane.

      #. Under the *General* tab, click the button to the right of the
         message about ``mongosh``, labelled either :guilabel:`Open
         Anyway` or :guilabel:`Allow Anyway` depending on your version
         of macOS.

