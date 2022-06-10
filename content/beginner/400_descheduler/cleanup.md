---
title: "Clean Up"
date: 2019-04-09T00:00:00-03:00
weight: 13
draft: false
---

### Cleaning up

To delete the resources used in this chapter

```bash
unset FIRST_NODE_NAME
kubectl delete -f https://raw.githubusercontent.com/kubernetes-sigs/descheduler/master/kubernetes/deployment/deployment.yaml
kubectl delete -f descheduler-configmap.yaml
kubectl delete -f https://raw.githubusercontent.com/kubernetes-sigs/descheduler/master/kubernetes/base/rbac.yaml
kubectl taint nodes --all dedicated=team1:NoSchedule-
kubectl delete -f podlife-nginx.yaml
kubectl delete deployment nginx
```
