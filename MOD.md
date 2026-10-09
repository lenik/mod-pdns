# mod-pdns (lenik fork of PowerDNS/pdns)

Upstream: https://github.com/PowerDNS/pdns  
Fork: https://github.com/lenik/mod-pdns

## Policy

All PowerDNS **source** changes for the pdns.1 deployment live on this fork
(branch `mod`). Do not patch distro `/usr` trees or vendor copies in-place.

## Current deployment note

pdns.1 currently runs **Debian package** `pdns-server` + `launch=remote` with
`/home/instance/pdns.1/scripts/hybrid-backend.py` (sqlite unique ∪ `zones/tree/inc`
commons). That hybrid script lives in the **instance tree** (`pdns.1`), not in
this auth repo — until/unless it is ported here as a first-class backend module.

When auth C++/backend patches are needed, develop them on `mod` and build from
this fork.
