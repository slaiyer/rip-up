# Update script for Rust nightly and ripgrep

Check out the excellent [ripgrep](https://github.com/BurntSushi/ripgrep)

## Overview
- Calls rustup
- Pulls changes from ripgrep upstream
- Builds ripgrep (if required) with SIMD and AVX extensions
- Runs built-in tests
- Strips built executable

## Usage
```
$ rip-up -h
Update toolchain and build ripgrep from source

Usage:
	rip-up
		[-h]           Print this help message
		[-v 0|1|2|3]   Control output verbosity
		[-f]           Force ripgrep rebuild
		[-d git_dir]   Specify path to Git local directory
		[-u upstream]  Specify Git upstream, e.g. 'origin/master'
		[-p]           Do not strip executable post build step
```

## Installation

- Clone with `git clone --recurse-submodules`
- Link top-level `rip-up` script into a directory in `PATH`

## Dependencies

- bash (version 4.4+)
- [bash_utils.sh](https://gitlab.com/slaiyer/bash_utils)
- Rust nightly CLI
    - rustup
    - cargo
- git
- grep
- sed
- expect package
    - unbuffer
- coreutils package
    - env
    - basename
    - md5sum
    - tee
    - chmod
- bsdmainutils package
    - column
- binutils package
    - strip
