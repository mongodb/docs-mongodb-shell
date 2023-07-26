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

Steps
~~~~~

.. procedure::
   :style: normal

   .. step:: Configure the package manager (``yum``).

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


   .. step:: Alternate Configuration: Download the .rpm File.

      If you are unable to add a MongoDB repository, uou can also
      download ``.rpm`` packages from the `MongoDB repository
      <https://repo.mongodb.org/yum/redhat/>`__.
     
       Downloads are organized in the following order:
            
            1. Red Hat or CentOS version (for example, ``8``)

            #. MongoDB edition (for example, ``mongodb-enterprise``)

            #. MongoDB :manual:`release version </reference/versioning>`
               (for example, ``{+mdb-version+}``)

            #. Architecture (for example, ``x86_64``)

        - id: aws2-tab
          name: Amazon Linux
          content: |


            You can also download the ``.rpm`` files directly from the
            `MongoDB repository
            <https://repo.mongodb.org/yum/amazon/>`__. Downloads are
            organized in the following order:
            
            1. Amazon Linux version (for example, ``2``)

            #. MongoDB :manual:`release version </reference/versioning>`
               (for example, ``{+mdb-version+}``)

            #. Architecture (for example, ``x86_64``)

---
title: Install ``mongosh``.
stepnum: 2
level: 4
ref: install
content: |

  .. include:: /includes/intro-openssl-installs.rst

  To install the latest stable version of ``mongosh`` with the included
  OpenSSL libraries:

  .. code-block:: sh

    sudo yum install -y mongodb-mongosh

  To install ``mongosh`` with your OpenSSL 1.1 libraries:

  .. code-block:: sh 

     sudo yum install -y mongodb-mongosh-shared-openssl11

  To install ``mongosh`` with your OpenSSL 3.0 libraries:

  .. code-block:: sh 

     sudo yum install -y mongodb-mongosh-shared-openssl3
...

