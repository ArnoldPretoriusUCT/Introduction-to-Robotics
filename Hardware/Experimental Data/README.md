# UCT MicroUAV Propulsion System – Performance Data
This README provides an overview of the static performance system testing conducted on the MicroUAV propulsion system. The data was collected using a standardised test setup to evaluate thrust response under controlled conditions.

## Test Configuration
The [Propulsion Rig](https://github.com/AltAirCoaxialVariableTiltMRAV/Propulsion-Rig), an open-source platform designed for multirotor propulsion testing, was used to measure the performance of the MicroUAV's propulsion components. The following test was conducted:
### 1. **Single-Rotor Static Bench Test**
- A PWM duty cycle sweep from 10% to 85% was performed to characterise thrust generation across the operating range.
- Measurements recorded:
    - PWM duty cycle (%)
    - Generated thrust (g)
- Test supply voltage: 11.85 V DC
### Components Tested
- **Motor:** [T-Motor F1203 Kv 7000](https://store.tmotor.com/product/f1203-fpv-motor.html)
- **Propeller:** [HQProp T2x2x4 (2-inch, 4-blade)](https://flyingrobot.co/products/hqprop-t2x2x4-propeller)

## Performance Data Files
|Filename|Description|
|---|---|
|`HQProp T2x2X4 … data.csv`|Raw test log at an 80 Hz sampling rate that includes `time [s]`, `thrust [g]`, and `PWM [%]`|
|`HQProp T2x2X4 … plot.png`|Plot of thrust vs. Commanded PWM duty cycle for a quick performance overview|


## Additional Equipment

- **Power Supply:** Aim-TTi QPX1200SP (1200 W DC programmable power supply)
    - Output set to 11.85 V with current limiting enabled