# Update script for Rust nightly and ripgrep

Check out the excellent [ripgrep](https://github.com/BurntSushi/ripgrep)

# Dependencies

- [bash_utils.sh](https://github.com/Slaiyer/bash_utils)

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
		[-d <git_dir>]   Specify path to ripgrep git local directory
		[-u <upstream>]  Specify ripgrep upstream, e.g. 'origin/master'
		[-f]             Force ripgrep rebuild
		[-v 0..2]        Control output verbosity
		[-p]             Do not strip executable post build step
```
