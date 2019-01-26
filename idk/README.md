Hardening-Hidden-Services-At-The-Application-Level
==================================================

A living guide to the pitfalls of configuring various types of hidden services.
Right now it's just an index of topics that I'm eventually going to write more
in-depth articles on. They won't be written in order, some of them are partly
done, those will be added first.

Part One: Don't Transmit Information about the Local Host
---------------------------------------------------------

  1. Assure that all debugging information is disabled or inaccessible.
  2. Don't tell others what server you are using via an error page, header or
    other straightforward or configurable meta-data.
  3. Don't transmit information about the host via the server.

Example 1: nginx

Example 2: lighttpd

Part Two: Don't Correlate to a Clearnet Service
-----------------------------------------------

  1. Only serve on the local host.
  2. Don't re-use security information across services.
  3. Audit calls to external services

Example 3: ssh

Part Three: Don't Connect to Other Services Without a Proxy
-----------------------------------------------------------

  1. Disabling outgoing connecions entirely
  2. Using Morty and Privoxy to sanitize and route outgoing requests made by
    a server, and what to do when you cannot.

Example 4: PHPbb

Example 5: gitea

Part Four: Preventing Information Leaking by Exploitation
---------------------------------------------------------

  1. Using VM's and Containers to keep the application from leaking information
    about the host by accident.

Example 6: Docker

Example 7: Qubes
