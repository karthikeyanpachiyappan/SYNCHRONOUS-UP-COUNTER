### SYNCHRONOUS-UP-COUNTER
To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/karthikeyanpachiyappan/SYNCHRONOUS-UP-COUNTER/assets/155143878/47ba8820-dccb-43ba-a932-ef9a20070a7d)



![image](https://github.com/karthikeyanpachiyappan/SYNCHRONOUS-UP-COUNTER/assets/155143878/835bc90b-a483-4f50-89a1-3c40eda52e1c)


Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

1.Initialize the shift register to a known state (e.g., all zeros).

2.Input a bit serially into the shift register.

3.Shift the contents of the register one position to the right (or left).

4.Output the shifted bit from the last stage of the register.

5.Repeat steps 2-4 for each bit you want to input and shift.


**PROGRAM**
```
Developed by : Karthikeyan P
Register no: 212223230102
```
![image](https://github.com/karthikeyanpachiyappan/SYNCHRONOUS-UP-COUNTER/assets/155143878/f9a35df1-9600-436f-a700-491fe5849ef8)




**RTL LOGIC UP COUNTER**
![image](https://github.com/karthikeyanpachiyappan/SYNCHRONOUS-UP-COUNTER/assets/155143878/6ef19ef0-f91d-46df-911a-a56d0832d367)




**TIMING DIAGRAM FOR IP COUNTER**
![image](https://github.com/karthikeyanpachiyappan/SYNCHRONOUS-UP-COUNTER/assets/155143878/a8b02740-ff1a-4994-a6cf-aa6daa26cab4)




**TRUTH TABLE**
![image](https://github.com/karthikeyanpachiyappan/SYNCHRONOUS-UP-COUNTER/assets/155143878/95532bfb-e3fe-473e-a9aa-9da1680c2178)





**RESULTS**  
Hence a 4 bit synchronous up counter is implemented correctly


