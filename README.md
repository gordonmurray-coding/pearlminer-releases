# Pearlminer

**pearlminer**, a Pearlhash (PRL) GPU miner for NVIDIA
RTX 30/40 series cards. 1% dev fee.

## HiveOS

Flight sheet: miner **Custom**, installation URL = the `pearlminer-<version>.tar.gz`
asset of the latest release, miner name `pearlminer`, algo `pearlhash`, wallet template
`%WAL%.%WORKER_NAME%`, pool `us.pearl.herominers.com:1200` (or your pool's host:port).
No extra config is needed: matrix sizes are chosen per card from its VRAM. HiveOS applies
overclocks itself.

## Linux

`pearlminer-<version>-linux-x86_64` needs only the NVIDIA driver (525+) and glibc 2.34+
(Ubuntu 22.04 or newer):

```
./pearlminer --pool us.pearl.herominers.com:1200 --wallet <PRL address> --worker <name>
```

`--show-profile` prints what each GPU will use; `--help` lists tuning flags.
