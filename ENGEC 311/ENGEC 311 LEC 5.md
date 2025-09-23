Verilog has a way you can define wires i guess? Scalar wires are the default:
> ```
> wire a;
> wire [7:0]b,c,d;
> reg clock;
> ```

For vector declarations it's possible to address bits or parts of vectors:
> ```
> b[3:0];
> ```

There's two types of Verilog: gate level (structural) and spec based (behavioral).
> ```
> module Simple (A, B, C, D, E);
> 	output D, E;
> 	input A, B, C;
> 	wire w1
> 	
> 	and G1 (w1, A, B);
> 	not G2 (E, C);
> 	or  G3 (D, w1, E);
> endmodule
> ```

Numbers can be represented in Verilog this way:
> ```
> 4'b0000
> 3'o7
> 16'hABBA
> ```

Unfortunately data in the hardware takes some time to move around. This can be specified in time units, using a "#" symbol followed by a number. Time units are proportional to a timescale specified before module declaration. It only affects simulation with synthetic gates. Real gates have their own delays.
> ```
> module Simple (A, B, C, D, E);
> ```

