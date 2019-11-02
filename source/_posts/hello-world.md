---
title: Hello
tags: blog
---

## code

```verilog
module args_binary #(
parameter IW = 10   ,//in data width 
parameter OW = 1     //out data width
)(
input           clk,
input           rst,
input [IW-1:0]  in,//in data
output[OW-1:0]  out,//out data
//register
input  [IW-1:0]   cfg_threshold
);
reg [OW-1:0]  do_r;
always @(posedge clk ) begin
    if(in>=cfg_threshold)begin
        do_r <= {OW{1'b1}};
    end else begin
        do_r <= {OW{1'b0}};
    end
end
assign out = do_r;
endmodule

```

## picture

![unsplash](https://images.unsplash.com/photo-1548468868-7480c2e846e9?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1052&q=80)
Photo by chuttersnap on Unsplash

![smms](https://i.loli.net/2019/11/02/BEokYd2mlMUfbju.jpg)

## emoji

🌱✨🎨⚡️🚀

<!-- todo -->
