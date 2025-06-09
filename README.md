# pfm - the \[p]ort \[f]orwarding \[m\]anager

NOTE: This is a  hobby project - if you ended up here you were probably looking for
- [python pfm](https://pypi.org/project/pfm/)
- [python port-forward-manager](https://pypi.org/project/port-forward-manager/)

Other things you should check out
- [haproxy](https://www.haproxy.org/)
- [nginx](https://www.nginx.com/)
- [squidman](http://squidman.net/squidman/)

## Getting Started

```sh
git clone git@github.com:andrewflbarnes/pfm ~/.pfm

cat << EOS >> ~/.bashrc
export PFM_HOME="\$HOME/.pfm"
PATH="\$PFM_HOME/bin:\$PATH"
eval "\$(pfm init bash)"
EOS

export PFM_HOME="$HOME/.pfm"
PATH="$PFM_HOME/bin:$PATH"
eval "$(pfm init bash)"
```

## Usage

To see a list of commands just run `pfm` without any arguments.

## Notes

### Ease of use

`pfm` is best used with some kind of "passive" authentication to reduce the need for having to enter credentials
manually on operations.

e.g. using and id key, kerberos or an ssh agent.

### Optional init function caching

The step to `eval "$(pfm init bash)"` is optional and will result in pfm functions getting cached in the shell.

This speeds up execution from the shell and is a proof of concept which may be useful for other
tooling like jenv which has prompt command interceptors.

The intention is that all features of pfm sould work without this being necessary.
