# Pearlminer

**Pearlminer**, a Pearlhash (PRL) GPU miner for NVIDIA
RTX 30/40 series cards. 1% dev fee.

## HiveOS

Flight sheet: miner **Custom**, installation URL = the `pearlminer-<version>.tar.gz`
asset of the latest release, miner name `pearlminer`, algo `pearlhash`, wallet template
`%WAL%.%WORKER_NAME%`, pool `us.pearl.herominers.com:1200` (or your pool's host:port).
No extra config is needed: matrix sizes are chosen per card from its VRAM. HiveOS applies
overclocks itself.

## mmpOS

Miner profile: custom miner, download URL = the `pearlminer-<version>-mmpos.tgz` asset of the
latest release, keep the default arguments (`--coin ... --pool ... --user ...`); append extra
flags such as `--n 524288` if wanted. Stats (per-GPU hashrate, shares) appear on the dashboard
after the miner's first stats line (~30 s after the GPUs are up).

## Windows

`pearlminer-<version>-windows-x86_64.zip`: unzip, edit the wallet and worker in `run.bat`, run it.
Needs only the NVIDIA driver (525+); overclock flags need an Administrator command prompt.

## Linux

`pearlminer-<version>-linux-x86_64` is a portable build: needs only the NVIDIA driver (525+)
and glibc 2.25+ (Ubuntu 18.04 or newer, any mining distro):

```
./pearlminer --pool us.pearl.herominers.com:1200 --wallet <PRL address> --worker <name>
```

`--show-profile` prints what each GPU will use; `--help` lists tuning flags.
