The legacy :binary:`~bin.mongo` shell used a configuration file called
``.mongorc.js``. If :binary:`mongosh` detects this file on startup and
``.mongoshrc.js`` is not available, :binary:`mongosh` doesn't load the
legacy ``.mongorc.js`` file, and states you should rename
``.mongorc.js`` to ``.mongoshrc.js``.
