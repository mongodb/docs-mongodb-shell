Starting in |mdb-shell| 2.4.0, you can use the ``history()`` command to
output a list of previously executed commands. For example:

.. code-block:: javascript

   history()

Example output, which shows a list of commands in an array of strings:

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
