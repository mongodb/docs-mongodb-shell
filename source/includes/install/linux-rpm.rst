Installation With an .rpm Package
---------------------------------

Supported Platforms
~~~~~~~~~~~~~~~~~~~

``mongosh`` is available as an ``.rpm`` package for the following
platforms:

- Red Hat Enterprise Linux (RHEL)
- Amazon Linux 2

.. important:: Amazon Linux 2023 Availability

   ``mongosh`` is **not** currently available on Amazon
   Linux 2023.

Supported Installation Methods
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You can use an ``.rpm`` package to install ``mongosh``. The ``.rpm``
package can be hosted in a repository or it can be a local copy. 

Install from a Repository
`````````````````````````

.. procedure::
   :style: normal

   .. step:: Configure a source repository. 

      There are ``.rpm`` distributions for RHEL and Amazon Linux.

      .. include:: /includes/install/linux-did-you-create-a-repo.rst

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

   .. step:: Install ``mongosh``.

      .. include:: /includes/intro-openssl-installs.rst

      To install the latest stable version of ``mongosh`` with the
      included OpenSSL libraries, run ``yum``. 

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

Install from a Local .rpm File
``````````````````````````````

You can download ``.rpm`` packages from the MongoDB repository and use
them to install ``mongosh``.

For RHEL, the repository is organized in the following way:

- The base URL: 

  .. code-block:: shell

     https://repo.mongodb.org/yum/redhat

- Red Hat or CentOS version
- MongoDB edition
- MongoDB release version
- Architecture
- The full URL resembles:

  .. code-block:: shell

     https://repo.mongodb.org/yum/redhat/8/mongodb-org/{+mdb-version+}/x86_64/RPMS/mongodb-mongosh-{+version+}.x86_64.rpm

For Amazon Linux, the repository is organized in the following
way:

- The base URL: 

  .. code-block:: shell

     https://repo.mongodb.com/yum/amazon/
 
- Amazon Linux version
- MongoDB release version
- Architecture
- The full URL resembles:

  .. code-block:: shell

     https://repo.mongodb.com/yum/amazon/2/mongodb-org/{+mdb-version+}/x86_64/RPMS/mongodb-mongosh-{+version+}.x86_64.rpm

.. procedure::
   :style: normal

   .. step:: Install ``mongosh``.

      .. include:: /includes/intro-openssl-installs.rst

      To install the latest stable version of ``mongosh`` with the
      included OpenSSL libraries, update the path and run:

      .. code-block:: sh

        sudo yum localinstall -y /path/to/mongodb-mongosh.rpm

      To install ``mongosh`` with your system's OpenSSL 1.1 libraries,
      update the path and run:

      .. code-block:: sh 

         sudo yum localinstall -y /path/to/mongodb-mongosh-shared-openssl11.rpm

      To install ``mongosh`` with your system's OpenSSL 3.0 libraries,
      update the path and run:

      .. code-block:: sh 

         sudo yum localinstall -y /path/to/mongodb-mongosh-shared-openssl3.rpm

