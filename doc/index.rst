|discord|_
|test|_
|stars|_

About
=====

Networking in the `Mys programming language`_.

Project: https://github.com/mys-lang/package-net

Examples
========

TCP client
----------

.. code-block:: mys

   from net.tcp.client import Client

   func main():
       client = Client()
       client.connect("localhost", 5858)
       print("Connected!")
       client.write(b"Hi!")
       data = client.read(3)
       print(f"Got: {data}")

TCP server
----------

.. code-block:: mys

   from net.tcp.server import Server

   func main():
       server = Server()
       server.listen(5858)
       client = server.accept()
       print("Connected!")
       data = client.read(3)
       print(f"Got: {data}")
       client.write(data)

API
===

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

.. |discord| image:: https://img.shields.io/discord/777073391320170507?label=Discord&logo=discord&logoColor=white
.. _discord: https://discord.gg/GFDN7JvWKS

.. |test| image:: https://github.com/mys-lang/package-net/actions/workflows/pythonpackage.yml/badge.svg
.. _test: https://github.com/mys-lang/package-net/actions/workflows/pythonpackage.yml

.. |stars| image:: https://img.shields.io/github/stars/mys-lang/package-net?style=social
.. _stars: https://github.com/mys-lang/package-net

.. _Mys programming language: https://mys-lang.org
