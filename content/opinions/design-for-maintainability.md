+++
title = '2025-08-24: Design for Maintainability'
date = 2025-08-24T20:00:00+02:00
draft = false
[params]
  author = 'Magnus Nordlander'
+++
If you've made a PCB, you've probably seen the acroynym DFM - Design for Manufacturing. DFM is an engineering philosophy that considers manufacturing processes, constraints, and costs during the product design phase to ensure the product can be efficiently and economically produced. By incorporating manufacturing considerations early in the design process, DFM helps reduce production costs, improve quality, minimize waste, and accelerate time-to-market.

Having used the La Marzocco GS3 for about a week, I got to thinking about another DFM - Design for Maintainability.

## Maintainability

What even is maintainability in an espresso machine? I'm not talking about keeping the machine clean, or how to change the group shower screen. While those things absolutely *does* qualify as maintenance and are important, many machines get those right. What I'm talking about is servicing the machine as a technician. 

Now, I'll be the first to admit, I haven't worked on *that* many espresso machines. In fact, I've really only worked on the Rancilio Silvia and the Lelit Bianca. They're nice machines for their respective price points, but they're clearly not meant to be serviced in place. Rather, they're made to send off to a repair center somewhere.

Comparing the Bianca to the GS3, to open up your Bianca, you first need to tip it over onto it's face (removing the tank, and grates as you go), then unscrew the legs and a few more screws (from underneath) the machine. Let's just hope your machine wasn't plumbed, because doing that while your machine is plumbed in is not fun. The GS3 by contrast has easily removable panels. You can easily remove the side panels, the front panels, the rear panel. Easy access.

## Spare parts

I messed up a couple of years ago. I was looking in to why the flow control paddle on my Bianca wasn't working well, so I removed it to inspect and possibly clean the gicleur. For those who don't know, the gicleur on the Bianca is a small brass fitting with threads and a hole. Said and done, I removed the gicleur, and indeed there was some scale build-up. I cleaned it up and went to re-install it. Sadly, I over-tightened the gicleur and it broke. Removing the broken part was a bit of a pain, but I managed to do it without issue.

Of course I needed a new gicleur, so I went online to try to find it. Looking at Lelit's spare part documentation, it turns out that you can't buy just the tiny brass gicleur. Instead, you have to buy an entirely new flow control kit. What could have been a $5 part on its own, only comes in a $300 part kit, with parts I didn't need.

I haven't had to buy any spare parts for the GS3 yet, but I have had a look at the spare parts catalog. Not only are parts almost always available separately, La Marzocco even sells part components to be able to preventatively maintain the parts. If your vacuum breaker valve is malfunctioning, you don't need to buy the full vacuum breaker - you can just buy the maintenance kit and fix your broken vacuum breaker.

Now - La Marzocco is by no means perfect here. Some of their spare parts have *ridiculous* prices, especially the electronics. As an example, the button board for the GS3 is €61. The button board is a 2 layer PCB with 12 push buttons, 6 LEDs, 6 capacitors and an IDC connector. The BOM cost is in the order of $5, and I could literally design a replacement in an hour. Similarly, the €69 display module is an off-the-shelf unit (mine is a Xiamen Ocular GDM1602K, but I believe other equivalent units are used as well) with a small adapter board with an IDC connector and some passives. Now, I have nothing against Xiamen Ocular - from what I can see, their display is perfectly adequate, but I would imagine they're about the same quality as the $1 equivalents on AliExpress. The adapter board is - again - something I could design a replacement for in an hour, and has a BOM cost of about $3. 

## Designing for maintainability

Pricing aside however, easily getting in to the machine, and having parts *available* clearly shows that La Marzocco has designed the machine for maintenance - and that makes sense. Most La Marzocco customers are cafés. If your huge 3 group Linea Classic breaks down, you can't ship your machine back to La Marzocco for them to fix it. You call your espresso tech, and they come out to your café and fix it there. Indeed, instead of waiting for the machine to break down on it's own accord, you schedule a yearly maintenance when the café would be otherwise closed, and you preventativly replace the wear-and-tear components. Not the entire part, mind you, but the wear-and-tear components of the part.

Now, I get that market forces (not to mention prices!) are quite different for a machine which is primarily intended as café equipment, and one that is primarily intended as a home appliance. The typical home user barely gets their things repaired if they can't get it done under warranty - many just throw it on a landfill and buy a new machine. Much less do they get someone to preventatively maintain their machines, and they certainly don't maintain them themselves.

This is of course not a sustainable approach to electronics, and I wish home users would demand better. It's refreshing to find a piece of hardware that is made to be maintained.