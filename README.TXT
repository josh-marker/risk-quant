This repo contains Excel-based FAIR tools and links to data sources to get you started with risk quantification.

FAIR-in-Excel.xlsx is a FAIR tool to approach loss event frequency and loss magnitude, taking inputs in the form of modified beta PERT parameters (minimum, most likely, maximum, lambda). It includes 4 tabs for 4 separate scenarios, as well as another to aggregate the results into a single loss exceedance curve.

FAIR-COMPARISON compares a single scenario using the above approach (which is loss event frequency and loss magnitude) with three distinct approaches
1) modified beta PERT parameters as inputs (minimum, most likely, maximum, lambda) for loss event frequency and loss magnitude
2) triangle distribution as inputs (minimum, most likely, maximum) for loss event frequency and loss magnitude
3) Poisson as input to loss event frequency and lognormal as input to loss magnitude
It compares all three resulting loss exceedance curves.

Monte-Carlo-Math.xlsx is an Excel-based tool which allows the user to quickly visualize and get feedback on simple mathematical operations. By default it includes:
1) a multiplier for up to 3 values (if you want to multiply 2 values, just make the third distribution 1*)
2) an adder for up to 6 values (if you want to add fewer than 6 distributions, just make the ones you don't want to use equal 0*)
3) a comparison operator (greater than) for simulating TCAP vs RS                                                             

All the above use 1,000 simulations.
They use Hubbard Decision Research's Pseudo Random Number Generator (HDR PRNG).

*For modified beta pert parameter inputs, if you get an error, please ensure that MIN =< ML < MAX.
For example, if you're trying to input the value 1 in the multiplier (because you only want to multiply 2 values), I suggest using the values MIN = 1 / ML = 1 / MAX = 1.000000001 to avoid errors.
