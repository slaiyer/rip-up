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
$ rip_up -h
Usage:
	rip_up
		[-h]             Print this help message
		[-v 0..2]        Control output verbosity
		[-f]             Force ripgrep rebuild
		[-d <git_dir>]   Specify path to ripgrep git local directory
		[-u <upstream>]  Specify ripgrep upstream, e.g. 'origin/master'
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
    - tee
- bsdmainutils package
    - column
- binutils package
    - strip
