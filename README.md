# Update script for Rust nightly and ripgrep

Check out the excellent [ripgrep](https://github.com/BurntSushi/ripgrep)

## Overview
- Calls rustup
- Pulls changes from ripgrep upstream
- Rebuilds ripgrep (but only if required) with SIMD and AVX extensions
- Runs built-in tests
- Strips built executable

## Usage
```
$ rip-up -h
Update toolchain and build ripgrep from source

Usage:
	rip-up
		[-h]             Print this help message
		[-v 0..2]        Control output verbosity
		[-f]             Force ripgrep rebuild
		[-d <git_dir>]   Specify path to Git local directory
		[-u <upstream>]  Specify Git upstream, e.g. 'origin/master'
		[-p]             Do not strip executable post build step
```

## Dependencies

- bash (version 4.4+)
- [bash_utils.sh](https://github.com/Slaiyer/bash_utils)
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
- bsdmainutils package
    - column
- binutils package
    - strip
