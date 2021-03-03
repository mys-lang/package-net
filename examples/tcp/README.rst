TCP networking
==============

Start a TCP server in one terminal. It waits for clients to connect
and echos any received data.

.. code-block:: text

   $ mys run server
   Accepting clients on localhost:59000.
   Client accepted.
   Echoing data.
   Echoing data.
   Echoing data.
   Disconnected.

Start a TCP client in another terminal. It connects to the server and
writes ``Hi!`` to it. The server responds with the same data and then
the connections is closed.

.. code-block:: text

   $ mys run client
   Connecting to localhost:59000.
   Connected.
   Sending 'Hi!'.
   Received 'Hi!'.
   Disconnecting.
