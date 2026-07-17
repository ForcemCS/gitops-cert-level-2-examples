1. Deploying a single application to many namespaces
使用list

2. Deploying many applications in a single cluster
使用list 生成器来管理应用程序集是个不错的开始方式。不过，如果你管理的应用程序数量较多，那么最好将它们作为独立的文件或文件夹直接存储在 Git 中，而不是将它们硬编码在list。
这样一来，你就可以添加或删除应用程序文件夹，而 ArgoCD 会自动部署或卸载这些应用程序（就像app of app 模式一样）。

3. Deploying a single application to many clusters
ArgoCD 拥有用于遍历所有已连接集群的cluster生成器

向ARGOCD添加外部集群
argocd login host:30443 --insecure --username admin --password WrSdvBzbX9hrL7W6
argocd cluster add default --name cluster-2


4. Deploying many applications in many clusters
在多个集群上部署多个应用程序， 可以使用matrix生成器
