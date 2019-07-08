# Example-coding
Example 1

Verilog code for a flip-flop with a negative-edge clock and asynchronous clear.


        module ff_posedge (clk, d, q);
          input clk, d;
          output q;
          reg q;
  
          always @ (posedge clk)
          begin 
              q <= d;
          end
        endmodule
        
 Verilog code for the flip flop with a positive-edge clock and synchronous set.
 
        module ff_syn ( clk, d, s, q);
          input clk, d, s;
          output q;
          reg q;
  
          always @(posedge clk)
            begin
              if(s) 
              q<= 1'b1;
            else
              q<= d;
            end
         endmodule
         
Verilog code for a flip-flop with a negative-edge clock and asynchronous clear.

        module neg_edge_asynchronous (clk, d, clr, q);
          input clk, d, clr;
          output q;
          reg q;
  
          always @(negedge clk or posedge clr)
            begin
              if(clr)
              q <= 1'b0;
              else
              q<= d;
            end
        endmodule
        
