## Steps To Run:
* Go to the directory for the strategy you want to run.
* Package the helm chart into a deployable package: 
```console
helm package .
```
* Run the package:
    * For ACI:
    ```console
    helm install spark-on-aci spark-on-aci-1.0.4.tgz
    ```
    * For Azure Spot Instances: 
    ```console
    helm install spark-on-spot-nodes spark-on-spot-nodes-1.0.4.tgz
    ```
* When done, delete the resources by running the following:
    * For ACI:
    ```console
    helm uninstall spark-on-aci
    ```
    * For Azure Spot Instances: 
    ```console
    helm uninstall spark-on-spot-nodes
    ```