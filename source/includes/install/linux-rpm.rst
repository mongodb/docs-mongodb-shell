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

Installation Methods
~~~~~~~~~~~~~~~~~~~~

When you use an ``.rpm`` package to install ``mongosh``, the ``.rpm``
package can be hosted in a :ref:`repository <mongosh-rpm-repo>` or it
can be a :ref:`local copy <mongosh-rpm-local>`. 

.. _mongosh-rpm-repo:

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

      .. include:: /includes/install/linux-openssl-installs.rst

      .. include:: /includes/install/linux-rpm-ssl-packages.rst

      To install ``mongosh``, uncomment and run one of the following
      commands. Only run the command that matches your configuration. 

      .. code-block:: sh

         # sudo yum install -y mongodb-mongosh
         # sudo yum install -y mongodb-mongosh-shared-openssl11
         # sudo yum install -y mongodb-mongosh-shared-openssl13

.. _mongosh-rpm-local:

Install from a Local .rpm File
``````````````````````````````

You can download ``.rpm`` packages from the MongoDB repository and use
them to install ``mongosh``.

.. include:: /includes/install/linux-openssl-installs.rst

.. include:: /includes/install/linux-rpm-ssl-packages.rst

Download the package that corresponds to your OpenSSL configuration.

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

      To install ``mongosh``, uncomment one of the following commands
      and edit the path to your ``.rpm``. Only run the command that
      matches your configuration. 

      .. code-block:: sh

         # sudo yum localinstall -y /path/to/mongodb-mongosh-{+version+}.x86_64.rpm
         # sudo yum localinstall -y /path/to/mongodb-mongosh-shared-openssl11-{+version+}.x86_64.rpm
         # sudo yum localinstall -y /path/to/mongodb-mongosh-shared-openssl13-{+version+}.x86_64.rpm

