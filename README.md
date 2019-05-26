# tag-connect-otii-stlink
Simple tool to disconnect the programming lines after completion for use with ST-Link broken out fo a discovery board with Otii power analyser and tag connect cable

## Circuit board requirements
 * Shield that sits on top of the ST nucleo board programming part broken off: https://jeelabs.org/book/1547a/
 * 2x connector for Tag Connect cable
   * one for RJ style https://www.digikey.com/product-detail/en/microchip-technology/TC2030-MCP-NL/TC2030-MCP-NL-ND/2125388
   * one for IDC style https://www.digikey.com/product-detail/en/tag-connect-llc/TC2050-IDC/TC2050-IDC-ND/2605366
 * 5V signal relays on all connections from programmer to tag-connect, for example https://si.farnell.com/omron/g5v-2-4-5dc/relay-signal-dpdt-30vdc-2a/dp/9949810?st=signal%20relay
 * IDC connector for Otii power analyser
 * Status LED showing what state this is in
 
## Operation
 * All signal lines from programmer to the device can be disconnected with the relay
 * 5V supply from Otii or Nucleo are used for relays (user selectable with 2.54mm header and jumper)
 * UART TX/RX can be connected to Otii or Nucleo (user selectable with 2.54mm header and jumper)
 * Relays are controlled by either Otii GPO or Nucleo 5V being present (user selectable with 2.54mm header and jumper)
 * Separate GPO channel is used for TX/RX relay - sometimes we want this turned on during testing
 * Relays have a bypass option with a solder jumper
 
