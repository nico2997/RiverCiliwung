# RiverCiliwung
![](figs/ciliwung%20map.jpg)

Contributors: Nico Septianus, Onno Bokhove

## TBD: FEV analysis using VBA/Excel for 2020 flood of River Ciliwung (Djakarta, Indonesia)

Work published as: 

TBD

Ciliwung River, a provincial cross-border river that flows by passing Bogor City, Depok City and ends up in the Jakarta bay is famous for major flooding in the capital city since 20th century (Ratnaningsih et al., 2019). With the total length of 75km from Mount Pangrango(upstream) to Jakarta Bay(downstream) and total area cover of 322 km2.

See also:
* 'Using flood-excess volume to assess and communicate flood-mitigation schemes': [presentation](http://www1.maths.leeds.ac.uk/~amttk/files/leedskyoto.pdf) and [poster](http://www1.maths.leeds.ac.uk/~amttk/files/INI_sept2018.pdf). 

### Graphical output 

#### Data analysis: from depth to discharge to FEV

From the ```/code``` dir, run: 
 * ```Ciliwungcode1.xlsm```  
 
The Excel/VBA script completes the FEV analysis and calls four plotting routines:
 * ```equation2()```
 * ```shadedarea()``` 
 * ```ratingcurve()``` 
 * ```FEV()``` 

in total, N figures are produced, including an adaptation of TBD:

![](figs/Ciliwungfinalplot.png)

*Caption: Quadrant plot for early 2020 new year flood of the River Ciliwung at Depok Floodgate.
The plot shows 3-panel graph between relationship of time vs height (original data), height
vs flowrate (rating curve), time vs flowrate (hydrograph).*

#### Cost-effectiveness analysis

Run ```mitigation()``` to produce mitigation analysis:

![](figs/mitigation1.png)

*Caption: First flood mitigation scenario that mitigates 96% of the FEV in the worst and 100% at the best. Technically, Ciawi and Sukamahi Dam are specifically to mitigate excess water which came from upstream and the remaining scheme (higher walls, planting trees, floodways) are to mitigate the excess water near downstream.*

![](figs/mitigation2.png)

*Caption: Second flood alternative scenario mitigates 100% of the FEV just with the floodways. Despite the low cost, however this mitigation relies heavily only on one mitigation.*

Below is the function correspond to the results (function name -> graph name):

equation2() -> the 3-panel graph (exclude the FEV shaded region).

shadedarea() -> the FEV shaded region (blue).

mitigation() -> the mitigation scheme (the colour is manually added).

threedshape() -> 2-meter deep square lake.

FEV() -> FEV-ht and 2-meter deep square - ht graph.

ratingcurve() -> only the rating curve graph.

p.s. : After you call the function. you need to delete the existing graph before run the function again. Since the nickname ofthe graph already exist. Unless, you change the nickname of the graph in the code. (I add -readertest to show the graph is call by you)
