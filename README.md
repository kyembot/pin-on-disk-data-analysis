# Pin on Disc Data Analysis (work in progress)
A Python script that will automate the cleaning of data from a TE67 Pin-on-Disc Tribometer and the generation of Coefficient of Friction and Material Wear plots. 

  * Place the script (pod.py) in the same directory as the folder containing the TSV files generated from the Pin-on-Disc.

  * Sample data generated from the TE67 Pin-on-disc is included. These are the results from testing Injection Molded Polyphenylene Sulfide (PPS) and Polytetrafluorethylene (PTFE) polymer blends with varying PTFE content and under various testing conditions. 

## Situation/Problem:

The TE67 Pin-on-Disc (PoD) is a tribometer that measures the friction and wear displacement of a material (pin) against a countersurface material (disc). It generates raw data in the form of TSV files and contains information such as: Time, Sliding Velocity, Speed, Mass, Total Revolutions, Specimen Temp, Contact Potential, Radius, Friction, Force, Load, Distance travelled by the pin, Displacement in the z direction, and Coefficient of Friction (CoF). 

For the research I am performing, I need to investigate the wear and friction experienced by the material (PPS and PTFE polymer blends) therefore I am only interested in the data for the Distance travelled, Load experienced, Displacement, and Coefficient of Friction.

The usual process to analyze the wear and coefficient of friction from the TE67 PoD is to:

1. Open the TSV file in Excel
2. Manually generate plots of the evolution of the CoF and Displacement over time.
3. Create spreadsheet formulas that will obtain the specific wear rate using the values for the Displacement, Load, and Distance travelled by the pin. 

This process becomes problematic when the test time goes beyond 30 minutes (1800s) as the PoD measures information per second. For composite materials, test time can go up to 24 hours which means the TSV files will contain around 100,000 lines. Also, this process has to be repeated for each trial. 

## Objectives and Status

The aim of this mini-project is to generate a Python script that will:


  * Automatically generate plots of the CoF over time for all trials (DONE!)
  * Automatically generate plots of the Material Displacement over time for all trials (DONE!)
  * Determine the CoF at the steady-state region of the plots generated for each trial (ongoing)
  * Determine the Specific Wear Rate at the steady-state region of the plots generated for each trial (ongoing)



