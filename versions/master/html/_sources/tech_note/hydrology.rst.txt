.. _rst_Hydrology:

Hydrology
============

The model parameterizes interception, throughfall, canopy drip, snow
accumulation and melt, water transfer between snow layers, infiltration,
evaporation, surface runoff, sub-surface drainage, redistribution within
the soil column, and groundwater discharge and recharge to simulate
changes in canopy water :math:`\Delta W_{can,\,liq}` , canopy snow water
:math:`\Delta W_{can,\,sno}` surface water :math:`\Delta W_{sfc}` ,
snow water :math:`\Delta W_{sno}` , soil water
:math:`\Delta w_{liq,\, i}` , and soil ice :math:`\Delta w_{ice,\, i}` ,
and water in the unconfined aquifer :math:`\Delta W_{a}`  (all in kg
m\ :sup:`-2` or mm of H\ :sub:`2`\ O).

The total water balance of the system is

.. math::
   :label: 7.1

   \begin{array}{l} {\Delta W_{can,\,liq} +\Delta W_{can,\,sno} +\Delta W_{sfc} +\Delta W_{sno} +} \\ {\sum _{i=1}^{N_{levsoi} }\left(\Delta w_{liq,\, i} +\Delta w_{ice,\, i} \right)+\Delta W_{a} =\left(\begin{array}{l} {q_{rain} +q_{sno} -E_{v} -E_{g} -q_{over} } \\ {-q_{h2osfc} -q_{drai} -q_{rgwl} -q_{snwcp,\, ice} } \end{array}\right) \Delta t} \end{array}

where :math:`q_{rain}`  is the liquid part of precipitation,
:math:`q_{sno}`  is the solid part of precipitation,
:math:`E_{v}`  is ET from vegetation,
:math:`E_{g}`  is ground evaporation,
:math:`q_{over}`  is surface runoff,
:math:`q_{h2osfc}`  is runoff from surface water storage,
:math:`q_{drai}`  is sub-surface drainage,
:math:`q_{rgwl}`  and
:math:`q_{snwcp,ice}`  are liquid and solid runoff from glaciers and lakes, and runoff from other surface types
due to snow capping 
(all in kg m\ :sup:`-2`
s\ :sup:`-1`), :math:`N_{levsoi}`  is the number of soil layers
(note that hydrology calculations are only done over soil layers 1 to
:math:`N_{levsoi}` ; ground levels :math:`N_{levsoi} +1` \ to
:math:`N_{levgrnd}` are currently hydrologically inactive; 
and :math:`\Delta t` is the time step (s).

