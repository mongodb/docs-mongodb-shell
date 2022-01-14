Use a function like this one for a prompt that shows the system uptime
and a count of documents across all collections in the current
database.

.. code-block:: javascript

   
   prompt = function() {
      return "Uptime:" + db.serverStatus().uptime +
             " Documents:" + db.stats().objects +
             " > ";
      }

