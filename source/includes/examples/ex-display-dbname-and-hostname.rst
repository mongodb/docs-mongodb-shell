Use a function like this one to display the database and hostname in
the :binary:`~bin.mongosh` prompt:

.. code-block:: javascript

   {
      const hostnameSymbol = Symbol('hostname');
      prompt = () => {
         if (!db[hostnameSymbol]) 
            db[hostnameSymbol] = db.serverStatus().host;
         return `${db.getName()}@${db[hostnameSymbol]}> `;
      };
   }

The prompt will look like this:

.. code-block:: javascript

   admin@centos0722:27502> 

