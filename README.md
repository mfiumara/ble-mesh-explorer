# ble-mesh-microservice
A BLE Mesh Microservice for exploring and provisioning a BLE Mesh network using gRPC.

### BLE Mesh
The BLE Mesh service is written in C and is hardware dependent, i.e. it needs to run on a linux machine with an HCI device available. It is implemented in C, using Zephyr Native Posix for its BLE Mesh framework and exposes these API's using googles protobuf. 

