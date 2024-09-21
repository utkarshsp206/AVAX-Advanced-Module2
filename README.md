# Metacrafters AVALANCHE HYPERSDK
The HyperSDK provides the ability to create a custom virtual machine, which offers complete control over a custom blockchain.

## Description

The HyperSDK provides the ability to create a custom virtual machine, which offers complete control over a custom blockchain. With the HyperSDK, you can design a blockchain that perfectly suits your needs, such as creating and transferring tokens or implementing a traditional order book for asset trading. This level of customization provides a powerful tool for businesses and organizations seeking a tailored solution.

By using the HyperSDK, you have full control over the rules and functionality of your chain, allowing you to create a custom blockchain that is tailored to your startup's specific needs. This offers an unparalleled level of control and flexibility, making it a valuable tool for organizations seeking a custom solution.

This level of control allows your startup to create a unique solution that meets the needs of your users and provides a competitive edge in the market.

## About the HyperSDK
Creating custom Virtual Machines (VMs) is one of the most powerful ways to build on Avalanche. HyperSDK is designed to simplify and accelerate custom VM development, making it safer and easier to launch your own optimized blockchain.

By abstracting away common runtime complexities, HyperSDK provides industry-leading performance and empowers builders to focus on customizations that matter to them. For example, an operator can launch an on-chain video game with the flexibility of fine tuning the architecture for better gameplay, knowing that HyperSDK will execute their transactions quickly and efficiently behind-the-scenes.

HyperSDK is structured so that developers can plug-into a lightning fast execution environment without writing massive amounts of code from scratch, reducing the time it takes to build your own blockchain runtime from many months to just a few days.


## Getting Started

After cloning the github, you will want to do the following to get the code running on your computer.

1. Inside your project folder, run go mod tidy to normalize all the dependencies
2. Configure your project constants
    Go to consts/consts.go and add the missing parts.
3. Register the Create_Asset and Mint_Assest actions in registry/registry.go
4. Run your VM locally
4. Make sure Go is on your path, defined on your terminal, if not you can do so by running ```export PATH=$PATH:$(go env GOPATH)/bin```
5. Run ```MODE="run-single" ./scripts/run.sh```
6. Run ```./scripts/build.sh```
7. Load the demo private key included on the project ```./build/token-cli key import demo.pk``` and ```./build/token-cli chain import-anr```
8. Interact with your own HyperChain!
9. To close your Local Avalanche Network run killall avalanche-network-runner

## Changes in consts.go

```
const (
	// TODO: choose a human-readable part for your hyperchain
	HRP = "ups"
	// TODO: choose a name for your hyperchain
	Name = "UTtoken"
	// TODO: choose a token symbol
	Symbol = "UTK"
)
```

## Changes in registry.go

```
    // TODO: register action: actions.CreateAsset
		// TODO: register action: actions.MintAsset
		consts.ActionRegistry.Register(&actions.BurnAsset{}, actions.UnmarshalBurnAsset, false),
		consts.ActionRegistry.Register(&actions.ModifyAsset{}, actions.UnmarshalModifyAsset, false),
```

## Authors
Utkarsh Singh
Chandigarh University - University Institute of Engineering





