# The symbols

The first part of designing a circuit is to draw symbols for all your components, you want them as obvious as possible.

## The right flow

The opposite of obvious is to draw them as their physical form, eg. their actual package on the board.
The circuit is **not** the place for that, the circuit should make anybody understand what it does, not what it looks like physically on the board (that's what the layout is for).

I have seen so many instance of circuit with their microcontroller drawn exactly like their physical package, and those are the worse schematics to read. Do you really want to force everyone to tilt their head left and right to figure out the pin name and what is connected to it?

Instead try to stick to the following rules.

### The pin orientation

This might be a controversial one but honestly it takes me more effort to read with my head tilted left or right so I hate symbol pins oriented vertically, for most cases.
To prevent your reader a headache, use the **horizontal** pin orientation as much as you can.

Here are the (tolerable) exceptions to this rule:

- power and ground ports and pins: their widely adopted representation is vertical
- symbols with no pin names and obvious function: you don't have to read to understand.

### The pin placement

For the pin placement, keep those couple rules in mind:

- place "inputs" on the left of the symbol
- place "outputs" on the right of the symbol.

Follow this order for placing input pins:

- **control inputs** are first, near the left-top corner
- **control interfaces** underneath the control inputs
- **clock inputs** underneath the control interfaces.

For output pins, use the following guidelines:

- Output "power" pins should be placed first, near the right-top corner.
- Microcontroller pins should be grouped by port.
- Dedicated interfaces pins should be grouped together.
- For regulator designs, place the feedback and compensation circuits on the right side (feedback pin should be close to corresponding switching node).
- Always keep placement so that there is a minimum of crisscrossing between all the different outputs.

> Any other rule that you think makes reading of symbols and circuits even easier should be used!

### The mystery box

"What's that box doing?". Ouch.

It might seems obvious to you what's in it but not to your readers, so to avoid this question be sure to draw a simplified version of the circuit inside the component's symbol.
Sometimes it could even be helpful to add the internal block diagram of the part taken from the datasheet so your reader really know what's in it, and the best part is that they don't even have to open the datasheet!

## The footprint

For your own and your coworker sake, always, yes always make sure the new components you add to your library have a footprint associated to them.
I have seen too many times symbols with no footprint because either the designer forgot to add it later on, or simply gave up in the process of using the component. If you think you won't use the component in the end, do not add it or remove it from the library. Nobody likes half-baked libraries.

### The 3D model

That guy too. Makes sure you have one associated to your footprint!

## The right library

This might sound like a silly rule but I have seen many instances of symbols been saved to the wrong library, and if you don't have a global search system in place then it is just simply annoying to either not find the symbol in the correct place or think it doesn't exist, create it from scratch then discover later you did unecessary redundant work...