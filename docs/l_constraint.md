# The constraints

Placement is fixed, only one more step before routing!

Constraining your design is necessary to avoid manufacturing, assembly and functional issues.
It might feel intimidating at first but when the machine is well oiled, you can re-use it every time when using the same manufacturing facilities.

## The PCB manufacturing capabilities

- Have you checked that the PCB vendor can drill and plate this via size you intended to use?
- Have you checked what is the minimum supported trace width?
- Have you checked that they can manufacture the stackup you picked?

Those are all the common questions you should ask yourself while setting up your board constraints: if they can't fabricate it then you can't use it, as simple as that.

Therefore, head over to the PCB vendor's website, find their specs and import them into your board. If you can't find the information, do not assume and contact them to be certain.

## The net classes

Not all CAD tools are built the same for constraining your design, but they should have net classes at the very least.
You should jump on the opportunity to classify your nets, which have already been named accurately [while drawing your circuit](../s_circuit/#the-name).

Creating net classes (eg. categories of nets) leads you to define a set of physical constraints. Once they are set-up, go through all the nets in your circuit and correctly allocate a class to each one.

## The signal integrity

Last but not least, do not forget those "high" circuits [we've already placed](../l_place/#the-high-circuits).
They need special consideration, and special consideration you should give them.

Here's a non-exhaustive, example list of items to constraint:

- trace resistance and thermals
- trace width and target signal impedance
- differential pair intra and inter-spacing
- signal length and matching between clock lanes and data lanes
- component and signal clearance and isolation with other traces.

You should check what is required for your circuit to function properly and build a set of physical constraints.
With constraints in place, the layout person won't be able to deviate from the specified values during routing without getting DRC errors and warnings.