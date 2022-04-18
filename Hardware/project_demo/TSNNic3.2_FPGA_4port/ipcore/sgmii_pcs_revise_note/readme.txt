sgmii_pcs_share modification instructions
The modification of the sgmii_pcs core is based on the fact that quartus software has its own problems when generating a 4-port IP core. Here, for the convenience of users, the following modification scheme is provided for reference only:
1. Replace and modify the sgmii_pcs_share.v file under the path\...\sgmii_pcs_share\synth
After generating the IP core file according to the parameter configuration, open the \...\sgmii_pcs_share\synth path:
1) Directly replace the sgmii_pcs_share.v file in the path with sgmii_substitute.v;
2) After the replacement, change the file name of sgmii_substitute.v to "sgmii_pcs_share.v";
3) Open the file "sgmii_pcs_share.v" with the modified name, and modify the 10th line to "module sgmii_pcs_share (";
4) Modify line 124 to "sgmii_pcs_share_altera_eth_tse_191_3sjnh4y eth_tse_0 ("

2. File replacement and modification under path\...\sgmii_pcs_share\altera_eth_tse_191\synth
Open \...\sgmii_pcs_share\altera_eth_tse_191\synth path:
1) Replace the sgmii_pcs_share_altera_eth_tse _191_3sjnh4y.v file in the path with the sgmii_eth_substitute.v file;
2) Modify the replaced file name to sgmii_pcs_share_altera_eth_tse_191_3sjnh4y.v,
3) Open the sgmii_pcs_share_altera_eth_tse_191_3sjnh4y.v text with the modified name, and modify the 10th line to "module sgmii_pcs_share_altera_eth_tse_191_3sjnh4y (";
4) Confirm that the 437th line of the text instantiates the sgmii_pcs_share_altera_lvds_191_ecdu3ty.v file pointing to the path \...\sgmii_pcs_share\altera_lvds_191\synth. If it points to an error, please modify it;
5) Confirm that the 449th line of the text instantiates the sgmii_pcs_share_altera_lvds_191_asrzfni.v file that points to the path \...\sgmii_pcs_share\altera_lvds_191\synth. If it points to an error, please modify it;

After the modification is complete, save it.
