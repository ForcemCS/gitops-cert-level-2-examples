Sync phases can work in simple scenarios, but sometimes you want more flexibility on resource ordering. What happens for example if you want to run 3 jobs before the main sync phase, but you also want to order them among themselves? Using sync phases is not enough in that scenario, as by default ArgoCD will deploy every resource available in every individual phase.

Argo CD now has a newer method for resource ordering which is called sync waves.

Sync waves are a number you assign in each resource. By default is each resource is assigned to wave 0 but you can add both negative and positive values to different resources.

During a deployment ArgoCD will order all resources from the lowest number to the highest and then deploy them according to that order.
