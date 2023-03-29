# eml
EML stands for Ethercat Master Library, but be aware that this is not a certified EtherCAT product.

# Disclaimer
This library is not guaranteed and not tested to be fully EtherCAT conformant, but it can be used to communicate with certain devices that use EtherCAT protocol at their Data Link Layer.

# Installation instructions

To build and install:

```
# git clone https://github.com/shadow-robot/eml.git
# cd eml
# mkdir build
# cd build
# cmake -DCMAKE_INSTALL_PREFIX:PATH=${HOME} ..
# make
# make install
```
