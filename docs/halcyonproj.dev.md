# API Reference

## Packages
- [halcyonproj.dev/v1alpha1](#halcyonprojdevv1alpha1)


## halcyonproj.dev/v1alpha1

Package v1alpha1 contains API Schema definitions for the  v1alpha1 API group

### Resource Types
- [AvailabilityZone](#availabilityzone)
- [DataCenter](#datacenter)
- [FabricClass](#fabricclass)
- [PhysicalCable](#physicalcable)
- [PhysicalCompute](#physicalcompute)
- [PhysicalInterface](#physicalinterface)
- [PhysicalPort](#physicalport)
- [PhysicalSwitch](#physicalswitch)
- [Rack](#rack)
- [RackType](#racktype)
- [Region](#region)



#### AvailabilityZone



AvailabilityZone is the Schema for the availabilityzones API





| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `apiVersion` _string_ | `halcyonproj.dev/v1alpha1` | | |
| `kind` _string_ | `AvailabilityZone` | | |
| `metadata` _[ObjectMeta](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.35/#objectmeta-v1-meta)_ | Refer to Kubernetes API documentation for fields of `metadata`. |  |  |
| `spec` _[AvailabilityZoneSpec](#availabilityzonespec)_ |  |  |  |


#### AvailabilityZoneCondition



AvailabilityZoneCondition defines conditions of the AvailabilityZone



_Appears in:_
- [AvailabilityZoneStatus](#availabilityzonestatus)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `type` _string_ |  |  |  |
| `lastHeartbeatTime` _string_ |  |  |  |
| `lastTransitionTime` _string_ |  |  |  |
| `message` _string_ |  |  |  |
| `reason` _string_ |  |  |  |


#### AvailabilityZoneLocation







_Appears in:_
- [AvailabilityZoneSpec](#availabilityzonespec)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `regionName` _string_ |  |  |  |


#### AvailabilityZoneSpec



AvailabilityZoneSpec defines the desired state of AvailabilityZone



_Appears in:_
- [AvailabilityZone](#availabilityzone)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `location` _[AvailabilityZoneLocation](#availabilityzonelocation)_ |  |  |  |




#### DataCenter



DataCenter is the Schema for the datacenters API





| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `apiVersion` _string_ | `halcyonproj.dev/v1alpha1` | | |
| `kind` _string_ | `DataCenter` | | |
| `metadata` _[ObjectMeta](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.35/#objectmeta-v1-meta)_ | Refer to Kubernetes API documentation for fields of `metadata`. |  |  |
| `spec` _[DataCenterSpec](#datacenterspec)_ |  |  |  |


#### DataCenterCondition



DataCenterCondition defines conditions of the DataCenter



_Appears in:_
- [DataCenterStatus](#datacenterstatus)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `type` _string_ |  |  |  |
| `lastHeartbeatTime` _string_ |  |  |  |
| `lastTransitionTime` _string_ |  |  |  |
| `message` _string_ |  |  |  |
| `reason` _string_ |  |  |  |


#### DataCenterLocation







_Appears in:_
- [DataCenterSpec](#datacenterspec)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `address` _string_ |  |  |  |
| `availabilityZoneName` _string_ |  |  |  |


#### DataCenterSpec



DataCenterSpec defines the desired state of DataCenter



_Appears in:_
- [DataCenter](#datacenter)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `type` _string_ |  |  | Enum: [private colocation] <br /> |
| `provider` _string_ |  |  |  |
| `location` _[DataCenterLocation](#datacenterlocation)_ |  |  |  |




#### FabricClass



FabricClass is the Schema for the fabricclasses API





| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `apiVersion` _string_ | `halcyonproj.dev/v1alpha1` | | |
| `kind` _string_ | `FabricClass` | | |
| `metadata` _[ObjectMeta](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.35/#objectmeta-v1-meta)_ | Refer to Kubernetes API documentation for fields of `metadata`. |  |  |
| `spec` _[FabricClassSpec](#fabricclassspec)_ |  |  |  |


#### FabricClassConfiguration







_Appears in:_
- [FabricClassSpec](#fabricclassspec)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `secretRef` _[FabricClassConfigurationSecretRef](#fabricclassconfigurationsecretref)_ |  |  |  |


#### FabricClassConfigurationSecretRef







_Appears in:_
- [FabricClassConfiguration](#fabricclassconfiguration)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `name` _string_ |  |  |  |


#### FabricClassSpec



FabricClassSpec defines the desired state of FabricClass



_Appears in:_
- [FabricClass](#fabricclass)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `configurationFrom` _[FabricClassConfiguration](#fabricclassconfiguration)_ |  |  |  |




#### PhysicalCable



PhysicalCable is the Schema for the physicalcables API





| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `apiVersion` _string_ | `halcyonproj.dev/v1alpha1` | | |
| `kind` _string_ | `PhysicalCable` | | |
| `metadata` _[ObjectMeta](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.35/#objectmeta-v1-meta)_ | Refer to Kubernetes API documentation for fields of `metadata`. |  |  |
| `spec` _[PhysicalCableSpec](#physicalcablespec)_ |  |  |  |


#### PhysicalCableSpec



PhysicalCableSpec defines the desired state of PhysicalCable



_Appears in:_
- [PhysicalCable](#physicalcable)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `sourceInterface` _string_ |  |  |  |
| `targetPort` _string_ |  |  |  |




#### PhysicalCompute



PhysicalCompute is the Schema for the physicalcomputes API





| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `apiVersion` _string_ | `halcyonproj.dev/v1alpha1` | | |
| `kind` _string_ | `PhysicalCompute` | | |
| `metadata` _[ObjectMeta](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.35/#objectmeta-v1-meta)_ | Refer to Kubernetes API documentation for fields of `metadata`. |  |  |
| `spec` _[PhysicalComputeSpec](#physicalcomputespec)_ |  |  |  |


#### PhysicalComputeBMC







_Appears in:_
- [PhysicalComputeSpec](#physicalcomputespec)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `powerState` _string_ |  |  | Enum: [ on off unknown] <br />Optional: \{\} <br /> |
| `connection` _[PhysicalComputeBMCConnection](#physicalcomputebmcconnection)_ |  |  |  |


#### PhysicalComputeBMCConnection







_Appears in:_
- [PhysicalComputeBMC](#physicalcomputebmc)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `type` _string_ |  |  | Enum: [ipmi redfish] <br /> |
| `interfaceName` _string_ |  |  |  |
| `credentialRef` _[PhysicalComputeBMCCredentialRef](#physicalcomputebmccredentialref)_ |  |  |  |


#### PhysicalComputeBMCCredentialRef







_Appears in:_
- [PhysicalComputeBMCConnection](#physicalcomputebmcconnection)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `name` _string_ |  |  |  |


#### PhysicalComputeBMCStatus







_Appears in:_
- [PhysicalComputeStatus](#physicalcomputestatus)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `GUID` _string_ |  |  |  |
| `powerPolicy` _string_ |  |  |  |
| `powerState` _string_ |  |  | Enum: [on off unknown] <br /> |
| `BIOSVersion` _string_ |  |  |  |
| `BIOSBuildDate` _string_ |  |  |  |
| `IPMIVersion` _string_ |  |  |  |
| `firmwareVersion` _string_ |  |  |  |
| `manufacturerID` _string_ |  |  |  |
| `manufacturerName` _string_ |  |  |  |


#### PhysicalComputeBoardStatus







_Appears in:_
- [PhysicalComputeDeviceInfoStatus](#physicalcomputedeviceinfostatus)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `serial` _string_ |  |  |  |
| `partNumber` _string_ |  |  |  |
| `manufacturerName` _string_ |  |  |  |


#### PhysicalComputeChassisStatus







_Appears in:_
- [PhysicalComputeDeviceInfoStatus](#physicalcomputedeviceinfostatus)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `serial` _string_ |  |  |  |
| `partNumber` _string_ |  |  |  |


#### PhysicalComputeConditionStatus







_Appears in:_
- [PhysicalComputeStatus](#physicalcomputestatus)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `type` _string_ |  |  |  |
| `reason` _string_ |  |  |  |
| `message` _string_ |  |  |  |
| `lastTransitionTime` _string_ |  |  | Format: date-time <br /> |


#### PhysicalComputeDeviceInfoStatus







_Appears in:_
- [PhysicalComputeStatus](#physicalcomputestatus)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `board` _[PhysicalComputeBoardStatus](#physicalcomputeboardstatus)_ |  |  |  |
| `chassis` _[PhysicalComputeChassisStatus](#physicalcomputechassisstatus)_ |  |  |  |
| `product` _[PhysicalComputeProductStatus](#physicalcomputeproductstatus)_ |  |  |  |


#### PhysicalComputeInterfaces







_Appears in:_
- [PhysicalComputeSpec](#physicalcomputespec)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `name` _string_ |  |  |  |
| `mac` _string_ |  |  |  |


#### PhysicalComputeLocation







_Appears in:_
- [PhysicalComputeSpec](#physicalcomputespec)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `rackName` _string_ |  |  |  |


#### PhysicalComputeProductStatus







_Appears in:_
- [PhysicalComputeDeviceInfoStatus](#physicalcomputedeviceinfostatus)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `serial` _string_ |  |  |  |
| `partNumber` _string_ |  |  |  |
| `manufacturerName` _string_ |  |  |  |


#### PhysicalComputeResourcesStatus







_Appears in:_
- [PhysicalComputeStatus](#physicalcomputestatus)



#### PhysicalComputeSpec



PhysicalComputeSpec defines the desired state of PhysicalCompute



_Appears in:_
- [PhysicalCompute](#physicalcompute)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `location` _[PhysicalComputeLocation](#physicalcomputelocation)_ |  |  |  |
| `interfaces` _[PhysicalComputeInterfaces](#physicalcomputeinterfaces) array_ |  |  |  |
| `bmc` _[PhysicalComputeBMC](#physicalcomputebmc)_ |  |  |  |
| `UID` _string_ |  |  | Enum: [ on off unknown] <br />Optional: \{\} <br /> |
| `computeClass` _string_ |  |  |  |




#### PhysicalInterface



PhysicalInterface is the Schema for the physicalinterfaces API





| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `apiVersion` _string_ | `halcyonproj.dev/v1alpha1` | | |
| `kind` _string_ | `PhysicalInterface` | | |
| `metadata` _[ObjectMeta](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.35/#objectmeta-v1-meta)_ | Refer to Kubernetes API documentation for fields of `metadata`. |  |  |
| `spec` _[PhysicalInterfaceSpec](#physicalinterfacespec)_ |  |  |  |


#### PhysicalInterfaceDevice







_Appears in:_
- [PhysicalInterfaceSpec](#physicalinterfacespec)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `type` _string_ |  |  |  |
| `refName` _string_ |  |  |  |


#### PhysicalInterfaceSpec



PhysicalInterfaceSpec defines the desired state of PhysicalInterface



_Appears in:_
- [PhysicalInterface](#physicalinterface)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `mac` _string_ |  |  |  |
| `device` _[PhysicalInterfaceDevice](#physicalinterfacedevice)_ |  |  |  |




#### PhysicalPort



PhysicalPort is the Schema for the physicalports API





| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `apiVersion` _string_ | `halcyonproj.dev/v1alpha1` | | |
| `kind` _string_ | `PhysicalPort` | | |
| `metadata` _[ObjectMeta](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.35/#objectmeta-v1-meta)_ | Refer to Kubernetes API documentation for fields of `metadata`. |  |  |
| `spec` _[PhysicalPortSpec](#physicalportspec)_ |  |  |  |


#### PhysicalPortSpec



PhysicalPortSpec defines the desired state of PhysicalPort



_Appears in:_
- [PhysicalPort](#physicalport)





#### PhysicalSwitch



PhysicalSwitch is the Schema for the physicalswitches API





| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `apiVersion` _string_ | `halcyonproj.dev/v1alpha1` | | |
| `kind` _string_ | `PhysicalSwitch` | | |
| `metadata` _[ObjectMeta](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.35/#objectmeta-v1-meta)_ | Refer to Kubernetes API documentation for fields of `metadata`. |  |  |
| `spec` _[PhysicalSwitchSpec](#physicalswitchspec)_ |  |  |  |


#### PhysicalSwitchLocation







_Appears in:_
- [PhysicalSwitchSpec](#physicalswitchspec)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `rackName` _string_ |  |  |  |


#### PhysicalSwitchSpec



PhysicalSwitchSpec defines the desired state of PhysicalSwitch



_Appears in:_
- [PhysicalSwitch](#physicalswitch)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `location` _[PhysicalSwitchLocation](#physicalswitchlocation)_ |  |  |  |
| `identifier` _string_ |  |  |  |
| `fabricClass` _string_ |  |  |  |




#### Rack



Rack is the Schema for the racks API





| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `apiVersion` _string_ | `halcyonproj.dev/v1alpha1` | | |
| `kind` _string_ | `Rack` | | |
| `metadata` _[ObjectMeta](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.35/#objectmeta-v1-meta)_ | Refer to Kubernetes API documentation for fields of `metadata`. |  |  |
| `spec` _[RackSpec](#rackspec)_ |  |  |  |


#### RackLocation







_Appears in:_
- [RackSpec](#rackspec)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `dataCenterName` _string_ |  |  |  |


#### RackSpec



RackSpec defines the desired state of Rack



_Appears in:_
- [Rack](#rack)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `serialNumber` _string_ |  |  |  |
| `rackTypeName` _string_ |  |  |  |
| `location` _[RackLocation](#racklocation)_ |  |  |  |




#### RackType



RackType is the Schema for the racktypes API





| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `apiVersion` _string_ | `halcyonproj.dev/v1alpha1` | | |
| `kind` _string_ | `RackType` | | |
| `metadata` _[ObjectMeta](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.35/#objectmeta-v1-meta)_ | Refer to Kubernetes API documentation for fields of `metadata`. |  |  |
| `spec` _[RackTypeSpec](#racktypespec)_ |  |  |  |


#### RackTypeFormFactor







_Appears in:_
- [RackTypeSpec](#racktypespec)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `enclosure` _string_ |  |  | Enum: [cabinet frame] <br /> |
| `position` _string_ |  |  | Enum: [free-standing mounted] <br /> |
| `posts` _integer_ |  |  | Enum: [2 4] <br /> |


#### RackTypeSpec



RackTypeSpec defines the desired state of RackType



_Appears in:_
- [RackType](#racktype)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `manufacturer` _string_ |  |  |  |
| `model` _string_ |  |  |  |
| `formFactor` _[RackTypeFormFactor](#racktypeformfactor)_ |  |  |  |
| `units` _[RackTypeUnits](#racktypeunits)_ |  |  |  |




#### RackTypeUnits







_Appears in:_
- [RackTypeSpec](#racktypespec)

| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `start` _integer_ |  |  |  |
| `end` _integer_ |  |  |  |
| `order` _string_ |  |  | Enum: [top-down bottom-up] <br /> |


#### Region



Region is the Schema for the regions API





| Field | Description | Default | Validation |
| --- | --- | --- | --- |
| `apiVersion` _string_ | `halcyonproj.dev/v1alpha1` | | |
| `kind` _string_ | `Region` | | |
| `metadata` _[ObjectMeta](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.35/#objectmeta-v1-meta)_ | Refer to Kubernetes API documentation for fields of `metadata`. |  |  |
| `spec` _[RegionSpec](#regionspec)_ |  |  |  |


#### RegionSpec



RegionSpec defines the desired state of Region



_Appears in:_
- [Region](#region)





