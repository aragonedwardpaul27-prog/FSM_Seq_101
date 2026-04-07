module clk_div(clk_out, clk_led, clk_in);
    input clk_in;
    
    output reg clk_out = 1'b0;
    output reg clk_led = 1'b0;

    
    parameter integer ticksAtHalfSec = 150_000_000;
    reg[24:0] tickCount = 28'b0; 

    always @(posedge clk_in) begin
      
        if(tickCount == (ticksAtHalfSec - 1)) begin 
            clk_out <= ~clk_out;
            clk_led <= ~clk_out;

            tickCount <= 28'b0;
        end 
        else tickCount <= tickCount + 1; 
    end 
endmodule