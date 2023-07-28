Install With a ``.zip`` Archive
-------------------------------

Considerations
~~~~~~~~~~~~~~

.. include:: /includes/install/windows-considerations.rst

Steps
~~~~~

.. procedure::
   :style: normal

   .. step:: Go to the MongoDB Shell download page

      .. include:: /includes/install/all-open-download.rst

   .. step:: Download ``mongosh``

      Select the :guilabel:`Windows 64-bit (8.1+)` package from the 
      :guilabel:`Platform` dropdown, then click :guilabel:`Download`.

      The package is a ``.zip`` file.

   .. step:: Extract ``mongosh``

      Open a ``cmd`` terminal and run the following command from the
      directory that has the ``mongosh`` ``.zip`` archive:

      .. code-block:: sh
         tar -xf mongosh-{+version+}-win32-x64.zip

      The extracted archive has a ``bin`` folder that contains two
      files, ``mongosh.exe`` and ``mongosh_crypt_v1.dll``.

   .. step:: Add ``mongosh`` to your ``PATH``

      Ensure that the extracted |mdb-shell| binary is in the desired 
      location in your filesystem, then add that location to your ``PATH`` 
      environment variable.

      To add the |mdb-shell| binary's location to your 
      ``PATH`` environment variable:

      a. Open the :guilabel:`Control Panel`.

      #. In the :guilabel:`System and Security` category, click 
         :guilabel:`System`.

      #. Click :guilabel:`Advanced system settings`. The **System 
         Properties** modal displays.

      #. Click :guilabel:`Environment Variables`.

      #. In the *System variables* section, select ``Path`` and click 
         :guilabel:`Edit`. The **Edit environment variable** modal 
         displays.

      #. Click :guilabel:`New` and add the filepath to your ``mongosh`` 
         binary.

      #. Click :guilabel:`OK` to confirm your changes. On each other 
         modal, click :guilabel:`OK` to confirm your changes.

      To confirm that your ``PATH`` environment variable is correctly 
      configured to find ``mongosh``, open a command prompt and enter the 
      ``mongosh --help`` command. If your ``PATH`` is configured 
      correctly, a list of valid commands displays.