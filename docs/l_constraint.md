# The constraints

Placement is fixed, only one more step before routing!

Constraining your design is necessary to avoid manufacturing, assembly and functional issues.
It might feel intimidating at first but when the machine is well oiled, you can re-use it every time when using the same manufacturing facilities.

## The PCB manufacturing capabilities

Have you checked that the PCB vendor can drill and plate this via size you intended to use?
Have you checked what is the minimum supported trace width?
Have you checked that they can manufacture the stackup you've setup?

Those are all the common questions you should ask yourself while setting up your board constraints: if they can't make it then you can't use it, as simple as that.

## The signal integrity

Last but not least, do not forget those "high" circuits [we've already placed](../l_place/#the-high-circuits).
They need special consideration, and special consideration you should give them.