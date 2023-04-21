# The most intuitive circuits

Everybody, even you, would hate looking at a circuit at a glimpse and have no clue what it does, right?

## The page

### The size

Let's start with a silly but important topic as there seems to be trend of fitting everything on a tiny page:

- use tabloid (11x17 inches) or A3 size pages but not bigger else it becomes impossible to navigate and print for review
- do **not** use small size pages with 90% circuit coverage else it becomes unreadable as circuits start to overlap and the mind (at least mine) needs to clearly differentiate the different section of the circuit.

### The organization

It is one of the most obvious start to drawing intuitive schematics but nonetheless deserves a reminder.
Leading your reader is uttermostly important as it is like reading a good book, you don't want to start from the end.

Suggestion:

1. Board diagram, revisions and other notes
0. Power circuits
0. Intelligence (eg. microcontroller)
0. Peripherals

### The title (block)

Final page topic, a clear understanding of what that page contains is often relied upon by readers:

- title block should be updated with the a short description of the circuit presented on that page
- that short description can be text added at the top of the page too
- the title block should contain oher useful information like the board revision, the circuit author, the last update date and other information you deemed necessary to clearly inform your readers.

## The purposeful component placement

Each component in the circuit has a place it belongs. Why you said?

Let's take the most simple example: a decoupling capacitor C3510 belonging to U5001.
The layout person (it could be you) will either:

1. not open the schematics and place it wherever they want
0. opens the schematics and take a few minutes to understand its purpose because it is on a complete different page than U5001
0. opens the schematics and immediately understand where it belongs as it is right next to U5001 `VDD` pin.

Note that if option 2. happened a couple of times already, the layout person will stick to 1. for the rest of the layout process resulting in subpar board routing.

So keep it simple for everybody's sake: group circuits by function and keep component of the same circuit together on the same page.

## The net

### The name

I'm begging you: please, please... add a name to **all your nets**.
You will see: it will be a huge relief to you or your layout person, and it will come very handy for constraining your board layout (more on that in the layout section).

That said, the name needs to be obvious so here are some suggestions.

For digital interfaces, use the following convention:

```
<INTERFACE-NAME>_<SOURCE>_TO_<DESTINATION>_<SIGNAL-FUNCTION>
```
For instance:

- SPI_MCU_TO_FLASH_SCK
- UART_CONNECTOR_TO_MCU_TX
- GPIO_MCU_TO_SENSOR_nRESET

For any other net, use the following convention:

```
<DEVICE-NAME>_<SIGNAL-FUNCTION>
```

For instance:

- BUCK_SW_NODE
- ACCEL_I2C_ADDRESS_0

### The type

Most CAD tools will let you choose between different options: a simple label (eg. text on the net), a hierarchical port or a gobal net.
Be certain you know when to use which:

- label: use to inter-connect symbols on the same page
- hierarchical port: use to inter-connect symbols between pages
- global net: avoid at all cost, you want to control the source and destination of that net and the global context can be prone to mistake.

### The power port

This question should never, never come up: which voltage is that rail supposed to be?

Whatever the voltage is, name your power port or label with the voltage value, and avoid `VDD` or `VBAT` or `VIN` at all cost.
My preferred method is to separate the decimal part from the main voltage value with the voltage unit `V`, for instance a 1.9V rail would have a port named `1V9` (but naming it `1.9V` is fine too).

## The text

### The disentangling

It is one of the worse thing in a schematics: text overlapping with another text or other elements of the circuit.
Have you ever read a book where there is text on top of text? No? So please, be mindful with your readers: make all text in the schematics easy to read and everybody will be delighted.

And as [previously mentioned](../s_symbol/#the-pin-orientation), keep the text orientation horizontal.

### The part number

Some CAD tools do not export symbol information to PDF, therefore it is very essential to indicate the part number of each symbol on the schematic so that the datasheet can easily be found via copy-pasting to your favorite browser.

### The short description

If the symbol does not indicate clearly its function (even after following [this rule](../s_symbol/#the-mystery-box)), it is STRONGLY recommended to add a note above or below the symbol to give an indication to the reader what is the circuit intended for.

### The designators

Best practice would be to annotate with leading digits being the page number. For instance, if you have 9 pages or less, use the first digit for the page number. If you have 99 pages or less, use the first two first digits for the page number. If you have 100 pages or more, I am not sure how it is even possible!

This is an optional rule but you should strongly consider it as it can be quite useful for large schematics.
