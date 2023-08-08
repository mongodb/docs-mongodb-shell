You can check the build info of your ``mongosh`` binary by 
running the following from your terminal:

.. code-block:: sh

   mongosh --build-info

The command returns the following JSON document that describes your 
``mongosh`` build:

.. code-block:: javascript

   {
   "version": "1.10.1",
   "distributionKind": "packaged",
   "buildArch": "x64",
   "buildPlatform": "linux",
   "buildTarget": "unknown",
   "buildTime": "2023-06-21T09:49:37.225Z",
   "gitVersion": "05ad91b4dd40382a13f27abe1ae8c3f9f52a38f7",
   "nodeVersion": "v16.20.1",
   "opensslVersion": "3.1.1",
   "sharedOpenssl": true,
   "runtimeArch": "x64",
   "runtimePlatform": "darwin",
   "deps": {
      "nodeDriverVersion": "5.6.0"
   }
   }

You can check the build info of your ``mongosh`` binary with the 
``buildInfo()`` command. In ``mongosh`` run the following command:

.. code-block:: javascript

   buildInfo()

The command returns the following JSON document that describes your 
``mongosh`` build:

.. code-block:: javascript

   {
   version: '1.10.1',
   distributionKind: 'packaged',
   buildArch: 'x64',
   buildPlatform: 'linux',
   buildTarget: 'unknown',
   buildTime: '2023-06-21T09:49:37.225Z',
   gitVersion: '05ad91b4dd40382a13f27abe1ae8c3f9f52a38f7',
   nodeVersion: 'v16.20.1',
   opensslVersion: '3.1.1',
   sharedOpenssl: true,
   runtimeArch: 'x64',
   runtimePlatform: 'darwin',
   deps: {
      nodeDriverVersion: '5.6.0',
      libmongocryptVersion: undefined,
      libmongocryptNodeBindingsVersion: undefined
   }
   }