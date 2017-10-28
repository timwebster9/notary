# Notary

Project for running the [official Notary images](https://hub.docker.com/_/notary/), NOT using the dev/testing methods described in the [Docker Trust tutorial](https://docs.docker.com/engine/security/trust/trust_sandbox/), or as described in [running your own servce](https://github.com/theupdateframework/notary/blob/master/docs/running_a_service.md)

The TLS certificates and SQL files were obtained from the [Notary project](https://github.com/theupdateframework/notary)

## Use

Import the root CA from the project into your OS.  For example, on Ubuntu:

    sudo cp certs/root-ca.crt /usr/local/share/ca-certificates/root-ca.crt && sudo update-ca-certificates

Start the services:

    make up

Try the [Docker Trust tutorial](https://docs.docker.com/engine/security/trust/trust_sandbox/#playing-in-the-sandbox), starting at 'Test some trust operations', substituting 'https://localhost:4443' for your notary server URL (note: you'll need your own registry).
