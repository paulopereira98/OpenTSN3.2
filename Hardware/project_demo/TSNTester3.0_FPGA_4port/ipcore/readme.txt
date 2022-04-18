The quartus version used in the TSN tester example project is Quartus Prime Standard Edition 19.1, the FPGA model used is Intel Arria10:10AX048H2F34E2SG, and a total of 10 ip cores are used in the hardware logic source code (including core code, device-related code and interface-related code). When building the TSN tester example project, the user can generate the corresponding IP core according to the following IP core configuration parameter description information, and place the generated files of all IP cores (including the QSYS file) in the current path.
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

(2) IP core: altera_eth_tse (after generating the triple-speed Ethernet IP core, two files need to be replaced, see ./sgmii_pcs_revise_note for details)
    ipcore_name: sgmii_pcs_share
    Core variation : 10/100/1000Mb Ethernet MAC with 1000BASE-X/sgmii pcs
    Component: 10AX048H2F34E2SG
    Use internal fifo: deseclect (uncheck Use internal fifo)
    Number of ports : 4
    Transceiver type : LVDS I/O
    PHY ID : 0x00000000
    Others:default

(3) IP core: 2-port RAM
    ipcore_name: ram_sdport_w128d32
    Operation Mode:With one read port and one write port
    Ram_width: 128
    Ram_depth: 32
    Clocking method : Single
    Create a 'rden' read enable signal:selected
    Others:default

(4) IP core: 2-port RAM
    ipcore_name: ram_sdport_w128d64
    Operation Mode:With one read port and one write port
    Ram_width: 128
    Ram_depth: 64
    Clocking method : Single
    Create a 'rden' read enable signal:selected
    Others:default

(5) IP core: 2-port RAM
    ipcore_name: ram_sdport_separaterwclock_rdaclr_w8d16
    Operation Mode:With one read port and one write port
    Ram_width:8
    Ram_depth: 16
    Clocking method : Single
    Clocking method:dual clock:use separate 'read' and 'write' clocks
    Create a 'rden' read enable signal:selected
    Read input aclrs:selected
    Others:default

(6) IP core: FIFO
    ipcore_name: fifo_w134d128_commonclock_sclr_showahead
    Operation Mode:With two read/write ports
    Ram_width: 134
    Ram_depth: 128
    Clock for reading and writing the FIFO : synchronize both reading and writing to 'clock'.
     Read access:show_ahead synchronous FIFO mode
    Reset: Synchronous clear
    Others:default


(7) IP core: FIFO
    ipcore_name: fifo_w31d4_commonclock_sclr_showahead
    Operation Mode:With two read/write ports
    Ram_width: 31
    Ram_depth: 4
    Clock for reading and writing the FIFO : synchronize both reading and writing to 'clock'.
     Read access:show_ahead synchronous FIFO mode
    Reset: Synchronous clear
    Others:default

(8) IP core: FIFO
    ipcore_name: fifo_w12d4_commonclock_sclr_showahead
    Operation Mode:With two read/write ports
    Ram_width: 12
    Ram_depth: 4
    Clock for reading and writing the FIFO : synchronize both reading and writing to 'clock'.
     Read access:show_ahead synchronous FIFO mode
    Reset: Synchronous clear
    Others:default

(9) IP core: FIFO
    ipcore_name: fifo_w9d16_respectclock_aclr_showahead
    Operation Mode:With two read/write ports
    Ram_width:9
    Ram_depth: 16
    Clock for reading and writing the FIFO : synchronize reading and writing to 'rdclk' and 'wrclk', respectively.
    Asynchronous clear: selected
    Read access:Normal synchronous FIFO mode
    Others:default

(10) IP core: FIFO
    ipcore_name: DCFIFO_10bit_64
    Fifo_width: 10
    Fifo_depth: 64
    Clock for reading and writing the FIFO : synchronize reading and writing to 'rdclk' and 'wrclk', respectively.
    Asynchronous clear: selected
    Read access:Normal synchronous FIFO mode
    Others:default
