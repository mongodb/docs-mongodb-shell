You can either:

- Copy the ``mongosh`` binary into a directory listed in your
  ``PATH`` variable, such as ``/usr/local/bin``. Run the following
  commands from the directory where you extracted the download file:

  .. code-block:: sh

    sudo cp mongosh /usr/local/bin/
    sudo cp mongosh_crypt_v1.so /usr/local/lib/

- Create symbolic links to the ``MongoDB Shell``. Switch to the
  directory where you extracted the files from the ``.tgz`` archive.
  Run the following command to create links to a directory already
  in your ``PATH`` such as ``/usr/local/bin``. 

  .. code-block:: sh

     sudo ln -s $(pwd)/bin/* /usr/local/bin/

