# nix-index [![Build Status](https://travis-ci.org/bennofs/nix-index.svg?branch=master)](https://travis-ci.org/bennofs/nix-index)
## A files database for nixpkgs
**nix-index** is a tool to quickly locate the package providing a certain file in [`nixpkgs`](https://github.com/NixOS/nixpkgs).

###### Demo

```
$ nix-locate 'bin/hello'
hello.out                                        29,488 x /nix/store/bdjyhh70npndlq3rzmggh4f2dzdsj4xy-hello-2.10/bin/hello
linuxPackages_4_4.dpdk.examples               2,022,224 x /nix/store/jlnk3d38zsk0bp02rp9skpqk4vjfijnn-dpdk-16.07.2-4.4.52-examples/bin/helloworld
linuxPackages.dpdk.examples                   2,022,224 x /nix/store/rzx4k0pb58gd1dr9kzwam3vk9r8bfyv1-dpdk-16.07.2-4.9.13-examples/bin/helloworld
linuxPackages_4_10.dpdk.examples              2,022,224 x /nix/store/wya1b0910qidfc9v3i6r9rnbnc9ykkwq-dpdk-16.07.2-4.10.1-examples/bin/helloworld
linuxPackages_grsec_nixos.dpdk.examples       2,022,224 x /nix/store/2wqv94290pa38aclld7sc548a7hnz35k-dpdk-16.07.2-4.9.13-examples/bin/helloworld
camlistore.out                                7,938,952 x /nix/store/xn5ivjdyslxldhm5cb4x0lfz48zf21rl-camlistore-0.9/bin/hello
```
## Installation
To install this tool, simply clone the repo and run `nix-env -if.` to install it into your user environment:

```
$ git clone https://github.com/bennofs/nix-index
$ cd nix-index
$ nix-env -if.
```

## Usage
First, you need to generate an index by running `nix-index`. Then, you can use `nix-locate pattern`. For more information, see `nix-locate --help` and `nix-index --help`.

## Contributing
If you find any missing features that you would like to implement, I'm very happy about any PRs! You can also create an issue first if the feature is more complex so we can discuss possible implementations. 
