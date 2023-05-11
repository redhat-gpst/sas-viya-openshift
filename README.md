# SAS Viya on Red Hat OpenShift

Example YAML files are provided for the ClusterAutoScaler, MachineAutoScaler and MachineSet definitions for node pool workload placement for SAS Viya on Red Hat OpenShift.

The following table provides the details about the example definition files provided for each of the SAS Viya [Workload Classes](https://documentation.sas.com/doc/en/itopscdc/v_039/dplyml0phy0dkr/p0om33z572ycnan1c1ecfwqntf24.htm#n0jo17lrlk83rsn1vvs2wqmewkt7), based on the [minimum sizing recommendations for OpenShift](https://documentation.sas.com/doc/en/itopscdc/v_039/itopssr/n08i2gqb3vflqxn0zcydkgcood20.htm#p04uz29tbignsin10sk5ld8h6jn0).

|**Workload Class**|**Example MachineSet file**|**Example MachineAutoScaler file**|
| :- | :- | :- |
|<p>CAS workloads (SMP)</p><p>CAS workloads (MPP)</p>|<p>[`cas-smp-machineset.yaml`](https://github.com/redhat-gpst/sas-viya-openshift/blob/main/cas-smp-machineset.yaml)</p><p>[`cas-mpp-machineset.yaml`](https://github.com/redhat-gpst/sas-viya-openshift/blob/main/cas-mpp-machineset.yaml)</p>|<p>[`cas-smp-autoscaler.yaml`](https://github.com/redhat-gpst/sas-viya-openshift/blob/main/cas-spp-autoscaler.yaml)</p><p>[`cas-mpp-autoscaler.yaml`](https://github.com/redhat-gpst/sas-viya-openshift/blob/main/cas-mpp-autoscaler.yaml)</p>|
|Connect workloads|[`connect-machineset.yaml`](https://github.com/redhat-gpst/sas-viya-openshift/blob/main/connect-machineset.yaml)|[`connect-autoscaler.yaml`](https://github.com/redhat-gpst/sas-viya-openshift/blob/main/connect-autoscaler.yaml)|
|Compute workloads|[`compute-machineset.yaml`](https://github.com/redhat-gpst/sas-viya-openshift/blob/main/compute-machineset.yaml)|[`compute-autoscaler.yaml`](https://github.com/redhat-gpst/sas-viya-openshift/blob/main/compute-autoscaler.yaml)|
|Stateful workloads|[`stateful-machineset.yaml`](https://github.com/redhat-gpst/sas-viya-openshift/blob/main/stateful-machineset.yaml)|[`stateful-autoscaler.yaml`](https://github.com/redhat-gpst/sas-viya-openshift/blob/main/stateful-autoscaler.yaml)|
|Stateless workloads|[`stateless-machineset.yaml`](https://github.com/redhat-gpst/sas-viya-openshift/blob/main/stateless-machineset.yaml)|[`stateless-autoscaler.yaml`](https://github.com/redhat-gpst/sas-viya-openshift/blob/main/stateless-autoscaler.yaml)|

