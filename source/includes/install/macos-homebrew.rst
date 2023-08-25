Installation With Homebrew
--------------------------

To view the complete list of system requirements for Homebrew,
see the `Homebrew Website <https://docs.brew.sh/Installation>`__.

Considerations
~~~~~~~~~~~~~~

``mongosh`` installed with Homebrew does not support
:ref:`automatic client-side field level encryption
<csfle-fundamentals>`.

You can use the core ``Homebrew`` tap to install ``mongosh`` or
you can add the `MongoDB supported tap
<https://github.com/mongodb/homebrew-brew>`__.

Steps
~~~~~

.. procedure::
   :style: normal

   .. step:: Install Homebrew.

      If Homebrew is not already installed, refer to the `Homebrew
      <https://brew.sh/>`__ website to install Homebrew on macOS.

   .. step:: Install the ``mongosh`` package.

      To install ``mongosh``, run this command from the terminal:

      .. code-block:: sh

         brew install mongosh

