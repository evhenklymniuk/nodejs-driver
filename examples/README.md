# Node.js Driver usage samples

This folder contains examples on how to use some features of the Node.js Driver for [Apache Cassandra][cassandra].

You should also visit the [Documentation][doc-index] and [FAQ][faq].

## Code samples
- Basic
  - [Connect](basic/basic-connect.js)
  - [Execute with promise-based API](basic/basic-execute.js)
  - [Execute using callbacks](basic/basic-execute-flow.js)
- Mapper
  - [Insert and retrieve using the Mapper](mapper/mapper-insert-retrieve.js)
- Metadata
  - [Get hosts information](metadata/metadata-hosts.js)
  - [Get keyspaces information](metadata/metadata-keyspaces.js)
  - [Get table information](metadata/metadata-table.js)
- User-defined types (UDT)
  - [Inserting and retrieving UDTs](udt/udt-insert-select.js)
- Tuples
  - [Inserting and retrieving Tuples](tuple/tuple-insert-select.js)
- Query tracing
  - [Retrieving the trace of a query request](tracing/retrieve-query-trace.js)

Each example is generally structured in a way where the `Client` is connected at the beginning and shutdown at the end.
While this is suitable for example single script purposes, you should reuse a single `Client` instance and
only call `client.shutdown()` when exiting your application.

If you have any questions regarding these examples, feel free to post your questions in the [mailing list][mailing-list].

[cassandra]: http://cassandra.apache.org/
[doc-index]: http://docs.datastax.com/en/developer/nodejs-driver/latest/
[mailing-list]: https://groups.google.com/a/lists.datastax.com/forum/#!forum/nodejs-driver-user
[faq]: http://docs.datastax.com/en/developer/nodejs-driver/latest/faq/
