The rtl files in this directory are files related to the number of network interfaces and device-related files of TSNSwitch3.2. This example project is a TSN switch project that instantiates 4 network interfaces. Each file in this directory is described as follows:
1. Documents related to the number of network interfaces
network_input_process_top.v: code related to the number of network interface input processing logic instantiations
network_output_process.v: code related to the number of network interface output processing logic instantiations
TSSwitch.v: calls network_input_process_top.v and network_output_process.v
TSSwitch_top.v: call TSSwitch.v and instantiate the corresponding number of gmii_adapters according to the number of network interfaces
2. Device related documents
Except network_input_process_top.v, network_output_process.v, TSSwitch.v, TSSwitch_top.v, other files are device related files.
