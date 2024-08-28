``mongosh`` formats query output differently than the deprecated
``mongo`` shell. You may have scripts which rely on the old format. To
reformat ``mongosh`` output on a single line, use ``EJSON.stringify()``.
