# *bsc-snapshots*


*\> [geth-snapshots](#geth-snapshots)*

*\> [erigon-snapshots](#erigon-snapshots)*


## geth-snapshots


> Database uses [geth(v1.1.11)](https://github.com/bnb-chain/bsc/releases/tag/v1.1.11) for sync


### download

<!-- begin_geth -->

!!! from block [19707818](https://bscscan.com/block/19707818)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/geth.19707818.tar.lz4 -o geth.tar.lz4
```


### checksum


!!! db size 549.72 gb, 561.47 gb after decompression
```bash
> openssl sha256 geth.tar.lz4
SHA256(geth.tar.lz4)= a386638d625e60da2e347bd7c11f5a3e94fa73aedd0ec367212a7a08e92674a8
```

<!-- end_geth -->

### uncompress


running a script: _`lz4 -cd geth.tar.lz4 | tar xf -`_


### flags


```bash
--txlookuplimit=0 --diffsync --syncmode=snap
```


## erigon-snapshots


> Database uses [erigon(v2022.07.02)](https://github.com/ledgerwatch/erigon/releases/tag/v2022.07.02) for sync


### download

<!-- begin_erigon -->

!!! from block [19703958](https://bscscan.com/block/19703958)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/erigon.19703958.tar.lz4 -o erigon.tar.lz4
```


### checksum


!!! db size 755.60 gb, 1074.49 gb after decompression
```bash
> openssl sha256 erigon.tar.lz4
SHA256(erigon.tar.lz4)= b1c81b110c937c301d4d598de67bd9c0e1e88319bd9c3c096eac4fa671c95e19
```

<!-- end_erigon -->

### uncompress


running a script: _`lz4 -cd erigon.tar.lz4 | tar xf -`_


### flags


```bash
--chain=bsc --prune= --prune.h.older=5000 --prune.r.older=5000 --prune.t.older=5000 --prune.c.older=5000 --db.pagesize=16k
```
