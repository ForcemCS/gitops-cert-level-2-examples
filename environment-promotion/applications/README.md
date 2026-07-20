## command
argocd login host:30443 --insecure --username admin --password	  
	  
	  
	  
argocd app create staging \
  --repo https://github.com/ForcemCS/gitops-cert-level-2-examples.git \
  --revision HEAD \
  --path ./environment-promotion/envs/staging \
  --dest-server https://kubernetes.default.svc \
  --dest-namespace staging \
  --project default \
  --sync-policy automated \
  --auto-prune \
  --self-heal \
  --sync-option CreateNamespace=true



