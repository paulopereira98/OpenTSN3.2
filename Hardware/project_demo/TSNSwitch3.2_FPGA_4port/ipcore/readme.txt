The quartus version used in the TSN switch example project is Quartus Prime Standard Edition 19.1, the FPGA model used is Intel Arria10:10AX048H2F34E2SG, and a total of 15 ip core files are used in the hardware logic source code (including core code, device-related code and interface-related code). , when building the TSN switch example project, users can generate corresponding IP cores according to the following IP core configuration parameter description information, and place all IP core generated files (including QSYS files) in the current path.
The IP core configuration parameter description information is as follows:
(1) IP core: altera_iopll
    ipcore_name:clk125M_50M125M
    Device Family: Arria 10
    Component: 10AX048H2F34E2SG
    Speed ​​Grade:2
    Reference Clock Frequency : 125.0 MHz
    Enable locked output port : selected
    Compensation Mode : direct
    Number Of Clocks : 2
    Clock Name of outclk0 : clk_50M
    Desired Frequency of outclk0 : 50.0 MHz
    Phase Shift Units of outclk0 : ps
    Desired Phase Shift of outclk0 : 0.0
    Desired Duty Cycle of outclk0 : 50.0%
    Clock Name of outclk1 : clk_125M
    Desired Frequency of outclk0 : 125.0 MHz
    Phase Shift Units of outclk0 : ps
    Desired Phase Shift of outclk0 : 0.0
    Desired Duty Cycle of outclk0 : 50.0%
    PLL Bandwidth Preset : Low
    Others:default

(2) IP core: altera_eth_tse (after generating the three-speed Ethernet IP core, two files need to be replaced, see ./sgmii_pcs_revise_note for details)
    Ip_core_name: sgmii_pcs_share
    Component: 10AX048H2F34E2SG
    Core variation : 10/100/1000Mb Ethernet MAC with 1000BASE-X/sgmii pcs
    Use internal fifo: deseclect (uncheck Use internal fifo)
    Number of ports : 4
    Transceiver type : LVDS I/O
    PHY ID : 0x00000000
    Others:default

(3) IP core: 2-port RAM
    Ip_core_name: asdprf16x8_rq
    Operation Mode:With one read port and one write port
    Ram_width:8
    Ram_depth: 16
    Clocking method:dual clock:use separate 'read' and 'write' clocks
    Create a 'rden' read enable signal:selected
    Read input aclrs:selected
    Others:default

(4) IP core: 2-port RAM
    Ip_core_name: asdprf16x9_rq
    Operation Mode:With one read port and one write port
    Ram_width:9
    Ram_depth: 16
    Clocking method:dual clock:use separate 'read' and 'write' clocks
    Create a 'rden' read enable signal:selected
    Read input aclrs:selected
    Others:default

(5) IP core: 2-port RAM
    Ip_core_name: sdprf512x9_s
    Operation Mode:With one read port and one write port
    Ram_width:9
    Ram_depth: 512
    Clocking method : Single
    Create a 'rden' read enable signal:selected
    Read input aclrs:selected
    Others:default

(6) IP core: 2-port RAM
    Ip_core_name: suhddpsram1024x8_rq
    Operation Mode:With two read/write ports
    Ram_width:8
    Ram_depth: 1024
    Clocking method : Single
    Create 'rden_a' and 'read_b' read enable signal:selected
    Output aclrs: "q_a port" and "q_b port" are both selected
    Others:default

(7) IP core: 2-port RAM
    Ip_core_name: suhddpsram16384x9_s
    Operation Mode:With two read/write ports
    Ram_width:9
    Ram_depth: 16384
    Clocking method : Single
    Create 'rden_a' and 'read_b' read enable signal:selected
    Output aclrs: "q_a port" and "q_b port" are both selected
    Others:default

(8) IP core: 2-port RAM
    Ip_core_name: suhddpsram65536x134_s
    Operation Mode:With two read/write ports
    Ram_width: 134
    Ram_depth: 65536
    Clocking method : Single
    Create 'rden_a' and 'read_b' read enable signal:selected
    Output aclrs: "q_a port" and "q_b port" are both selected
    Others:default

(9) IP core: 2-port RAM
    Ip_core_name: suhddpsram512x4_rq
    Operation Mode:With two read/write ports
    Ram_width: 4
    Ram_depth: 512
    Clocking method : Single
    Create 'rden_a' and 'read_b' read enable signal:selected
    Output aclrs: "q_a port" and "q_b port" are both selected
    Others:default

(10) IP core: FIFO
    Ip_core_name: DCFIFO_10bit_64
    Fifo_width: 10
    Fifo_depth: 64
    Clock for reading and writing the FIFO : synchronize reading and writing to 'rdclk' and 'wrclk', respectively.
    Asynchronous clear: selected
    Read access:Normal synchronous FIFO mode
    Others:default

(11) IP core: FIFO
    Ip_core_name: dcm_fifo9x256
    Fifo_width:9
    Fifo_depth: 256
    Clock for reading and writing the FIFO : synchronize both reading and writing to 'clock'.
    Read access:show_ahead synchronous FIFO mode
    Reset:Asynchronous clear
    Others:default

(12) IP core: FIFO
    Ip_core_name: fifo_35x4
    Fifo_width: 35
    Fifo_depth: 4
    Clock for reading and writing the FIFO : synchronize both reading and writing to 'clock'.
    Read access:show_ahead synchronous FIFO mode
    Reset:Asynchronous clear
    Others:default


(13) IP core: FIFO
    Ip_core_name: fifo_w61d32
    Fifo_width: 61
    Fifo_depth: 32
    Clock for reading and writing the FIFO : synchronize both reading and writing to 'clock'.
    Read access:show_ahead synchronous FIFO mode
    Reset:Asynchronous clear
    Others:default

(14) IP core: FIFO
    Ip_core_name: fifo_w14xd16
    Fifo_width: 14
    Fifo_depth: 16
    Clock for reading and writing the FIFO : synchronize both reading and writing to 'clock'.
    Read access:show_ahead synchronous FIFO mode
    Reset:Asynchronous clear
    Others:default

(15) IP core: 2-port RAM
    Ip_core_name: suhddpsram32x57
    Operation Mode:With two read/write ports
    Ram_width: 57
    Ram_depth: 32
    Clocking method : Single
    Create 'rden_a' and 'read_b' read enable signal:selected
    Output aclrs:"q_a port" and "q_b port" are both selected
    Others:default

