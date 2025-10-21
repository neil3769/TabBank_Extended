This file contains detailed description about each of the datasets to be considered for checking TabPFN performance.

---
# Industrial Domain - Manufacturing


## 1. `AI4I 2020 Predictive Maintenance Dataset`
- **Description:** The AI4I 2020 Predictive Maintenance Dataset is a synthetic dataset that reflects real predictive maintenance data encountered in industry.
- **Source:** <a href="https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset">UCIMLR</a>
- **File:**  ![AI4I_2020_Predictive_Maintenance.csv](.datasets/Industry_Manufacturing/AI4I_2020_Predictive_Maintenance.csv)
- **#Rows:** 10000
- **#Features:** 14
- **Target:** `MachineFailure`
- **#Views:** 85066 (as of October 21, 2025)
- **Additional Description:** "Since real predictive maintenance datasets are generally difficult to obtain and in particular difficult to publish, we present and provide a synthetic dataset that reflects real predictive maintenance encountered in industry to the best of our knowledge."
- **Features:** <br>
`UDI`: Unique ID <br>
`ProductID`: Unique Product ID<br>
`Type`: Product Quality Variant. L: Low, M: Medium, H: High<br>
`AirTemperature`: Generated with random walk process normalised to a standard deviation of 2K (K)<br>
`ProcessTemperature`: Generated with random walk process normalised to a standard deviation of 1K added to air temperature plus 10K (K)<br>
`RotationalSpeed`: Calculated from power of 2860W, overlaid with normal noise (rpm)<br>
`Torque`: Torque values are normally distributed around 40Nm with a σ = 10 Nm and no negative values (Nm)<br>
`ToolWear`: Quality variants H/M/L add 5/3/2 minutes of tool wear to the used tool in the process (min)<br>
`TWF (Tool Wear Failure)`: Tool will be replaced or fail at a randomly selected tool wear time between 200 – 240 mins<br>
|- Case for 120 data points <br>
`HDF (Heat Dissipation Failure)`: Heat dissipation causes a process failure, if the difference between air and process temperature is 
below 8.6 K and the tool’s rotational speed is below 1380 rpm<br>
|- Case for 115 data points <br>
`PWF (Power Failure)`: Product of torque and rotational speed (in rad/s) equals the power required for the process. If this power is below 3500 W or above 9000 W, the
process fails <br>
|- Case for 95 data points <br>
`OSF (Overstrain Failure)`: If the product of tool wear and torque exceeds 11,000 minNm for the L product variant (12,000 for M, 13,000 for H), the process fails due
to overstrain<br>
|- Case for 98 data points <br>
`RNF (Random Failures)`: Each process has a chance of 0,1 % to fail regardless of its process parameters<br>
|- Case for 19 data points <br>
`MachineFailure (Target)`: Did the machine fail at this particular datapoint due to any to above five failure categories?<br>


## 2. `Productivity Prediction of Garment Employees`
- **Description:** This dataset includes important attributes of the garment manufacturing process and the productivity of the employees which had been collected manually and also been validated by the industry experts.
- **Source:** <a href="https://archive.ics.uci.edu/dataset/597/productivity+prediction+of+garment+employees">UCIMLR</a>
- **File:**  ![garments_worker_productivity.csv](.datasets/Industry_Manufacturing/garments_worker_productivity.csv)
- **#Rows:** 1197
- **#Features:** 14
- **Target:** `actual_productivity`
- **#Views:** 50927 (as of October 21, 2025)
- **Additional Description:** "The Garment Industry is one of the key examples of the industrial globalization of this modern era. It is a highly labour-intensive industry with lots of manual processes. Satisfying the huge global demand for garment products is mostly dependent on the production and delivery performance of the employees in the garment manufacturing companies. So, it is highly desirable among the decision makers in the garments industry to track, analyse and predict the productivity performance of the working teams in their factories. This dataset can be used for regression purpose by predicting the productivity range (0-1) or for classification purpose by transforming the productivity range (0-1) into different classes."
- **Features:** <br>
`date`: Date in MM-DD-YYYY <br>
`day`: Day of the Week<br>
`quarter`: A portion of the month. A month was divided into four quarters<br>
`department`: Associated department with the instance<br>
`team_no`: Associated team number with the instance<br>
`no_of_workers`: Number of workers in each team<br>
`no_of_style_change`: Number of changes in the style of a particular product<br>
`targeted_productivity`: Targeted productivity set by the Authority for each team for each day<br>
`smv`: Standard Minute Value, it is the allocated time for a task<br>
`wip`: Work in progress. Includes the number of unfinished items for products<br>
`over_time`:Represents the amount of overtime by each team in minutes<br>
`idle_time`: The amount of time when the production was interrupted due to several reasons<br>
`idle_men`: The number of workers who were idle due to production interruption<br>
`actual_productivity (Target)`: The actual % of productivity that was delivered by the workers. It ranges from 0-1<br>

## 3. `Predicting Manufacturing Defects Dataset`
- **Description:** This dataset provides insights into factors influencing defect rates in a manufacturing environment. Each record represents various metrics crucial for predicting high or low defect occurrences in production processes.
- **Source:** <a href="https://www.kaggle.com/datasets/rabieelkharoua/predicting-manufacturing-defects-dataset">Kaggle</a>
- **File:**  ![manufacturing_defect_dataset.csv](.datasets/Industry_Manufacturing/manufacturing_defect_dataset.csv)
- **#Rows:** 3240
- **#Features:** 17
- **Target:** `DefectStatus`
- **#Views:** 35500 (as of October 21, 2025)
- **#Downloads:** 7265 (as of October 21, 2025)

- **Features:** <br>
`ProductionVolume`: Number of units produced per day <br>
`ProductionCost`: Cost incurred for production per day<br>
`SupplierQuality`: Quality ratings of suppliers<br>
`DeliveryDelay`: Average delay in delivery<br>
`DefectRate`: Defects per thousand units produced<br>
`QualityScore`: Overall quality assessment<br>
`department`: Associated department with the instance<br>
`MaintenanceHours`: Hours spent on maintenance per week<br>
`DowntimePercentage`: Percentage of production downtime<br>
`InventoryTurnover`: Ratio of inventory turnover<br>
`StockoutRate`: Rate of inventory stockouts<br>
`WorkerProductivity`: Productivity level of the workforce<br>
`EnergyConsumption`:  Energy consumed in kWh<br>
`EnergyEfficiency`: Efficiency factor of energy usage<br>
`AdditiveProcessTime`: Time taken for additive manufacturing<br>
`AdditiveMaterialCost`: Cost of additive materials per unit<br>
`DefectStatus (Target)`: Predicted defect status<br>

## 4. `Predicting Manufacturing Defects Dataset`
- **Description:** This dataset provides insights into factors influencing defect rates in a manufacturing environment. Each record represents various metrics crucial for predicting high or low defect occurrences in production processes.
- **Source:** <a href="https://www.kaggle.com/datasets/rabieelkharoua/predicting-manufacturing-defects-dataset">Kaggle</a>
- **File:**  ![manufacturing_defect_dataset.csv](.datasets/Industry_Manufacturing/manufacturing_defect_dataset.csv)
- **#Rows:** 3240
- **#Features:** 17
- **Target:** `DefectStatus`
- **#Views:** 35500 (as of October 21, 2025)
- **#Downloads:** 7265 (as of October 21, 2025)

- **Features:** <br>
`ProductionVolume`: Number of units produced per day <br>
`ProductionCost`: Cost incurred for production per day<br>
`SupplierQuality`: Quality ratings of suppliers<br>
`DeliveryDelay`: Average delay in delivery<br>
`DefectRate`: Defects per thousand units produced<br>
`QualityScore`: Overall quality assessment<br>
`department`: Associated department with the instance<br>
`MaintenanceHours`: Hours spent on maintenance per week<br>
`DowntimePercentage`: Percentage of production downtime<br>
`InventoryTurnover`: Ratio of inventory turnover<br>
`StockoutRate`: Rate of inventory stockouts<br>
`WorkerProductivity`: Productivity level of the workforce<br>
`EnergyConsumption`:  Energy consumed in kWh<br>
`EnergyEfficiency`: Efficiency factor of energy usage<br>
`AdditiveProcessTime`: Time taken for additive manufacturing<br>
`AdditiveMaterialCost`: Cost of additive materials per unit<br>
`DefectStatus (Target)`: Predicted defect status<br>

---
# Industrial Domain - Construction


## 5. `Building Structural Health Sensor Dataset`
- **Description:** This dataset is designed for research and development in Structural Health Monitoring (SHM) using embedded systems and machine learning techniques. It contains simulated time-series sensor data representing the physical state of building structures under various operational and environmental conditions.
- **Source:** <a href="https://www.kaggle.com/datasets/ziya07/building-structural-health-sensor-dataset/data">Kaggle</a>
- **File:**  ![building_health_monitoring_dataset.csv](.datasets/Industry_Manufacturing/building_health_monitoring_dataset.csv)
- **#Rows:** 1000
- **#Features:** 7
- **Target:** `ConditionLabel`
- **#Views:** 1508 (as of October 21, 2025)
- **#Downloads:** 263 (as of October 21, 2025)

- **Features:** <br>
`Timestamp`: Date and time of recording <br>
`Accel_X`: Accelerometer reading on X axis (m/s^2)<br>
`Accel_Y`: Accelerometer reading on Y axis (m/s^2)<br>
`Accel_Z`: Accelerometer reading on Z axis (m/s^2)<br>
`Strain`: Microstrain reading (Î¼Îµ)<br>
`Temp`: Reading from temperature sensors (Â°C)<br>
`ConditionLabel (Target)`: Structural condition, 0: Healthy, 1: Minor Damage, 2: Severe Damage<br>

---
# Industrial Domain - Materials


## 5. `Concrete Compressive Strength`
- **Description:** Concrete is the most important material in civil engineering. The concrete compressive strength is a highly nonlinear function of age and ingredients.
- **Source:** <a href="https://archive.ics.uci.edu/dataset/165/concrete+compressive+strength">UCIMLR</a>
- **File:**  ![Concrete_Data.csv](.datasets/Industry_Manufacturing/Concrete_Data.csv)
- **#Rows:** 1030
- **#Features:** 9
- **Target:** `ConcreteCompressiveStrength`
- **#Views:** 88099 (as of October 21, 2025)

- **Features:** <br>
`Cement`: Quantity of cement in the concrete mix, the primary binding material responsible for strength gain (kg/m³) <br>
`BlastFurnaceSlag`: Supplementary cementitious material that improves long-term strength and durability (kg/m³)<br>
`Fly_Ash`: Byproduct from coal combustion; acts as a pozzolanic additive enhancing workability and strength (kg/m³)<br>
`Water`: Amount of mixing water; affects workability and strength (higher water reduces strength) (kg/m³)<br>
`Superplasticizer`: Chemical admixture that improves workability without adding extra water (kg/m³)<br>
`CoarseAggregate`: Crushed stone or gravel providing bulk and strength to the concrete (kg/m³)<br>
`FineAggregate`: Sand used to fill voids and improve finish and density (kg/m³)<br>
`Age`: Curing age of the concrete at the time of strength testing. Strength increases with age (days)<br>
`ConcreteCompressiveStrength (Target)`: Compressive strength of the cured concrete specimen, the main indicator of material performance (MPa)<br>

## 6. `Material science dataset for battery prediction`
- **Description:** Concrete is the most important material in civil engineering. The concrete compressive strength is a highly nonlinear function of age and ingredients.
- **Source:** <a href="https://archive.ics.uci.edu/dataset/165/concrete+compressive+strength">UCIMLR</a>
- **File:**  ![lithium_battery_materials.csv](.datasets/Industry_Manufacturing/lithium_battery_materials.csv)
- **#Rows:** 1030
- **#Features:** 9
- **Target:** `is_semiconductor`
- **#Views:** 1873 (as of October 21, 2025)
- **#Downloads:** 240 (as of October 21, 2025)

- **Features:** <br>
`material_id`: Unique Materials Project ID for each compound <br>
`formula_pretty`: Chemical formula of the compound<br>
`n_elements`: Number of distinct chemical elements present in the compound<br>
`formation_energy_per_atom`: Formation energy per atom, typically computed via DFT; reflects thermodynamic stability (negative values = more stable)<br>
`contains_transition_metal`: Indicates whether the compound contains a transition-metal element (T/F)<br>
`energy_per_atom`: Total DFT-calculated energy per atom; baseline for comparing relative stabilities (eV/atom)<br>
`band_gap`: Electronic band gap energy, key property indicating whether a material is metallic or insulating (eV)<br>
`density`: Material density derived from crystal structure and atomic masses<br>
`volume`: Volume of the material’s primitive or conventional unit cell, per formula unit<br>
`elements`: List of individual elements present in the compound; useful for compositional feature engineering<br>
`is_semiconductor (Target)`: True if the band gap exceeds a defined threshold (usually >0 eV); indicates semiconducting behavior (T/F)<br>

## 7. ` Inorganic ABX3 Perovskite Materials Dataset`
- **Description:** Concrete is the most important material in civil engineering. The concrete compressive strength is a highly nonlinear function of age and ingredients.
- **Source:** <a href="https://github.com/chenebuah/ML_abx3_dataset">GitHub</a>
- **File:**  ![abc3_data.csv](.datasets/Industry_Manufacturing/abc3_data.csv)
- **#Rows:** 4557
- **#Features:** 21
- **Target:** `stable`

- **Features:** <br>
`mp_id`: Unique Materials Project identifier for each compound; can be used to retrieve metadata or structure <br>
`formula`: Chemical formula of the material in reduced form<br>
`sites`: Number of atomic sites (unique atoms) in the unit cell<br>
`composition`: Stoichiometric breakdown of atomic species within the formula<br>
`a_edge`: Lattice parameter a, the length of the unit-cell edge along x-axis (angstom)<br>
`b_edge`: Lattice parameter b, the length of the unit-cell edge along x-axis (angstom)<br>
`c_edge`: Lattice parameter c, the length of the unit-cell edge along x-axis (angstom)<br>
`alpha_ang`: Unit-cell angle α between b and c axes (degrees)<br>
`beta_ang`: Unit-cell angle β between b and c axes (degrees)<br>
`gamma_ang`: Unit-cell angle γ between b and c axes (degrees)<br>
`crystal_system`: Crystal family or symmetry system derived from the lattice parameters (e.g., cubic, tetragonal, orthorhombic)<br>
`space_group`: International (Hermann–Mauguin) space-group symbol describing atomic symmetry<br>
`total_magnetisation`: Total magnetic moment per unit cell, calculated from spin-polarized DFT (bohr)<br>
`energy_per_atom`: DFT-computed total energy per atom in the relaxed structure (eV/atom)<br>
`formation_energy`: Formation energy per atom relative to elemental reference phases, negative values indicate stability (eV/atom)<br>
`energy_above_hull`: Energy difference above the thermodynamic convex hull; 0 = thermodynamically stable (eV/atom)<br>
`density`: Calculated density from mass and unit-cell volume (g/cm³)<br>
`band_gap`: Electronic band gap computed from DFT (may underestimate experimental values) (eV)<br>
`direct_bandgap`: True if band gap is direct (valence-band maximum and conduction-band minimum at same k-point)<br>
`volume`: Unit-cell volume of the relaxed structure (cubic angstrom)<br>
`bulk_modulus`: Elastic bulk modulus, resistance to uniform compression; values may be given as dict (Voigt, Reuss, VRH averages) (GPa)<br>
`shear_modulus`: Elastic shear modulus, resistance to shape deformation; also provided as averaged values (GPa)<br>
`stable (Target)`: Thermodynamic stability indicator (TRUE if on the convex hull, else FALSE)<br>


## 8. `Supply Chain Dataset`
- **Description:** This is a dataset we collected from a Fashion and Beauty startup. The dataset is based on the supply chain of Makeup products.
- **Source:** <a href="https://www.kaggle.com/datasets/amirmotefaker/supply-chain-dataset">Kaggle</a>
- **File:**  ![supply_chain_data.csv](.datasets/Industry_Manufacturing/supply_chain_data.csv)
- **#Rows:** 101
- **#Features:** 24
- **Target:** `RevenueGenerated`

- **Features:** <br>
`ProductType`: Category of the product<br>
`SKU`: Unique stock keeping unit (product code)<br>
`Price`: Selling price per unit of product<br>
`Availability`: Number of items currently available in stock or percentage availability<br>
`NumberOfProductsSold`: Quantity of units sold<br>
`CustomerDemographics`: Demographic information of customers (gender, segment, etc.)<br>
`StockLevels`: Current warehouse stock level for the product<br>
`LeadTimes`: Supplier lead time (days) for delivery of ordered goods<br>
`OrderQuantities`: Quantity ordered per batch or replenishment cycle<br>
`ShippingTimes`: Time (days) taken to deliver goods to customers<br>
`ShippingCarriers`: Name or code of carrier responsible for delivery<br>
`ShippingCosts`: Cost incurred in shipping goods<br>
`SupplierName`: Supplier providing the materials or finished goods<br>
`Location`: Geographic location of supplier or manufacturing site<br>
`LeadTime`: Time (days) between order placement and supplier dispatch<br>
`ProductionVolumes`: Total units produced in the period<br>
`ManufacturingLeadTime`: Time (days) required to manufacture the product<br>
`ManufacturingCosts`: Cost incurred to produce the product batch<br>
`InspectionResults`: Outcome of quality inspection<br>
`DefectRates`: Proportion of defective units found during inspection<br>
`TransportationModes`: Mode of transport used for distribution<br>
`Routes`: Distribution route code or identifier<br>
`Costs`: Total logistics or transportation cost for the route<br>
`RevenueGenerated (Target)`: Total sales revenue for the product<br>