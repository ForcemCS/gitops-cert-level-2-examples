Apart from the PreSync, Sync and PostSync phases, ArgoCD also has an optional SyncFail phase that is only activated if the main Sync phase has any errors.

In the case Argo CD will apply/deploy all resources that are marked with the SyncFail annotation. Notice also that a failure in the Sync process will never execute any PostSync resources.

You can use the SyncFail annotations for several scenarios such as

send a slack message about the deployment failure
Revert some resources that need to be reverted after a failure
Cleanup resources that were reserved during the deployment
