 # circuit explenation 
<img width="1386" height="763" alt="image" src="https://github.com/user-attachments/assets/92acb776-620f-4e1e-ba3e-62a0b0e64e15" />
----------------------------------------------------------------------------------------------------------------------------------------
<img width="1289" height="500" alt="image" src="https://github.com/user-attachments/assets/e5ffb324-af65-499b-9872-8de600953f77" />
<img width="1259" height="352" alt="image" src="https://github.com/user-attachments/assets/830054c1-61db-43fc-b4b8-8a68b3bad7d9" />

Now the input circuitry and output circuitry,   the input and output capasitors, the datasheet demands ceramic capasitors with a dielectricum of X7R or better.
Why ceramic capacitors you may ask? because there ESR(equivalent series resitance) is low. which in turn means  lower ripel , control loop is stabel, better transient response and the losses are lower.

<img width="1920" height="543" alt="image" src="https://github.com/user-attachments/assets/0938483a-9792-47bc-87ec-3ddcea421c62" />

For the output circuitry we especialy want that to be suuper stable , why you may ask? Let me show you.

<img width="861" height="476" alt="image" src="https://github.com/user-attachments/assets/b752a021-da03-4022-9980-4e703ddd2f6a" />

As you can see from this block diagram of the chip  the feedbac circuitry is connected (via resistors) to the output. So as you can guess and see. 
Any oscilation will upset the comperator which in turn will pass and upset the control circuitry

----------------------------------------------------------------------------------------------------------------------------------
<img width="607" height="779" alt="image" src="https://github.com/user-attachments/assets/698279ea-bc27-4b47-8393-5dbcf1813ebc" />
Now we will explain the controll pins a bit.
The first pin we 

---------------------------------------------------------------------------------------------------------------------------------------
<img width="1086" height="307" alt="image" src="https://github.com/user-attachments/assets/bde3d319-19b2-42d1-a2b8-02bdc089ebce" />
----------------------------------------

 # schematic details  
