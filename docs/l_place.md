# The layout: placement

If you happen to skip right to routing, you'll encounter a whole world of hurt down the road. Do not be that person.

Here's who you want to be:
- understand your circuit well and how things flow
- recreate this flow in your layout
- deliver an awesomely designed board.

Easy said, super tough in reality. Let's give it a shot!

## The board setup

Congrats on completing your schematics. Eager to start part placement?

Let's run through those checks first.

### The mechanical fit

* Set the size of your board so it fits mechanically in the target case or enclosure.
* Is it single-sided board or can you have components on both sides?
* Are there any height-constrained zones? Define them clearly on the board so you don't encroach those zones.
* Are there any no-component zones? Define them clearly on the board so you don't encroach those zones.

### The connectors

* Sometimes connector placement is non-negociable, keep an eye open for possible improvement to both mechanical assembly and your circuit
* Use the edges of the board to enable easy plug-unplug cycles
* Avoid placing connectors in the mix of other circuits
* If you can, keep it to a minimum number of edges used by connectors as it is easier to work with

## The component and circuit priorities

Not all component and circuit are created equal, they all have different size, requirements and importance on board placement.

Regardless if you have to deal with high-sensitivity, high-voltage, high-frequency or radio-frequency circuits, you must know which comes first and which comes last in the order of priorities.

### The large components

It's unavoidable, after connectors, large components are coming in as it is the best way to map out your board with the different circuits (eg. one large component = one circuit).

Do **not** start placing decoupling capacitors before you are 100% certain that LQFP-100 package is in the right place.

Run a mechanical check, do they all fit right?

### The "high" circuits

Any circuit which you call "high-xyz" gets high priority placement, there is no way around it.
Between "high" circuits there are fights for a spot, and here you have to use your best judgment to see which wins.
If you are unusure or want a second opinion, talk to your peers to see what they think.

### The understanding of where it belongs

I touched on briefly [earlier](../s_circuit/#purposeful-part-placement), good schematics should lead the layout grouping parts that belong together. It is not always simple and there is never enough space on schematics pages. However, both the circuit designer and layout person should know where part be placed on the board. Meaningless part placement will lead to desastrous results and not accomplish the ultimate goal of creating a neatly designed circuit board.

## The review

Done with placement? Check, double-check, triple-check... do whatever it takes so you do not have to move anything later on.
