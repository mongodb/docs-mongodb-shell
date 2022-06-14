To update the :binary:`~bin.mongosh` prompt to display line numbers, run
the following code inside ``mongosh``:

.. code-block:: javascript

   let cmdCount = 1;
   prompt = function() {
                return (cmdCount++) + "> ";
            }

The prompt will look like this:

.. code-block:: javascript

   1> show collections
   2> use test
   3>
