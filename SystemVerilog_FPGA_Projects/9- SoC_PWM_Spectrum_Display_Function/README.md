# SoC_PWM_Spectrum_Display_Function - Saif Alomari

About FPGA-based SoC:

A “high-end” embedded system usually has a processor and simple I/O peripherals to perform general user interface and housekeeping tasks and special hardware accelerators to handle computation-intensive operations. These components can be integrated into a single integrated circuit, commonly referred to as an SoC (system on a chip). As the capacity of FPGA devices continues to grow, the same design methodology can be realized in an FPGA chip. Instead of just realizing the system functionalities through customized software, we can incorporate customized hardware into the embedded system as well. The FPGA technology allows us to tailor the processor, select only the needed I/O peripherals, create a custom I/O interface, and develop specialized hardware accelerators for computation-intensive tasks.

The FPro system is composed of those major parts shown in the diagram down below:
- Processor module: The processor module consists of a processor, a memory controller core, and RAM. It is the part that is constructed from the vendors’ IP cores.
- FPro bridge and FPro bus: The processor needs to communicate with other cores. This is done by a bus or interconnect structure specified in the vendor’s IP platform. The modern interconnect is designed to accommodate a wide variety of communication and data transfer needs and involves complex protocols.
- MMIO (memory-mapped I/O) subsystem: The MMIO subsystem provides a framework to accommodate memory-mapped general-purpose and special I/O peripherals as well as hardware accelerators.

The Sampler Diagram (Made by HDL): 

<img src='./images/sampler_system.jpg' width='800'>


# Application Level: 

A rainbow-like spectrum is shown in the figure below. The spectrum can be generated by varying the intensity of the red, green, and blue inputs of the tricolor LEDs. A rainbow light uses the potentiometer and XADC core as the input to specify the desired color on a tricolor LED. 

The x-axis shows the voltage value as read by the XADC core, and the value is displayed on the seven-segment display using the LED-MUX core

<img src='./images/spectrum_display.png' width='500'>



Wiring Diagram (from the potentiometer to the ADC pins):

<img src='./images/wiring_diagram.jpg' width='500'>
