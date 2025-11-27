This research presents a comprehensive investigation into the design, modeling, and real-time
validation of advanced power converter topologies for high-efficiency electric vehicle charging
systems. The work encompasses three interconnected studies: (1) a market-driven survey of
contemporary electric vehicle architectures and competitive landscape analysis, identifying key
trends in fast-charging infrastructure and converter technology adoption; (2) systematic simula-
tion and comparative analysis of industry-standard Totem-Pole Power Factor Correction (PFC)
and LLC resonant converter topologies in MATLAB-Simulink, evaluating performance metrics
including efficiency, transient response, and harmonic distortion across representative operating
conditions; and (3) FPGA-based hardware-in-the-loop (HIL) real-time validation of discrete-
time digital controllers, demonstrating seamless integration between simulation environments
and embedded implementations. The converter platform operates at 7.7 kW output power with
400 V ports, incorporating soft-switching characteristics and galvanic isolation to achieve re-
duced electromagnetic interference. A Z-domain compensator is derived through systematic
discretization of an S-domain reference controller, enabling precision voltage regulation with
fast transient settling and robust operation across dynamic load variations. Experimental HIL
results confirm superior damping and minimal overshoot characteristics of the discrete-time
implementation relative to continuous-time equivalents.
