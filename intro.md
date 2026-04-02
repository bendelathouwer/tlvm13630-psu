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
----------------------------------------------------------------------------------------------------------------------------
<img width="607" height="779" alt="image" src="https://github.com/user-attachments/assets/698279ea-bc27-4b47-8393-5dbcf1813ebc" />

Now we will explore the controll inputs a bit closer. First you will see the enable pin, this can be used in one of three  way's.
The first way is to just tie it high which means that the convertor will start working as soon as the Input voltage is pressent.
The second way is to controll it externaly this could be an other DC/DC convertor ( done for power sequencing ) or an microcontroller for example
The third way is to include a voltage devider, this is done to have finer controll over the UVLO( Under Voltage Lock Out).
This can be especialy handy if you want to disable the convertor if you're input voltage is to low (battery applications)
The next pin we encounter is the Rrt pin. with this pin we can controll the frequency of the convertor . the lower the frequency the higher the efficiency, but bigger components. the higher the smaller the components but the lower the frequency. this also has an effect on EMC. the higher the frequency the higer the noice and vice versa.
The next pin we encounter is the VCC pin , we decouple this to reduce the noise. Now the weird thing is the datasheet is a bit weird on this pin. it mentions multiple times to NOT connect any loads to this pin BUT in the datasheet  schemmatic it is connected to  PG via a pullup. BUT in the evaluation module it isn't, so this is a mistery. 
So the final pin of this side is the Power good pin, this pin is open drain. This pin is used to show for example that the DC/DC convertor is operating whithin its spec. As previously mentiond there is a thing called power sequencing , whith this scheme you connect the power good pin from this DC/DC convertor to the enable pin of an other DC/DC schematic. Which the picture below demonstrates 
<img width="761" height="329" alt="image" src="https://github.com/user-attachments/assets/11741005-251c-42b2-8370-731fc47a71ba" />

---------------------------------------------------------------------------------------------------------------------------------------
<img width="1086" height="307" alt="image" src="https://github.com/user-attachments/assets/bde3d319-19b2-42d1-a2b8-02bdc089ebce" />
----------------------------------------

 # schematic details  
