# NAME : ANTONY ABISHEK

# REGISTER NUMBER : 212223240009

# JKFLIPFLOP-USING-IF-ELSE

# Aim :

To implement  JK flipflop using verilog and validating their functionality using their functional tables

# Software required :

Quartus prime

# Theory :

# JK flip flop

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/user-attachments/assets/e6eeb997-000d-470e-890a-bc93349b9eeb)

This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/user-attachments/assets/5ea07395-0981-4cb4-b19f-138e6e776f3b)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/user-attachments/assets/775f1b63-9dce-4f3c-afbe-16e6615f295b)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/user-attachments/assets/690c3a83-bbaa-479a-9581-592fad8c346e)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

# Procedure

Step 1: Open Quartus II in your laptop.

Step 2: Write code to implement SR flipflop using verilog and validating their functionality using their functional tables.

Step 3: Run compilation to check for errors.

Step 4: Open waveform output and load input values.

Step 5: Run simulation to get the output.

Step 6: Open in RTL viewers to get RTL diagram output.

# Program :

```
NAME : ANTONY ABISHEK

REGISTER NUMBER : 212223240009

module JKFLIPFLOPUSINGIFELSE(q, qb,j,k,clock,reset);
    input j,k,clock,reset;
    output reg q, qb;
	 
always @ (posedge (clock))

    begin 
        if (!reset)
            begin
               q <= q;
               qb <=qb;
            end   
        
else
    begin
	     if(j==0 && k==0)
		  begin 
		  q<=q;
		  qb<=qb;
		  end
	 else if (j!=k)
	     begin
	     q<=j;
	     qb<=k;
	     end	 
	 else if(j==1 && k==1)
	     begin
	     q<=~q;
	     qb<=~qb;
	     end
    end
end
endmodule
```

# RTL logic for flipflops :

![image](https://github.com/user-attachments/assets/000f8324-2160-4b25-8ec7-b4e676bf5c89)

# Timing diagrams for flipflops :

![image](https://github.com/user-attachments/assets/ccebb3ec-bd0c-400c-9c17-a6020bbafd76)

# Result :

Hence, JK flipflop using verilog and validating their functionality using their functional tables is implemented.
