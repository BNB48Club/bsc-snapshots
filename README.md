# *bsc-snapshots*


*\> [geth-snapshots](#geth-snapshots)*

*\> [erigon-snapshots](#erigon-snapshots)*


## geth-snapshots


> Database uses [geth(v1.1.11)](https://github.com/bnb-chain/bsc/releases/tag/v1.1.11) for sync


### download

<!-- begin_geth -->

!!! from block [19010634](https://bscscan.com/block/19010634)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/geth.19010634.tar.lz4 -o geth.tar.lz4
```


### checksum


!!! db size 514.92 gb, 544.18 gb after decompression
```bash
> openssl sha256 geth.tar.lz4
SHA256(geth.tar.lz4)= efaede32fac418a187b8b30b8ae8181fd8b66dd19636adf478de545de6707825
```

<!-- end_geth -->

### uncompress


running a script: _`lz4 -cd geth.tar.lz4 | tar xf -`_


### flags


```bash
--txlookuplimit=0 --diffsync --syncmode=snap
```


## erigon-snapshots


> Database uses [erigon(v2022.06.06)](https://github.com/ledgerwatch/erigon/releases/tag/v2022.06.06) for sync


### download

<!-- begin_erigon -->

!!! from block [19000058](https://bscscan.com/block/19000058)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/erigon.19000058.tar.lz4 -o erigon.tar.lz4
```


### checksum


!!! db size 699.40 gb, 1033.24 gb after decompression
```bash
> openssl sha256 erigon.tar.lz4
SHA256(erigon.tar.lz4)= dc218b8339dc71ea015773ba2d4a65c33178aa31dccae3aacb781ada57aa0561
```

<!-- end_erigon -->

### uncompress


running a script: _`lz4 -cd erigon.tar.lz4 | tar xf -`_


### flags


```bash
--chain=bsc --prune= --prune.h.older=5000 --prune.r.older=5000 --prune.t.older=5000 --prune.c.older=5000 --db.pagesize=16k
```
