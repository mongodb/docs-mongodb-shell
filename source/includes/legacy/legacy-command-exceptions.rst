For commands whose output includes ``{ ok: 0 }``, ``mongosh`` returns a
consistent exception and omits the server raw output. The legacy
``mongo`` shell returned output that varied for each command.
