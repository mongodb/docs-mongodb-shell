The legacy ``mongo`` shell used a configuration file called
``.mongorc.js``. If :binary:`mongosh` finds ``.mongorc.js`` on startup
but ``.mongoshrc.js`` isn't found, ``mongosh`` doesn't load the legacy
``.mongorc.js`` file and states you should rename ``.mongorc.js`` to
``.mongoshrc.js``.
