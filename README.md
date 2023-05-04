# SAS Viya on Red Hat OpenShift

Example YAML files are provided for the ClusterAutoScaler, MachineAutoScaler and MachineSet definitions for node pool workload placement for SAS Viya on Red Hat OpenShift.

The following table provides the details about the example definition files provided for each of the SAS Viya [Workload Classes](https://documentation.sas.com/doc/en/itopscdc/v_039/dplyml0phy0dkr/p0om33z572ycnan1c1ecfwqntf24.htm#n0jo17lrlk83rsn1vvs2wqmewkt7), based on the [minimum sizing recommendations for OpenShift](https://documentation.sas.com/doc/en/itopscdc/v_039/itopssr/n08i2gqb3vflqxn0zcydkgcood20.htm#p04uz29tbignsin10sk5ld8h6jn0).

| Workload Class | Example MachineSet file | Example MachineAutoScaler file |
|----------------|-------------------------|--------------------------------|
|CAS workloads (SMP)|cas-smp-machineset.yaml|cas-smp-autoscaler.yaml|
|CAS workloads (MPP)|cas-mpp-machineset.yaml|cas-mpp-autoscaler.yaml|
|Connect workloads|connect-machineset.yaml|connect-autoscaler.yaml|
|Compute workloads|compute-machineset.yaml|compute-autoscaler.yaml|
|Stateful workloads|stateful-machineset.yaml|stateful-autoscaler.yaml|
|Stateless workloads|stateless-machineset.yaml|stateless-autoscaler.yaml|

