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
