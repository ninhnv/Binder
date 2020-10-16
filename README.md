# Binder Communication Architecture
IPC communication Architecture of Android

# The diagram is to show the IPC communication Architecture of Android and their allocation to the different domains
![binder communication architecture](binder_communication_architecture.png)

* Binder
** All AIDL based communication between SystemServices and SystemService↔Apps
*HwBinder
** All HIDL based communication between HALs and HAL↔SystemServices
** Do not create HIDLs for HAL↔HAL communication unless they are also required for HAL↔SystemService
* VndBinder
** All AIDL based communication between HALs and HAL↔VndServices
** VndServices suite as common Services for HAL implementation which is not intended to Surface to the SystemServices