# The validation

The board is here, rejoice!  
Rushing to build your product and ship it? Nope, it's time for validation.

## The sequence

The recommended validation sequence is the following:

- power: sources, battery charging, regulators (for each IC)
- clock source: crystals, oscillators, etc
- reset source
- heartbeat, GPIO control
- low-speed interfaces (I2C, UART)
- high-speed interfaces (SPI, I2S, USB, etc)

## The findings

When you are working through the validation of your circuit board, track all items and measurements compared to expected results.
That way, you can keep track of the progress of the validation and leave a trail for issues or improvements to be used in the next revision. Not keeping notes might cost you and you will likely repeat the same design errors or not remember what was wrong with such or such circuit without redoing the full validation.

Once you have identified all the necessary corrections for the next revision, make a checklist and tackle all items one by one by updating your design. This checklist can also be used to track changes requested by other people.

The overhead might hurt your immediate productivity as you are documenting everything, but it will save you precious time in the future and you would be able to deliver the final design more efficiently.