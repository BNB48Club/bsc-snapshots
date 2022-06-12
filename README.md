# *bsc-snapshots*


*\> [geth-snapshots](#geth-snapshots)*

*\> [erigon-snapshots](#erigon-snapshots)*


## geth-snapshots


> Database uses [geth(v1.1.11)](https://github.com/bnb-chain/bsc/releases/tag/v1.1.11) for sync


### download

<!-- begin_geth -->

!!! from block [18607310](https://bscscan.com/block/18607310)
```bash
aria2c -s8 -x8 -k1M https://snapshots.bnb48.club/geth.18607310.tar.gz -o geth.tar.gz
```


### checksum


!!! db size 511.15 gb, 543.88 gb after decompression
```bash
> openssl sha256 geth.tar.gz
SHA256(geth.tar.gz)= a60b3b92a5c86f7e91b30998ae905756730f62664f11d6b966d444d68f4c9945
```

<!-- end_geth -->

### uncompress


running a script: _`pigz -dkc geth.tar.gz | tar xvf -`_


## erigon-snapshots


> Database uses [erigon(v2022.06.01)](https://github.com/ledgerwatch/erigon/releases/tag/v2022.06.01) for sync


### download

<!-- begin_erigon -->

!!! from block [18602663](https://bscscan.com/block/18602663)
```bash
aria2c -s8 -x8 -k1M https://snapshots.bnb48.club/erigon.18602663.tar.gz -o erigon.tar.gz
```


### checksum


!!! db size 748.53 gb, 1803.00 gb after decompression
```bash
> openssl sha256 erigon.tar.gz
SHA256(erigon.tar.gz)= 66ceff3f334eb637fe7278cffb7b93ba458201f581e76b70795ecabf8be3b2ed
```

<!-- end_erigon -->

### uncompress


running a script: _`pigz -dkc erigon.tar.gz | tar xvf -`_


### flags


```bash
--snapshots=false --prune= --prune.h.older=5000 --prune.r.older=5000 --prune.t.older=5000 --prune.c.older=5000
```