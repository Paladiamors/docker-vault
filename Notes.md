# Notes for modification

## Objective

The objective of this project is to provide an initialization mechanism for vault when in server mode. It is needed to initalize vault and auto unseal vault when there are no cloud methods available. Docker does not make it easier to run post startup scripts

## Method

We inject a startup script before the process starts and access the apis.
The necessary information are stored in the docker contianer and the necessary calls to initialize vault and unseal vault on start are made. A global token can be made available to all machines in some location to request and have their own certificates issued and signed by the CA. We can also
have puppet or a service manage the requesting of keys from a server on startup.


