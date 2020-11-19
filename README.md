[![Build Status](https://travis-ci.org/vinzenz/vsqlite--.png?branch=master)](https://travis-ci.org/vinzenz/vsqlite--)
[![Coverity Scan Build Status](https://scan.coverity.com/projects/1976/badge.svg)](https://scan.coverity.com/projects/1976)

VSQLite++ - A welldesigned and portable SQLite3 Wrapper for C++
(C) 2006-2014 by virtuosic bytes  - vinzenz.feenstra@gmail.com

Author: Vinzenz Feenstra

License: BSD-3

# Website: http://vsqlite.virtuosic-bytes.com

[![Join the chat at https://gitter.im/vinzenz/vsqlite--](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/vinzenz/vsqlite--?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

# Supported Compilers
- g++ 4.x
- MSVC 2005-2013
- Clang 3.x

# Operating Systems
- Linux
- Windows
- Mac OS X

# Dependencies
- Boost Libraries [ http://www.boost.org ] >= 1.33
- libsqlite3


Additional notices:

- Please let me know if you want to suggest features
- Contributions are welcome
- Proposals for Design Improvement are welcome

# Building a new debian package #
Run the following to create a new debian package for a new version:
```
apt install build-essential devscripts fakeroot libboost-system-dev libboost-filesystem-dev
dch --newversion <version>-<build_number>ps0 <message> && dch -r --distribution buster ""
apt build-dep libvsqlitepp3v5 -y
dpkg-buildpackage -rfakeroot-tcp -aarmhf -b -uc -us
```

After running the above commands, the debian package will be created in the
parent direction of this repo.
