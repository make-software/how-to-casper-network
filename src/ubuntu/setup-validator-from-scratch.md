## Install software

### Update package repositories

```
sudo apt update
```

### Install pre-requisites

```
sudo apt install -y dnsutils software-properties-common git
```

The node uses ```dig``` to get external IP for autoconfig during the installation process

### Install helpers

```
sudo apt install jq -y
```

We will use ```jq``` to process JSON responses from API later in the process

### Install OpenSSL 1.1

The recommended OS is `Ubuntu 22.04`, which comes with `OpenSSL 3`, but `casper-node` still depends on `OpenSSL 1.1`. Thus, you need to install it manually before installing `casper-node`:

```bash
cd ~ && curl -f -JLO http://security.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.1_1.1.1f-1ubuntu2_amd64.deb
sudo apt install -y ./libssl1.1_1.1.1f-1ubuntu2_amd64.deb
```

### Remove Previous Versions (Not Needed for Fresh Installations)

If you were running previous versions of the casper-node on this machine, first stop and remove the old versions:

[include remove-casper-node.md]

### Install Casper node

[include install-casper-node.md]
