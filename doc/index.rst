|test|_

About
=====

Networking in the `Mys programming language`_.

Project: https://github.com/mys-lang/package-net

Examples
========

TCP client
----------

.. code-block:: python

   from net.tcp.client import Client

   def main():
       client = Client()
       client.connect("localhost", 5858)
       print("Connected!")
       client.write(b"Hi!")
       data = client.read(3)
       print(f"Got: {data}")

TCP server
----------

.. code-block:: python

   from net.tcp.server import Server

   def main():
       server = Server()
       server.listen(5858)
       client = server.accept()
       print("Connected!")
       data = client.read(3)
       print(f"Got: {data}")
       client.write(data)

Functions and types
===================

TCP client
----------

.. mysfile:: src/tcp/client.mys

TCP server
----------

.. mysfile:: src/tcp/server.mys

UDP socket
----------

.. warning:: UDP sockets are not yet implemented!

.. mysfile:: src/udp.mys

Secure TCP client
-----------------

.. warning:: Not yet implemented!

.. mysfile:: src/stcp/client.mys

.. |test| image:: https://github.com/mys-lang/package-net/actions/workflows/pythonpackage.yml/badge.svg
.. _test: https://github.com/mys-lang/package-net/actions/workflows/pythonpackage.yml

.. _Mys programming language: https://mys-lang.org
