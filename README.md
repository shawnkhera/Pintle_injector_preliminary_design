# Pintle_injector_preliminary_design
Preliminary LOX/GCH4 pintle injector design model using NASA CEA. Calculates propellant flow rates, injector pressure drops, velocities, annular gap, momentum ratios, spray angles, and tracing-opening dimensions for 1, 2, and 3 kN operating points.

A Python-based preliminary design tool for a liquid oxygen (LOX) and gaseous methane (GCH4) pintle injector for a liquid rocket engine, with a maximum design thrust of 3 kN at a chamber pressure of 24 bar.

The model uses NASA CEA to estimate combustion performance parameters, including characteristic velocity (C*), thrust coefficient (Cf), specific impulse (Isp), specific heat ratio (gamma), and chamber temperature. These parameters are used to estimate the ideal sea-level nozzle expansion ratio, calculate throat and exit dimensions, and check consistency between the specified mass flow rate and thrust-based engine sizing.

For injector sizing, the model calculates LOX and GCH4 mass flow rates from the prescribed mixture ratio, estimates injector pressure drops and LOX injection velocity, and iteratively determines the methane annular gap while keeping the estimated methane Mach number below a specified limit. It then calculates the required LOX flow area, slot width, blockage factor, and momentum ratios (TMR and EMR) to estimate the resulting spray half-angle and full spray angle.

The model evaluates three operating points—1 kN, 2 kN, and 3 kN—using scaled mass flow rates and preliminary chamber pressures for the lower-thrust conditions. It also estimates the tracing-opening distance using a selected K-value correlation and predefined fluid and flow parameters.

Finally, the script prints the calculated engine and injector parameters and exports the results for all three operating points to pintle_design_results.csv, supporting preliminary injector sizing and comparison across the intended operating range.

Scope: This is a first-order analytical sizing model. Several fluid properties and spray correlations are preliminary assumptions; the results require validation using real-fluid properties, injector-specific correlations, and experimental or higher-fidelity analysis before detailed design.
