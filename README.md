# tag-connect-otii-stlink
<img src="https://github.com/sakalaka8/tag-connect-otii-stlink/blob/master/4_DOC/irnas_logo.png" height="100">

Simple tool to disconnect the programming lines after completion for use with ST-Link broken out fo a discovery board with Otii power analyser and tag connect cable
<img src="https://github.com/sakalaka8/tag-connect-otii-stlink/blob/master/4_DOC/otii_tool_2.jpg" height="500">

## Folder structure
 * folder 1_SCHEMATIC includes Altium schematic files and PDF schematic
 * folder 2_PCB includes Altium PCB file, PDF PCB print and PDF 3D PCB print
 * folder 3_OUTPUT_FILES includes Gerber and NC Drill files, PDF Assembly file and Bill of Material
 * folder 4_DOC includes 3D step model of PCB and photos of device
 * folder 5_ALTIUM_FILES incudes all Altium Designer files (Libraries, Output job, Project document, ...)

## Concept od device
<img src="https://github.com/sakalaka8/tag-connect-otii-stlink/blob/master/4_DOC/Tag_connect_otii_stlink.png" height="500">
User can disconnect the programming lines in Otii environment with two GPO buttons and choose debug UART lines (Otii or STM Nucleo or both). 

## Circuit board features
 * Shield that sits on top of the ST nucleo board programming part broken off: https://jeelabs.org/book/1547a/
 * 2x connector for Tag Connect cable
   * one for RJ style https://www.digikey.com/product-detail/en/microchip-technology/TC2030-MCP-NL/TC2030-MCP-NL-ND/2125388
   * one for IDC style https://www.digikey.com/product-detail/en/tag-connect-llc/TC2050-IDC/TC2050-IDC-ND/2605366
 * 5V signal relays on all connections from programmer to tag-connect, for example https://si.farnell.com/omron/g5v-2-4-5dc/relay-signal-dpdt-30vdc-2a/dp/9949810?st=signal%20relay
 * IDC connector for Otii power analyser
 * Status LED showing what state this is in
 * IDC connector comaptible with ST-LINK v2
 
## Operation
 * All signal lines from programmer to the device can be disconnected with the relay
 * 5V supply from Otii or Nucleo are used for relays (user selectable with 2.54mm header and jumper)
 * UART TX/RX can be connected to Otii or Nucleo (user selectable with 2.54mm header and jumper)
 * Relays are controlled by either Otii GPO or Nucleo 5V being present (user selectable with 2.54mm header and jumper)
 * Separate GPO channel is used for TX/RX relay - sometimes we want this turned on during testing
 * Relays have a bypass option with a solder jumper

## PCB specifications:
 * Device dimensions: 76x70 mm  
 * PCB thickness: 1.6mm <br/>
<img src="https://github.com/sakalaka8/tag-connect-otii-stlink/blob/master/4_DOC/pcb_top.png" height="300">	<img src="https://github.com/sakalaka8/tag-connect-otii-stlink/blob/master/4_DOC/pcb_angle.png" height="300">


## Licensing

Tag connect Otii ST Link hardware with documentation is licensed under [CERN OHL v.1.2. license](https://www.ohwr.org/licenses/cern-ohl/license_versions/v1.2).

What this means is that you can use this hardware and documentation without paying a royalty and knowing that you'll be able to use your version forever. You are also free to make changes but if you share these changes then you have to do so on the same conditions that you enjoy.

IRNAS is name and mark of Institute IRNAS Race. You may use these name and terms only to attribute the appropriate entity as required by the Open Licence referred to above. You may not use them in any other way and in particular you may not use them to imply endorsement or authorization of any hardware that you design, make or sell.