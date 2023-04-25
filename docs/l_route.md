# The routing

Finally, it is time!

If you dare starting to read this section before [the previous layout sections](../l_place/), you've missed the point!
Routing your board is the last step of a sucessful board output, and it should run smoothly **if** you've followed this guide's winding road without skipping a turn.

## The priorities

In the process of setting the board for routing, you should now have a really good idea how each and every power rail and signal should be routed, and in which order. And if it's not the case then you must be missing some key information about the circuit and you need to figure them out before churning through the routes.

Any "high" circuit will likely be the first with traces and shapes.

## The design rule checks

Remember [in the previous step](../l_constraint) how we made sure that the final result goes smoothly to fabrication? Well, it all goes to waste if your design contains a whole lot of DRC errors!

This step should be an integral part of your final layout review process or checklist, make sure all the DRC items are all addressed and do not leave any open item before getting those gerber files out of the door.