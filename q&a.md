
<img width="1386" height="763" alt="image" src="https://github.com/user-attachments/assets/92acb776-620f-4e1e-ba3e-62a0b0e64e15" />
----------------------------------------------------------------------------------------------------------------------------------------

<img width="607" height="779" alt="image" src="https://github.com/user-attachments/assets/698279ea-bc27-4b47-8393-5dbcf1813ebc" />

I included both the possibility to have a power good led OR the possibility to facilitate power sequencing by including the relevant components but to DNP them.
I also added he possibility to enable the uvlo by addind the voltage devider , the upper resistor is a 0 ohm jumper and the bottom part is DNP.
I did this just because ( and especialy in the early stage of development ) to have more wigle room so to speak. With that i mean  board cost money and to make and chip them it takes a lot of time.
So by addind the footprints for the optional features , it saves me a lot of time and money, the procudtion boards can then be adapted to the findings of the proto.
----------------------------------------------------------------------------------------------------------------------------------------
<img width="1289" height="500" alt="image" src="https://github.com/user-attachments/assets/e5ffb324-af65-499b-9872-8de600953f77" />
<img width="1259" height="352" alt="image" src="https://github.com/user-attachments/assets/830054c1-61db-43fc-b4b8-8a68b3bad7d9" />

Now the input circuitry , here you can note a couple of things. First of all the input capasitors, the datasheet demands ceramic capasitors with a dielectricum of X7R.
Why ceramic capacitors you may ask? because there ESR(equivalent series resitance) is low. which in turn means  lower ripel , control loop is stabel, better transient response and the losses are lower
<img width="1920" height="543" alt="image" src="https://github.com/user-attachments/assets/0938483a-9792-47bc-87ec-3ddcea421c62" />

