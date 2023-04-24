# The validation

The board is here, rejoice!  
Rushing to build your product and ship it? Nope, it's time for validation.

## The documentation

When you are working through the validation of your circuit board, track all items and measurements compared to expected results.
That way, you can keep track of the progress of the validation and leave a trail for issues or improvements to be used in the next revision. Not keeping notes might cost you and you will likely repeat the same design errors or not remember what was wrong with such or such circuit without redoing the full validation.

Once you have identified all the necessary corrections for the next revision, make a checklist and tackle all items one by one by updating your design. This checklist can also be used to track changes requested by other people.

The overhead might hurt your immediate productivity as you are documenting everything, but it will save you precious time in the future and you would be able to deliver the final design more efficiently.

## The sequence

Before tackling head down the validation of a circuit, ask yourself where you should start.
For instance, power unstabilities can cause many headaches to the rest of the circuit so you should ensure nothing is wrong there before moving onto validating a device using that power.

My suggested validation sequence is the following:

- power sources: input, regulators, charging, etc.
- clock sources: crystals, oscillators, etc
- reset sources
- low-speed IO controls
- low-speed interfaces (I2C, UART)
- high-speed interfaces (SPI, I2S, USB, etc)

However, as every board is different, you should build your own sequence.

## The equipment

It might seem obvious, but it is not okay to validate a circuit with the wrong set of equipment and call it a day. Using a multimeter to check the output of a regulator is fine for quick information but it is not for validation. A multimeter does not tell you anything on that regulator's stability while probing the same node with an oscilloscope will show you the full picture.

There are many existing tools, some cheap and some expensive. You should know which circuits you can validate and which you can't with the equipment you have. It is critical to make your team aware in the case that you cannot validate an interface because of the equipment limitation. Being informed, you can make the right decision altogether.

## The specifications

Each circuit should meet a certain set of specifications, which is either following a standard, a datasheet or your own rules. Using your equipment, your goal is to check for any mismatch between the reality and the specifications. Finding a mismatch should automatically trigger a deeper investigation, do not ignore it or leave it for later.