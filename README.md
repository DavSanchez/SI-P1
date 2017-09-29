# Problema 1 - Sistemas Integrados
## Asignación de Puertos
Para acometer el problema propuesto declaramos los puertos a utilizar, comenzando por el nivel externo en el fichero `cip_gpio_rgb_v1_0.v`.

```verilog
module cip_gpio_rgb_v1_0 # (
    // Users to add parameters here
    
    // User parameters ends
    // Do not modify the parameters beyond this line
    
    // Parameters of Axi Slave Bus Interface S00_AXI
    parameter integer C_S00_AXI_DATA_WIDTH = 32,
    parameter integer C_S00_AXI_ADDR_WIDTH = 4
    )
    (
    // Users to add ports here
    input wire [31:0]seg_button,
    output wire [7:0]siete_seg,
    // User ports ends
    // Do not modify the ports beyond this line
    // ...
);
// Instantiation of Axi Bus Interface S00_AXI
cip_gpio_rgb_v1_0_S00_AXI # (
    .C_S_AXI_DATA_WIDTH(C_S00_AXI_DATA_WIDTH),
    .C_S_AXI_ADDR_WIDTH(C_S00_AXI_ADDR_WIDTH)
    ) cip_gpio_rgb_v1_0_S00_AXI_inst (
    // Users to add ports here
    .SEG_BUTTON(seg_button),
    .SIETE_SEG(siete_seg),
    // User ports ends
    
    //...
);
```

## Lógica de Funciones
A continuación declaramos la lógica que incorporarán nuestras funciones para realizar el cometido deseado.

