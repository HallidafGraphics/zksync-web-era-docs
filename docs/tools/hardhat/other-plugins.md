# Community plugins

The following plugins were created by the community and tested on zkSync Era. Feel free to suggest new plugins by [creating a PR for this page](https://github.com/matter-labs/zksync-web-era-docs/blob/main/docs/tools/hardhat/other-plugins.md).

## Supported plugins

::: tip Example project

Here is [a template project configured with all plugins mentioned below](https://github.com/matter-labs/era-hardhat-with-plugins). You can use it as a starting template for your projects.

:::

### hardhat-deploy

Multiple tasks for advanced deployments.

This plugin was [updated to support zkSync Era](https://github.com/wighawag/hardhat-deploy/pull/437) on version `0.11.26`.

[More information](https://www.npmjs.com/package/hardhat-deploy)

### typechain/hardhat

Automatically generate TypeScript bindings for smart contracts.

[More infomation](https://www.npmjs.com/package/@typechain/hardhat)


### hardhat-contract-sizer

Generates a report of the bytecode size of the contracts in your project.

[More information](https://www.npmjs.com/package/hardhat-contract-sizer)

### hardhat-abi-exporter

Different options to export smart contract ABIs.

[More information](https://www.npmjs.com/package/hardhat-abi-exporter)

### hardhat-gas-reporter

Although this plugin works out of the box, zkSync Era has a [different fee model](../../dev/developer-guides/transactions/fee-model.md) than Ethereum. Users should consider this when analysing the report generated by this plugin.

In addition, make sure to read about [local testing](./testing.md).

[More information](https://www.npmjs.com/package/hardhat-gas-reporter)


## Unsupported plugins

### openzeppelin/hardhat-upgrades

This plugin is currently not supported as it overrides compiler tasks and is incompatible with the zkSync Era compiler. 

:::tip
- Proxy contracts are supported on zkSync Era and you can write proxies manually.
- Only this plugin is not currently supported. 
:::

### nomicfoundation/hardhat-network-helpers

This plugin adds new methods that interact with the Hardhat network used for testing.

However, we do not recommend using the Hardhat network for testing contracts that will be deployed on zkSync Era. We recommend instead using the [local setup to test your contracts](testing.md) as it will give you the same results as our testnet/mainnet.

The additional methods provided by this plugin are not compatible with the zkSync Era local setup.


 