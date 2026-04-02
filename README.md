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

As you can see from this block diagram of the chip  the feedback circuitry is connected (via resistors) to the output. So as you can guess and see any oscilation will upset the comperator which in turn will pass and upset the control circuitry

----------------------------------------------------------------------------------------------------------------------------------
<img width="607" height="779" alt="image" src="https://github.com/user-attachments/assets/698279ea-bc27-4b47-8393-5dbcf1813ebc" />

Now we will explain the controll pins a bit.
The first pin we encounter is the Enable pin, which we can use in one of three ways/
The first way is to just tie it to the input voltage , when we do this the convertor will start working whenever a input voltage is present.
The next posibility is to connect an external signal to the enable pin , this can be a microcontroller for example or this can be the power good signal of a upstream convertor.
This is done for when powersequencing is needed , an example of power sequencing can be seen below.

<img width="705" height="269" alt="image" src="https://github.com/user-attachments/assets/d3a3bb0a-7185-445d-bfdf-9a643fbe539a" />

The next and last posebility is to add a voltage devider so we enable the UVLO(Under Voltage Lock Out). This will disable the convertor until a certain voltage is reached or disable the convertor if a voltage dips below a treshold.
This is handy when we are using batterys for example 

The next pin will be the Rt pin ,this pin sets the internal oscilator via a resistor. We need to be careful to choose this resistor. The higher the frequency the more emc and efficency  will become a problem BUT the components can be smaller.
The lower the frequency the lower emc will be and the efficency will be higher BUT the components will be bigger 

The next pin is the VCC pin which comes from the external regulator. Now the datasheet mentions multiple times that there shoudn't be any load connected to the VCC pin BUT in the application schematic in the datasheet it show a load (albeit a pull up).
The EVM schematic shows no load even no pullup connected, so for me it is a mistery if you should or should not connect a load to it.

Next pin is the power good pin , this pin is an open drain pin. This pin will indicate if the convertor works as intended or not.
Also this pin can connect to the enable pin of a downstream converter. So to enable power sequencing as mentiond above.

---------------------------------------------------------------------------------------------------------------------------------------

<img width="1086" height="307" alt="image" src="https://github.com/user-attachments/assets/bde3d319-19b2-42d1-a2b8-02bdc089ebce" />

So the final pin is the feedback pin with it's resistor diverder , this voltage divider will set the input voltage at the input of the controll circuit comperator.
The lower resistor is recomended at 10K and the upper can be a calculated value BUT be awere resistors larger than 1M can introduce noise which in turn will upset the controll circuitry.
Also the feedback trace needs to be short and and bee kept away to again reduce noise.

---------------------------------------------------------------------------------------------------------------------------------------

 # schematic details  
 
As you can see in the overview of the schematic I have a couple of DNP components, I think we all have been there we have our boards in our hands but then we realise some feature of the chip isn't brought out.
So after our little cry we have to spend extra money and time on a new board. So with the DNP parts we have already have a footprint there and so we can easly adapt and continue with a smile.
You will also notice I like to work with collors and net names , the reason behind that is realy simple. So I can see in a blink of an eye what net I am dealing with. This both in the layout side and schematic capture side of things.You will also notice formulas, tables and annotations. This is done so that I don't need to scroll trough the data sheet or have it open on the desktop. We all know engineers have limited desktop space.
