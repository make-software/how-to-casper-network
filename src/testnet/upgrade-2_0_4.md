# Upgrade to casper-node v2.0.4

## Introduction and Timing
We are requesting that all Casper Testnet participants stage the upgrade of their nodes to a new version of `casper_node`
immediately, using the instructions below. "Staging an upgrade" is a process in which you tell your node to download
the upgrade files and prepare them, so that they can automatically be applied at the pre-defined activation point.

For this upgrade, to `casper-node v2.0.4`, the activation point is `Era 19267`, which will be approximately around Thursday, September 11, 2025 at 12:46 UTC.

Please make sure you have properly staged the upgrade well ahead of the activation point, so that your node will be upgraded on time.

## Upgrade Staging Instructions

The process to upgrade your node is very straightforward. Log in to your node, and execute the following command:

```shell
sudo -u casper casper-node-util stage_protocols casper-test.conf
```

## Verifying Successful Staging

After you have successfully executed the above command, you can verify that your node is correctly staged with the
upgrade by taking a look at the output of the following command to make sure it has the 
`Next Upgrade: {'activation_point': 19267, 'protocol_version': '2.0.4'}` `status` line:

```shell
casper-node-util watch
```

If you don't see the `Next Upgrade` line here, then your upgrade staging was not executed successfully.

[include ../disclaimer.md]

