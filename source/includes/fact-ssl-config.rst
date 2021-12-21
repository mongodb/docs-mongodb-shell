
If ``--tlsCAFile`` or ``net.tls.CAFile`` (or their aliases
``--sslCAFile`` or ``ssl.CAFile``) is not specified,
:binary:`~bin.mongosh` uses the system-wide CA certificate store to
connect to an TLS/SSL-enabled server.

To use x.509 authentication, you must specify ``--tlsCAFile`` or
``net.tls.CAFile`` unless you are using ``--tlsCertificateSelector``
or ``--net.tls.certificateSelector``.

