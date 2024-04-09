# pfm - the \[p]ort \[f]orwarding \[m\]anager

NOTE: This is a constant WIP hobby project - you are probably looking for a _real_ port forwarding manager.

## Getting Started

```sh
git clone git@github.com:andrewflbarnes/pfm ~/.pfm

cat << EOS >> ~/.bashrc
export PFM_HOME="\$HOME/.pfm"
PATH="\$PFM_HOME/libexec:\$PATH"
eval "\$(pfm init -)"
EOS

export PFM_HOME="$HOME/.pfm"
PATH="$PFM_HOME/libexec:$PATH"
eval "$(pfm init -)"
```

## Usage

To see a list of commands just run `pfm` without any arguments.

## Notes


### Optional init function caching

The step to eval pfm init optional and will result in pfm functions getting cached in the shell.

This speeds up execution from the shell and is a proof of concept which may be useful for other
tooling like jenv which has prompt command interceptors.
