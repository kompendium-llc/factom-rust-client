# Factom client test environment

#### Installing command line binaries
```bash
wget https://github.com/FactomProject/distribution/releases/download/v6.1.0/factom-amd64.deb 
dpkg -i factom-amd64.deb
rm factom-amd64.deb
```




#### Starting custom factomd testnet
```bash
factomd -network=CUSTOM -customnet="cargo-test" -exclusive=true
```

##### Commands used creating test environment
```bash

factom-cli importaddress Fs3E9gV6DXsYzf7Fqx1fVBQPQXV695eP3k5XbmHEZVRLkMdD9qCK

factom-cli importaddress Es2r45VdEdf34jBrA2zSeiQQKuH8sP9xzCsSBzLE68pB2KuhjTBn

factom-cli buyec FA2jK2HcLnRdS94dEcU27rF3meoJfpUcZPSinpb7AwQvPRY6RL1Q EC3EAsdwvihEN3DFhGJukpMS4aMPsZvxVvRSqyz5jeEqRVJMDDXx 10000

echo "A test chain" | factom-cli addchain -n "rust api client testing" EC3EAsdwvihEN3DFhGJukpMS4aMPsZvxVvRSqyz5jeEqRVJMDDXx

```