# Introduction #

Some computation mechanics software uses generalized and self-consistent units. In this approach, the burden is on the user to specify consistent units. Although this approach is elegant and has lots of flexibility, it can also cause confusion when code is used in the real world, especially by students just learning computation mechanics. To avoid such issues, NairnMPM internally uses a fixed set of units and always outputs results in one set of units. There are some options to provide input data in alternate units, but once in the code a single system is used. Sometimes that system is strange. This  wiki page defines the internal units. Anyone working on the code must use these same units when writing code.

# Units #

This list defines the units for key variables used during the calculations

  * `mtime` and `timestep` for times are in seconds.
  * masses are in g.
  * coordinates (material point, nodal point, _etc._) are in mm.
  * velocity are in mm/sec.
  * momenta are g mm/sec
  * forces are g mm/sec<sup>2</sup>, which is µN.
  * stresses are stored as specific stress in units of Pa cm<sup>3</sup>/g or µJ/g. There are archived as Pa or N/m<sup>2</sup>.
  * strains are absolute strains
  * material density (`rho`) is in g/cm<sup>3</sup>