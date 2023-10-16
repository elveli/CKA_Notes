# CKA_Notes
My CKA Notes

* https://medium.com/geekculture/my-jq-cheatsheet-34054df5b650
* https://kubernetes.io/docs/reference/kubectl/cheatsheet/
* https://github.com/alijahnas/CKA-practice-exercises
* https://github.com/walidshaari/Kubernetes-Certified-Administrator
* https://github.com/StenlyTU/K8s-training-official
* https://github.com/ramitsurana/awesome-kubernetes
* https://github.com/MohanRamadoss/ckakubernetes-network-policy
* https://github.com/MohanRamadoss/ckakubernetes-network-policy
* https://docs.linuxfoundation.org/tc-docs/certification/tips-cka-and-ckad#resources-allowed-during-exam
* https://github.com/ascode-com/wiki/blob/main/certified-kubernetes-administrator/README.md
* https://editor.networkpolicy.io/?id=Uvdc7jwZhZfY3LpX
* https://gist.github.com/JamieMac96/adf9d3c9fe9aa6cd40a20047efabc9ec
* https://www.youtube.com/watch?v=o321_1TwD8s
* https://www.youtube.com/watch?v=9UqkWcdy140
* https://www.youtube.com/watch?v=Gbnhyu1oGeY
* https://www.youtube.com/watch?v=4THV5o6ntIE&t=580s
* https://www.youtube.com/watch?v=YMxHK7FRlV0
* https://www.youtube.com/watch?v=7wRqtBMS6E0
* https://www.youtube.com/watch?v=8VK9NJ3pObU
* https://www.youtube.com/watch?v=lR1-XfWeDcc

Key areas to focus
tbd

Tools
```
vim
jq
tmux
aliases
yq
```

Tips

```
use / get kubernetes short names
delete pods without waiting
export now='--force --grace-period 0"
k delete pod nginx $now
k delete pod nginx --now=true
export LESS="-RLFi"
alias l='ls -lsrth'
:set autoindent
```

Aliases and functions

```
alias k="kubectl"
alias v="vim"

function ns () {
  kubectl config set-context --current --namespace=$1
}

export drc="--dry-run=client -oyaml"
export drs="--dry-run=server -oyaml"
```
