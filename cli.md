Formatting to be checked before publishing

Smesher setup - CLI

Spacemesh is an open-source, common people-oriented project. Our protocol and repositories are publicly available and one can fork and experiment with the Spacemesh code, but to participate in the network and mine coins, it’s necessary to configure and run the node in a specific way. To do so, besides the GUI (Smapp), there are several CLI tools available.

# Preparation 

We highly recommend using the officially released packages, which can be easily found on Github, there are proper resources for different Operating Systems. 

It’s crucial to have OpenCL support on your system - especially Linux Users. You can use the command clinfo -l to check it.

Preferably create a new folder for Spacemesh, which must be outside of $GOPATH.

In the undermentioned examples, we will be using an "*SM*" folder (mkdir SM) in the home directory. It will be macOS version, please remember to amend the command accordingly to your operating system and needs. 

To smesh - mine SMESH coins - you have to run a Spacemesh node- [the go-spacemesh node](https://github.com/spacemeshos/go-spacemesh). 

To have a wallet on which you would like to get the rewards -  use [SMCLI](https://github.com/spacemeshos/smcli). 

To generate the Proof of Space data and participate in the Smeshing process, you can use [the go-spacemesh node](https://github.com/spacemeshos/go-spacemesh) or [POSTCLI tool.](https://github.com/spacemeshos/post/blob/develop/cmd/postcli/README.md)

## Go-spacemesh node

Get the latest [go-spacemesh release from GitHub](https://github.com/spacemeshos/go-spacemesh/releases).

Download the right package, unzip it, and move to a new directory, prepared for your Spacemesh-related tools.

| cd Downloads
unzip macOS.zip
rm -rf macOS.zip
mv ./Downloads/macOS/ ./SM/node
cd SM/node |
| -- |

In the same directory prepare a network config file. Update the config file name accordingly to the resource you will be using. If you use VS Code you can run: 

| code config.testnet-05.json |
| -- |

To have the content of this file, you should always use the officially published resources, you can find them for example on [Twitter](https://twitter.com/teamspacemesh?s=20).

For the Testnet-05, get the content from here: [https://smapp.spacemesh.network/config.testnet-05.json](https://smapp.spacemesh.network/config.testnet-05.json)

Try running a local node to check if everything is going as expected so far.

| ./go-spacemesh --listen [a_multiaddr] --config [configFileLocation] -d [nodeDataFilesPath] |
| -- |

For example, run the following command from the "node" directory we just created (having the testnet config file in the same directory): 

| ./go-spacemesh --listen /ip4/0.0.0.0/tcp/7513 --config ./config.testnet-05.json -d ./sm_data |
| -- |

You might see a prompt regarding the firewall or accepting incoming connections, approve it and wait a bit to check if the node continues to run without any errors. You should see the logs being written continuously. 

## SMCLI

If you need to create a wallet, you can use our GUI - SMAPP, but if you prefer CLI or you need to extract your public key, our recommendation is [SMCLI](https://github.com/spacemeshos/smcli).

To start, get the latest released SMCLI package for your operating system from our GitHub repository: [SMCLI Releases](https://github.com/spacemeshos/smcli/releases). 

Extract the content, for example to the SM directory to have everything in one place. 

Open your terminal, and change the directory to be in the SMCLI folder. Run the smcli tool and create a new wallet file with the following command: 



| ./smcli wallet create |
| -- |

You will be prompted to enter your [BIP39-compatible mnemonics,](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki) but you can also hit enter if you want to have them generated for you. In the following steps, we choose the second option. 



Please read carefully the information you will get. The mnemonics are listed in one row, take your time to save them. It’s crucial to keep them safe, but also correct. Once noted, hit enter/return. 
![image alt text](image_0.png)

The next step set up a password for your wallet. No requirements here, but of course the stronger it will be, the better for your wallet's security. You can technically skip this step, but we highly recommend setting up a strong passphrase. 

While typing the password, be careful not to make any mistakes, you will not see your input, and once you hit enter, the process will be finalized, with no additional "confirm your password" step. 
After this last step, you will find the location of your wallet. 

Copy it to be able to get the public key with the following command: 

| ./smcli wallet read -f /Users/yourusername/.spacemesh/yourwalletfilename.json |
| -- |

Then just insert your password set just a moment ago, and there you go - your public key information is displayed. 


![image alt text](image_1.png)

Once you created your wallet, there was a piece of advice at the end to back up this file immediately. To do so, you can go on and copy the file manually in via finder/file explorer, but its location is by default hidden (…/.spacemesh/…).
So it might be easier to stay in CLI, and just run copy command, paste the directory you just copied, hit space, and then provide a location where you want your file to be copied to:

| cp /Users/yourusername/.spacemesh/yourwalletfilename.json /Users/yourusername/SM/yourwalletfilename.json |
| -- |

# Smeshing 

Now, that you have your go-spacemesh node prepared and a wallet created, you can go ahead and generate the Proof of Space data. For that, you can use the go-spacemesh node or post-cli, a dedicated tool for POST initialization. 

Either way, we will need an empty directory for our POS files. 

Create a directory for your POS data, for example



| mkdir ./SM/POS |
| -- |

## go-spacemesh node

Go to the node directory. You can run the command indicated in the go-spacemesh README, but the basic scenario requires specifying only the chosen POS directory and the coinbase:



| ./go-spacemesh --listen [a_multiaddr] --config [configFileLocation] -d [nodeDataFilesPath] --smeshing-coinbase [coinbase_account] --smeshing-start --smeshing-opts-datadir [dir_for_post_data] |
| -- |

Most probably you will want to set up more than this.

To customize your Smesher, start with 

| ./go-spacemesh -h |
| -- |

Pick the flags related to the settings you want to customize. 

Here are the flags you probably will need the most when it comes to the Smesher configuration: 



| --smeshing-coinbase			string		coinbase account to accumulate rewards
--smeshing-opts-datadir		string		(default "/Users/username/post/data")
--smeshing-opts-maxfilesize	uint		(default 4294967296)
--smeshing-opts-numunits		uint32		(default 4)
--smeshing-opts-provider		int		(default -1) |
| -- |

More details on each flag:


--smeshing-coinbase **string**          coinbase account to accumulate rewards
The coinbase in any valid wallet address, the one you want to get your rewards on. 

It doesn’t have to be an account in your wallet, you don’t have to be logged in to such a wallet.
Currently, smcli does not support all features and therefore we strongly recommend using smapp for wallet operation. You can still create your wallet using smcli and then import it to Smapp.

--smeshing-opts-datadir **string**      (**default** "/Users/username/post/data")

The datadir is the location of your POS data, our recommendation is to use a new, empty directory. 

These two first inputs are mandatory. 

--smeshing-opts-maxfilesize **uint**    (**default** 4294967296)

Maxfilezsie is the maximum size of one POS data file. - your Proof of space data by default will not be stored in one enormous file, you can choose here if you want your POS split into more smaller files or fewer bigger files. The default is 2 Gibibyte file (note, it’s not Gigabyte). You might want to customize this value for your convenience of moving the generated POS data to another machine for example. Please keep in mind your file system restrictions. As an example, if you don’t customize this flag (leave the default 2GiB), and choose to generate the minimum 256 of POS data, you will get it in 128 files. 

--smeshing-opts-numunits **uint32**     (**default** 4)

The *smeshing-opts-numunits* flag allows you to indicate how much disk space you want to allocate for the Proof of Space files. The bigger your POS, the more rewards you will be getting. But remember, that generating this data might take days or even weeks, and then it will have to be read through regularly (once per epoch - so once per two weeks in the Mainnet) to create proof that you do have it. If the sequential reading process and proof generation will not be finalized in a specific timeframe, you will not be eligible to get the rewards in the next epoch. We have a dedicated profiler tool to check the recommended POS data size for your hardware, feel free to check it out.

How to use this flag? Just provide an integer - minimum 4 - indicating how many units you would like to generate. How big is one unit? In the Mainnet it will be 64 Gibibytes. Now let’s do the math to understand it. 

The hard coded minimum 4 of 64 GiB units gives 256 Gibites of POS data as a minimum. If you wanted to create around 1 Tebibyte, you would need to specify 16 with this *numunits* flag. 

--smeshing-opts-provider **int**        (**default** -1)

The *provider* is the processor you would like to use to generate the POS data. By default, it will pick up the fastest one, so in most cases no need to modify this parameter. To be able to use GPUs you need to make sure you have OpenCL support. GPUs are far more efficient than CPUs.

As an example let’s specify the POS params as follows and run this command from the abovementioned "node" directory: 

| ./go-spacemesh --listen /ip4/0.0.0.0/tcp/7513 --config ./config.testnet-05.json -d ./sm_data --smeshing-coinbase stest1qqqqqqz86qq5r5853yvsksnyh376fwhx5758azgyjnl8h --smeshing-start --smeshing-opts-datadir ./SM/POS --smeshing-opts-numunits 8 |
| -- |

Let’s decompose this example for a better understanding:

We keep the values copied from Github for the port and app data directory, it is absolutely ok to use these default values i.e.:

--listen /ip4/0.0.0.0/tcp/7513

-d ./sm_data


 For the config, insert the name of your config file, in our example:
--config ./config.testnet-05.json




The smeshing coinbase is a wallet address, for example

--smeshing-coinbase stest1qqqqqqz86qq5r5853yvsksnyh376fwhx5758azgyjnl8h

The POS files location - in our example we prepared
--smeshing-opts-datadir ./SM/POS

We set 8 as the *numunits*. (8x64=512GiB)

--smeshing-opts-numunits 8


 The flags not set here explicitly will take the default values. 

Once we run such a command from the *"./SM/node"* directory, the go-spacemesh application should start running and creating the data in the ./SM/POS directory.

## POSTCLI

If you wish, you can generate your Proof of Space data using a dedicated tool for that - namely POSTCLI.
Go to the[ POST Releases](https://github.com/spacemeshos/post/releases) and take the latest released package for your operating system. If you get any warnings from your browser regarding the file not commonly downloaded - click keep and once downloaded, unzip it. You can remove the .zip file and move the postcli folder to the Spacemesh node directory (./SM/node in our case).

| cd Downloads
unzip postcli-macos-v0.8.2.zip
rm -rf postcli-macos-v0.8.2.zip
mv ./Downloads/postcli ./SM/node |
| -- |

 Make sure your postcli tool is an executable file, to make it so, change the directory to ./SM/**node** and you can run

| chmod +x postcli |
| -- |

 

Now to check the possible options you can run 

| ./postcli --help |
| -- |

 

There are two parameters that are required to be specified by the User in order to use the postcli tool, namely : 

| -commitmentAtxId   string   commitment atx id, in hex (required) |
| -- |

and 

| -provider		int	compute provider id (required) (default -1) |
| -- |

To get the actual value of commitmentAtxId you can use gRPC API of the node and call ActivationService::Highest(). For example: 



| grpcurl -plaintext 0.0.0.0:10093 spacemesh.v1.ActivationService.Highest |
| -- |

In the first epoch during the genesis phase, it’s safe to use GoldenATX as commitementAtxId

If you happen to have your private key already (it’s the same smesher-id) you can pass the public key as -id argument.

To get the -provider you can use the following command:

| ./postcli -printProviders |
| -- |

Here’s the example of a command assuming all default and minimum values for POS:



| ./postcli -provider=0 -commitmentAtxId=[atxid-here-removed-for-safety] |
| -- |

Analogically to the above-mentioned go-spacemesh flags, you can customize the below parameters: 



| -commitmentAtxId	string	commitment atx id, in hex (required
-datadir	string	filesystem datadir path (default "/Users/username/post/data")
-id	string	miner's id (public key), in hex (generated if not provided)
-labelsPerUnit	uint	the number of labels per unit (default 512)
-maxFileSize	uint	max file size (default 4294967296)
-numUnits	uint	number of units (default 4)
-provider	int	compute provider id (required) (default -1)  |
| -- |

The generated data is tied to the commitementATXid AND id.

You can pause creating this data and continue anytime. If you already moved the files then `postcli` will try to recreate them. Currently, there is no way to start with an offset.

The postcli tool lets you perform some other actions simply by using these flags:

| -genproof		generate proof as a sanity test, after initialization
-printConfig	print the used config and options
-printProviders	print the list of compute providers
-reset		whether to reset the datadir before starting |
| -- |

# How to move POS data between the computers

If at any point you decide to move your fully generated Proof of Space data for some reason, you can very easily do it. You can also generate the POS files on one PC with a powerful GPU and then set up smeshing with this data on another machine, as generating the proofs doesn’t require huge computing power, a CPU will be enough. 

Let’s assume 2 POS directories, *POS1* and *POS2*.

1. While setting up the Proof of Space data generation, note the parameters you are using, you will need them later on.

2. Once you have the data entirely generated in your *POS1 *folder*, *copy **ALL** the files,* *including `*post_metadata.json*` and `*key.bin*`. 

3. Create a new, empty folder (*POS2) *and move all the copied files to this directory*.*

4. To use this POS data you have to run a node and indicate the *POS2* directory as the --smeshing-opts-datadir

5. Make sure that you specify **exactly** the same post parameters as the ones chosen while generating the data. 

6. When setting the provider you can leave it empty, then the CPU will be selected as a fallback device.

7. You might need to install OpenCL ICD on the target smeshing machine too.
