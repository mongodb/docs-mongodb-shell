Installation With an .rpm Package
---------------------------------

Supported Platforms
~~~~~~~~~~~~~~~~~~~

``mongosh`` is available as an ``.rpm`` package for the following
platforms:

- :abbr:`RHEL (Red Hat Enterprise Linux)`
- Amazon Linux 2

.. important:: Amazon Linux 2023 Availability

   ``mongosh`` is **not** currently available on Amazon
   Linux 2023.

Before you Begin
~~~~~~~~~~~~~~~~

Before you install an ``.rpm`` package, you have to configure a
repository or download a local copy of the package.

Configure the package manager (``yum``)
```````````````````````````````````````

There are ``.rpm`` distributions for RHEL and Amazon Linux.

Create a repository file for your platform so that you can use 
``yum`` to install ``mongosh`` rpms. 

If you use RHEL, paste this code into
``/etc/yum.repos.d/mongodb-org-{+mdb-version+}.repo``:

.. code-block:: shell

   [mongodb-org-{+mdb-version+}]
   name=MongoDB Repository
   baseurl=https://repo.mongodb.org/yum/redhat/$releasever/mongodb-org/{+mdb-version+}/$basearch/
   gpgcheck=1
   enabled=1
   gpgkey=https://www.mongodb.org/static/pgp/server-{+pgp-version+}.asc

If you use Amazon Linux, paste this code into
``/etc/yum.repos.d/mongodb-org-{+mdb-version+}.repo``:

.. code-block:: shell

   [mongodb-org-{+mdb-version+}]
   name=MongoDB Repository
   baseurl=https://repo.mongodb.org/yum/amazon/$releasever/mongodb-org/{+mdb-version+}/$basearch/
   gpgcheck=1
   enabled=1
   gpgkey=https://www.mongodb.org/static/pgp/server-{+pgp-version+}.asc 

Download the .rpm File
``````````````````````

If you are unable to add a MongoDB repository, you can also
download ``.rpm`` packages from the MongoDB repository. You need to
provide the path to the downloaded package when you run ``yum`` to
install ``mongosh``.

For RHEL, the repository is organized in the following way:

   1. The base URL: 

      .. code-block:: shell

         https://repo.mongodb.org/yum/redhat

    #. Red Hat or CentOS version (for example, ``8``)

    #. MongoDB edition (for example, ``mongodb-enterprise``)

    #. MongoDB :manual:`release version </reference/versioning>`
       (for example, ``{+mdb-version+}``)

    #. Architecture (for example, ``x86_64``)

  The full URL resembles:

  .. code-block:: shell

     https://repo.mongodb.org/yum/redhat/9/mongodb-org/{+mdb-version+}/x86_64/RPMS/mongodb-mongosh-1.9.1.x86_64.rpm

For Amazon Linux, the repository is organized in the following
way:

   1. The base URL: 

      .. code-block:: shell

         https://repo.mongodb.org/yum/amazon/
    
    #. Amazon Linux version (for example, ``2``)

    #. MongoDB :manual:`release version </reference/versioning>`
       (for example, ``{+mdb-version+}``)

    #. Architecture (for example, ``x86_64``)

The full URL resembles:

.. code-block:: shell

   https://repo.mongodb.org/yum/amazon/2/mongodb-org/{+mdb-version+}/x86_64/RPMS/mongodb-mongosh-1.9.1.x86_64.rpm

Steps
~~~~~

.. procedure::
   :style: normal

   .. step:: Install ``mongosh``.

      .. include:: /includes/intro-openssl-installs.rst

      To install the latest stable version of ``mongosh`` with the
      included OpenSSL libraries, run:

      .. code-block:: sh

        sudo yum install -y mongodb-mongosh

      To install ``mongosh`` with your system's OpenSSL 1.1 libraries,
      run:

      .. code-block:: sh 

         sudo yum install -y mongodb-mongosh-shared-openssl11

      To install ``mongosh`` with your system's OpenSSL 3.0 libraries,
      run:

      .. code-block:: sh 

         sudo yum install -y mongodb-mongosh-shared-openssl3

