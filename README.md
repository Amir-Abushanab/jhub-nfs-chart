### NFS JupyterHub Helm Chart

This repo was created to mitigate a very peculiar bug involving Rancher and kubeSpawner interpreting ints as strings. Consider it a default deployment for an NFS storage Jupyterhub, based on (v0.7.0) https://github.com/jupyterhub/helm-chart

The default values are set similar to those described here https://zero-to-jupyterhub.readthedocs.io/en/stable/amazon/efs_storage.html

The only other modification is that the network is set to `ClusterIP` - i.e you should add a separate ingress and make sure to generate and set a value for `proxy.secretToken`
