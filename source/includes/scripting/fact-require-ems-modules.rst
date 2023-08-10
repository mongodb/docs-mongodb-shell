Node.js modules are packaged in two formats. Newer modules use the
``ECMAScript`` standard. Older modules use the ``CommonJS`` (CJS)
format. You cannot ``require`` an ECMAScript module in ``mongosh``.

If you need to use an ECMAScript module, check to see if there is an
earlier CJS version that you can use instead. For more information, see:

- `Node.js module documentation
  <https://nodejs.org/api/esm.html#modules-ecmascript-modules>`__
- `npm package installation documentation
  <https://docs.npmjs.com/cli/v6/commands/npm-install>`__

