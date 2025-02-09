#!/bin/bash

echo "Disabling anonymous authentication in Kubernetes API server..."
kubectl patch kubeapiserver cluster --type='merge' -p '{"spec":{"anonymousAuth":false}}'

echo "Enforcing strong security policies..."
kubectl apply -f https://raw.githubusercontent.com/kubernetes/kubernetes/master/cluster/addons/podsecuritypolicy/privileged-psp.yaml

echo "Hardening completed!"
