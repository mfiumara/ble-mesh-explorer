# ble-mesh-microservice
A BLE Mesh Microservice for exploring and provisioning a BLE Mesh network using gRPC.

### BLE Mesh
The BLE Mesh service is written in C and is hardware dependent, i.e. it needs to run on a linux machine with an HCI device available. It is implemented in C, using Zephyr Native Posix for its BLE Mesh framework and exposes these API's using googles protobuf. 

### Zephyr set-up
```
virtualenv env
source env/bin/activate
pip install -r zephyr/scripts/requirements.txt
west init -l zephyr
west update
```

### Build the application
```
export ZEPHYR_TOOLCHAIN_VARIANT=native
west build -b native_posix
```

### Running the application
Assuming your bluetooth HCI device is hci0, the following line starts the application:
```
./build/zephyr/zephyr.exe --bt-dev=hci0
```