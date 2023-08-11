There are two packing standards for Node.js modules. 
- ``CommonJS`` (CJS)
- ``ECMAScript``

Older modules use ``CommonJS`` (CJS). Newer modules use the
``ECMAScript`` standard. You cannot ``require`` an ECMAScript module in
``mongosh``.

If you want to use an ECMAScript module, check to see if there is an
earlier CJS version that you can use instead. For more information, see:

- `Node.js module documentation
  <https://nodejs.org/api/esm.html#modules-ecmascript-modules>`__
- `npm package installation documentation
  <https://docs.npmjs.com/cli/v6/commands/npm-install>`__

