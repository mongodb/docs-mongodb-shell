The ``mongosh`` shell returns output differently from the legacy
``mongo`` shell. If you have scripts that require the output to be
formatted in a similar way to the legacy ``mongo`` shell, try
reformatting the ``mongosh`` output with ``EJSON.stringify()``.
