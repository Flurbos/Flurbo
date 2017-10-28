Flurbo Core version 0.12.2 is soon available from:

  <https://flurbo.xyz/bin/flurbo-core-0.12.2/>

This is a new minor version release, including ........,
various bugfixes and Client name change.

Please report bugs using the issue tracker at github:

  <https://github.com/flurbo/flurbo/issues>

Upgrading and downgrading
=========================

How to Upgrade
--------------

If you are running an older version, shut it down. Wait until it has completely
shut down (which might take a few minutes for older versions), then run the
installer (on Windows) or just copy over /Applications/Flurbo-Qt (on Mac) or
flurbod/flurbo-qt (on Linux).

Downgrade warning
-----------------

### Downgrade to a version < 0.12.0

Because release 0.12.0 and later will obfuscate the chainstate on every
fresh sync or reindex, the chainstate is not backwards-compatible with
pre-0.12 versions of Flurbo Core or other software.

If you want to downgrade after you have done a reindex with 0.12.0 or later,
you will need to reindex when you first start Flurbo Core version 0.11 or
earlier.

Notable changes
===============

Example item
---------------------------------------

Example text.

0.12.2 Change log
=================
Setup bitcoin-seeder for flurbocore, added correct domains. ( 2 currently, 1 working ).
Change clientname, to easily identify correct nodes in peers list.
- Working on fixing bitcoin nodes connecting -

0.12.1 Change log
=================

Detailed release notes follow. This overview includes changes that affect
behavior, not code moves, refactors and string updates. For convenience in locating
the code changes and accompanying discussion, both the pull request and
git merge commit are mentioned.

### RPC and REST

Asm script outputs replacements for OP_NOP2 and OP_NOP3
-------------------------------------------------------

OP_NOP2 has been renamed to OP_CHECKLOCKTIMEVERIFY by [BIP 
65](https://github.com/flurbo/bips/blob/master/bip-0065.mediawiki)

OP_NOP3 has been renamed to OP_CHECKSEQUENCEVERIFY by [BIP 
112](https://github.com/flurbo/bips/blob/master/bip-0112.mediawiki)

The following outputs are affected by this change:
- RPC `getrawtransaction` (in verbose mode)
- RPC `decoderawtransaction`
- RPC `decodescript`
- REST `/rest/tx/` (JSON format)
- REST `/rest/block/` (JSON format when including extended tx details)
- `flurbo-tx -json`

### Configuration and command-line options

### Block and transaction handling

### P2P protocol and network code

### Validation

### Build system

### Wallet

### GUI

### Tests and QA

### Miscellaneous

Credits
=======

Thanks to everyone who directly contributed to this release:


As well as everyone that helped translating on [Transifex](https://www.transifex.com/projects/p/flurbo/).


