Logic could be either positively triggered or negatively triggered.
```
module dlatch(
	input d, 
	input clk, 
	input reset,
	output reg q);
	always@(clk, d) begin
		case({reset, clk})
			(2’b0x): q <= 0;
			(2’b11): q <= d;
		endcase
	end
```

Sync Reset
```
module dff(
	input d, 
	input clk, 
	input reset,
	output reg q);
	always@(clk) begin
		case(reset)
			(0): q <= 0;
			(1): q <= d;
		endcase
	end
```

Async Reset DFF
```
module dff(
	input d, 
	input clk, 
	input reset,
	output reg q);
	always@(posedge clk, negedge reset) begin
		case(reset)
			(0): q <= 0;
			(1): q <= d;
		endcase
	end
```

$A=AX+BX$
$B=A’X$
$y=(A+B)X’$