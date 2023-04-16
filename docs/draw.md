# Draw the most intuitive circuits

Everybody, even you, would hate looking at a circuit at glimpse and not know what it does.

## Page organization

It is one of the most obvious start to drawing intuitive schematics but nonetheless deserves a reminder.
Leading your reader is uttermostly important as it is like reading a good book, you don't want to start from the end.

Suggestion:

1. Board diagram, revisions and other notes
0. Power circuits
0. Intelligence (eg. microcontroller)
0. Peripherals

## Symbol that flows right

The first part of designing a circuit is to draw symbols for all your components, you want them as obvious as possible.

What is the opposite of obvious is to draw them as their physical form, eg. their actual package on the board.
The circuit is not the place for that, the circuit should make anybody understand what it does, not what it looks like physically on the board (there is the layout file for that).

I have seen so many instance of circuit with their microcontroller drawn exactly like their physical package, those are the worse schematics to read: do you really want to tilt your head left and right to figure what is connected to which pin?

Instead try this:

<place holder for symbol rules>

## Purposeful part placement

Each component in the circuit has a place it belongs. Why you said?

Let's take the most simple example: a decoupling capacitor C3510 belonging to U5001.
The layout person (it could be you) will either:

1. not open the schematics and place it wherever they want
0. opens the schematics and take a few minutes to understand its purpose because it is on a complete different page than U5001
0. opens the schematics and immediately understand where it belongs as it is right next to U5001 `VDD` pin.

Note that if option 2. happened a couple of times already, the layout person will stick to 1. for the rest of the layout process resulting in subpar board routing.
