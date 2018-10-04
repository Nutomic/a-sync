## This project was merged into [syncthing-lite](https://github.com/syncthing/syncthing-lite). The repository only exists for historic reasons.

[![MPLv2 License](https://img.shields.io/badge/license-MPLv2-blue.svg?style=flat-square)](https://www.mozilla.org/MPL/2.0/)

This project is an java client implementation of [Syncthing][1] protocols. It is made of several modules, providing:

 1. a command line utility for accessing a Syncthing network (ie a network of devices that 
 speak Syncthing protocols)'

 2. a service implementation for the 'http-relay' protocol (that proxies 'relay' protocol 
 over an http connection);

 3. a client library for Syncthing protocol, that can be used by third-party applications 
 (such as mobile apps) to integrate with Syncthing.

Care is taken to make sure the client library is compatible with android (min sdk 19), so it 
can be used for the [syncthing-lite][2] project.

This is a client-oriented implementation, designed to work online by downloading and
uploading files from an active device on the network (instead of synchronizing a local copy 
of the entire repository). This is quite different from the way the [syncthing-android][3] app
works, and its useful from those implementations that cannot or wish not to download the 
entire repository (for example, mobile devices with limited storage available, wishing to 
access a syncthing share).

## Building

The project uses a standard gradle build. After installing gradle, simply run `gradle assemble` to compile, or
`gradle install` to add it to your local maven repository.

## Running

To use the command line client, run `gradle run -Pargs="-h"`. 

## License

All code is licensed under the [MPLv2 License][3].

[1]: https://syncthing.net/
[2]: https://github.com/Nutomic/syncthing-lite
[3]: https://github.com/syncthing/syncthing-android
[4]: LICENSE


