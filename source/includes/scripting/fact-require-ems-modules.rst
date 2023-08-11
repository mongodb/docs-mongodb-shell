There are two packing standards for Node.js modules.

.. list-table::
   :header-rows: 1

   * - Standard
     - Works with ``require()`` ``mongosh``

   * - ``CommonJS`` (CJS)
     -  Yes

   * - ``ECMAScript``
     -  No

You can ``require`` a CommonJS module in ``mongosh``. You cannot
``require`` an ECMAScript module. If you want to use an ECMAScript
module, check to see if there is a CommonJS version that you can use
instead. For more information, see:

- `Node.js module documentation
  <https://nodejs.org/api/esm.html#modules-ecmascript-modules>`__
- `npm package installation documentation
  <https://docs.npmjs.com/cli/v6/commands/npm-install>`__

