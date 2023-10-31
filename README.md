# CKA_Notes
My CKA Notes

* https://medium.com/geekculture/my-jq-cheatsheet-34054df5b650
* https://kubernetes.io/docs/reference/kubectl/cheatsheet/
* https://github.com/alijahnas/CKA-practice-exercises (useful)
* https://pmvk.medium.com/tips-to-crack-certified-kubernetes-administrator-cka-exam-c949c7a9bea1 (useful)
* https://medium.com/@san.agarwal10/my-journey-to-pass-ckad-exam-312d24382177 (useful)
* https://kodekloud.com/blog/kubernetes-sidecar-container/ (useful)
* https://www.vmantra.in/strategy-how-to-pass-cka-exam-with-less-stress/
* https://medium.com/bb-tutorials-and-thoughts/practice-enough-with-these-questions-for-the-ckad-exam-2f42d1228552
* https://github.com/stretchcloud/cka-lab-practice
* https://github.com/dgkanatsios/CKAD-exercises
* https://github.com/walidshaari/Kubernetes-Certified-Administrator
* https://github.com/StenlyTU/K8s-training-official (useful)
* https://github.com/ramitsurana/awesome-kubernetes
* https://github.com/dgkanatsios/CKAD-exercises (useful)
* https://github.com/MohanRamadoss/ckakubernetes-network-policy
* https://docs.linuxfoundation.org/tc-docs/certification/tips-cka-and-ckad#resources-allowed-during-exam
* https://github.com/ascode-com/wiki/blob/main/certified-kubernetes-administrator/README.md
* https://editor.networkpolicy.io/?id=Uvdc7jwZhZfY3LpX
* https://www.reddit.com/r/kubernetes/comments/ssxhsd/cleared_my_cka_exam_with_a_score_of_92_here_are_a/
* https://www.linkedin.com/pulse/how-score-over-90-certified-kubernetes-application-exam-jackson/
* https://gist.github.com/JamieMac96/adf9d3c9fe9aa6cd40a20047efabc9ec
  
* https://www.youtube.com/watch?v=o321_1TwD8s
* https://www.youtube.com/watch?v=9UqkWcdy140
* https://www.youtube.com/watch?v=Gbnhyu1oGeY
* https://www.youtube.com/watch?v=4THV5o6ntIE&t=580s
* https://www.youtube.com/watch?v=YMxHK7FRlV0
* https://www.youtube.com/watch?v=7wRqtBMS6E0
* https://www.youtube.com/watch?v=8VK9NJ3pObU
* https://www.youtube.com/watch?v=lR1-XfWeDcc
* https://www.youtube.com/playlist?list=PLpbwBK0ptsswtM6ihzE6ABGpA-b0NaHXU (useful)

* https://ahmet.im/blog/kubectl-aliases/index.html (kubectl aliases)

* https://stackoverflow.com/questions/40686151/kubernetes-pod-gets-recreated-when-deleted

* https://opensource.com/downloads/kubernetes-sysadmin?intcmp=7016000000127cYAAQ (A 53 page pdf guide to Kubernetes for SREs and sysadmins. Useful)
* https://opensource.com/article/22/12/kubernetes-articles
* https://opensource.com/downloads/chaos-engineering-kubernetes
* https://opensource.com/article/21/6/chaos-mesh-kubernetes
* https://opensource.com/article/22/6/kubernetes-networking-fundamentals (useful)
* https://opensource.com/article/21/6/kubernetes-litmus-chaos (useful)
* https://opensource.com/article/22/5/containers-pods-101-ebook
* https://opensource.com/article/22/3/visual-map-kubernetes-deployment

Key areas to focus
```
taints and tolerations
replication controller
liveness probe: used to determine if a container is still running and responding to requests.
readiness probe: when a container is ready to start accepting traffic.
configmap
service discovery
statefulsets
anti affinity
daemonSets
replicasets
```


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

alias bb='k run busyboxtemp-$$ --image busybox:latest --rm -it --restart=Never --command -- '
then use it like this

bb nslookup google.com
bb wget -qO- https://demo:8888
bb sh

Or specify your namespace:

k run busyboxtemp-$$ --image busybox:latest --rm -it --restart=Never -n your_ns --command -- sh
```
