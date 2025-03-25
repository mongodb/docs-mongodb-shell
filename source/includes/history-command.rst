Starting in |mdb-shell| 2.4.0, you can use the ``history()`` command to
display the command history for the current session. This command shows
a list of all the commands that have been executed in the current
mongosh session.

This will output a list of previously executed commands, allowing you to
review your command history directly within the shell.

For example:

.. code-block:: javascript

   history()

Example output:

.. code-block:: javascript
   :copyable: false

   [
     'db.salesFromFile.find()',
     '   let salesCollection = JSON.parse( db.sales.find().toArray() )   ',
     '   let salesCollection = JSON.parse( db.sales.find() )   ',
     '   let salesCollection = EJSON.stringify( db.sales.find().toArray() )   ',
     "   fs.writeFileSync( 'salesDeserialize.json', salesCollection ) ",
     'db.salesFromFile.find()',
     'db.salesFromDeserializeFile.find()',
     'db.salesFromDeserializeFile.drop()',
     'exit',
     ...
  ]
