The rtl files in this directory are files related to the number of network interfaces and device-related files of TSNSwitch3.0. This example project is a TSN switch project that instantiates 4 network interfaces. Each file in this directory is described as follows:
1. Documents related to the number of network interfaces
um.v: Mapping logic for each interface. In the TSN Tester 3.0 example project, interface 0 is used to process time synchronization related logic, interface 1 is used to send test packets, and interface 2 is used to receive test packets. Interface 3 is used to receive TSN tester configuration packets, send TSN tester status report packets and test encapsulation packets
tester_3_0_top.v: code related to the number of network interface input processing logic and network interface output processing logic instantiation, instantiate the corresponding number of gmii_adapters according to the number of network interfaces, and call um.v
2. Device related documents
Except um.v, tester_3_0_top.v, other files are device related files.
