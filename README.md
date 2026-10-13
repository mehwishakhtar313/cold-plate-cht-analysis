# Comparative CFD and Conjugate Heat Transfer Analysis of Cold-Plate Channel Designs

## 1. Project Overview

This project presents a comparative Computational Fluid Dynamics (CFD) and Conjugate Heat Transfer (CHT) analysis of two cooling-channel configurations for an aluminium cold plate using SimScale.

Both designs were simulated over a duration of 5000 seconds to investigate coolant velocity distribution, temperature patterns, and numerical convergence under the same general operating conditions.

The study evaluates how changes in channel geometry influence flow distribution and thermal behavior, providing insights into cold-plate design for thermal-management applications.

## 2. Project Objectives

- Compare coolant flow through two cold-plate channel configurations.
- Analyze velocity distribution and flow patterns within cooling passages.
- Compare temperature distributions across the aluminium plate.
- Examine residual convergence over a simulation interval of 5000 seconds.
- Investigate the influence of channel geometry on thermal performance.
- Identify the design characteristics that may contribute to effective cooling.

## 3. Software and Simulation Methodology

| Parameter | Value |
|---|---|
| Simulation Platform | SimScale |
| Analysis Type | Conjugate Heat Transfer (CHT) |
| Flow Regime | Incompressible |
| Turbulence Model | k-ω SST |
| Coolant | 50% ethylene glycol + 50% water |
| Solid Material | Aluminium |
| Applied Surface Heat Flux | 400 W/m² |
| Inlet Pressure | 2000 Pa |
| Outlet Pressure | 20 Pa |
| Ambient Temperature at Outlet Pressure Boundary | 20°C |
| Mesh Fineness | 5 |
| Simulation Duration | 5000 s |

The conjugate heat transfer approach accounts for fluid flow through the cooling channels, heat conduction through the aluminium plate, and heat transfer between the coolant and the solid.

The same general operating conditions and mesh fineness level were used for both designs to facilitate comparison.

## 4. Coolant Properties

The coolant was modeled as a 50% ethylene glycol–water mixture using constant thermophysical properties.

| Property | Value |
|---|---:|
| Density | 1079 kg/m³ |
| Dynamic Viscosity | 0.003912 kg/(m·s) |
| Kinematic Viscosity | 3.63 × 10⁻⁶ m²/s |
| Specific Heat Capacity | 3473 J/(kg·K) |
| Thermal Conductivity | 0.4257 W/(m·K) |
| Prandtl Number | 31.9 |
| Turbulent Prandtl Number | 0.85 |
| Reference Temperature | 293.15 K |

## 5. Design 1: Closely Spaced Serpentine Channels

### 5.1 Geometry and Mesh

Design 1 consists of numerous closely spaced serpentine cooling passages distributed throughout the cold plate. The coolant travels through successive channel sections, creating an extended flow path across the plate.

This configuration provides a distributed network of cooling passages.

![Design 1 Mesh](images/design1_mesh.png)

### 5.2 Temperature Distribution

The temperature contour shows a progressive change in thermal conditions along the serpentine flow path. Darker colours appear near the inlet and initial sections, while warmer colours extend across much of the remaining channel network.

This pattern is consistent with progressive coolant heating as heat is transferred from the plate to the coolant.

![Design 1 Temperature Contour](images/design1_temp_contour.png)

### 5.3 Velocity Distribution

The velocity contour illustrates coolant flow through the closely spaced serpentine passages. Local velocity variations appear near the inlet junctions and channel turns.

The multiple passages distribute the flow across the plate, although the degree of flow uniformity would require quantitative analysis to confirm.

![Design 1 Velocity Contour](images/design1_velocity_contour.png)

### 5.4 Residual Convergence

The residual history extends to 5000 seconds. The monitored residuals decrease substantially during the initial stages and subsequently fluctuate around relatively stable levels.

Some residuals continue to exhibit oscillations, indicating that convergence should also be assessed using physical monitoring quantities such as mass-flow balance, pressure difference, and temperature.

![Design 1 Residuals](images/design1_residuals.png)

## 6. Design 2: Modified Channels with a Central Manifold

### 6.1 Geometry and Mesh

Design 2 uses a modified channel arrangement with fewer serpentine passages and a more prominent central distribution manifold.

The modified geometry changes the flow path and the way coolant is distributed through the cooling-channel network.

![Design 2 Mesh](images/design2_mesh.png)

### 6.2 Temperature Distribution

The temperature contour shows a different thermal pattern from Design 1. Cooler colours appear across portions of the upper channel sections, while warmer colours are visible along parts of the lower channels and outer perimeter.

Because both designs use the same numerical temperature range and colour scale, these differences can be compared directly. The contour suggests greater spatial variation in temperature across Design 2.

![Design 2 Temperature Contour](images/design2_temp_contour.png)

### 6.3 Velocity Distribution

The velocity contour shows localized velocity variations around the central manifold, channel junctions, and connecting passages.

Compared with Design 1, the modified distribution region changes how the flow enters and travels through the channels. These local variations highlight the importance of manifold geometry in cooling-plate design.

![Design 2 Velocity Contour](images/design2_velocity_contour.png)

### 6.4 Residual Convergence

The residual history extends to 5000 seconds. The residuals decrease substantially during the initial stages before exhibiting fluctuations around relatively stable levels.

Some monitored variables display noticeable oscillations during the later stages. Further checks of mass-flow balance, pressure difference, and thermal monitoring quantities would help determine whether the solution is sufficiently converged.

![Design 2 Residuals](images/design2_residuals.png)

## 7. Comparative Analysis

| Parameter | Design 1 | Design 2 |
|---|---|---|
| Channel Configuration | Numerous closely spaced serpentine passages | Fewer passages with a central distribution manifold |
| Flow Path | Extended serpentine path | Modified path influenced by the central manifold |
| Velocity Distribution | Flow distributed across multiple passages, with local variations at turns | Localized variations around the manifold and channel junctions |
| Temperature Distribution | Progressive thermal pattern along the serpentine path | More spatially varied thermal pattern across the plate |
| Temperature Colour Scale | Same numerical range | Same numerical range |
| Residual Behavior | Substantial initial reduction followed by fluctuations | Substantial initial reduction followed by fluctuations |
| Simulation Duration | 5000 s | 5000 s |
| Mesh Fineness | 5 | 5 |
| Quantitative Pressure Drop | Not extracted | Not extracted |
| Quantitative Heat-Transfer Rate | Not extracted | Not extracted |

## 8. Velocity and Flow Distribution: Discussion

The velocity contours demonstrate that channel geometry influences the distribution of coolant throughout the cold plate.

Design 1 provides numerous closely spaced passages through which the coolant travels along an extended serpentine path. The contour shows local velocity variations around channel turns and inlet regions.

Design 2 introduces a central distribution manifold, producing a different flow pattern around the manifold and connecting passages. These regions are important when evaluating flow distribution and potential hydraulic limitations.

The velocity contours provide qualitative insight into the flow field. However, the design with the highest local velocity is not necessarily the best-performing design. A more complete comparison would require mass-flow distribution among individual passages, average velocity, and pressure drop.

## 9. Heat Dissipation and Thermal Performance: Discussion

Both designs were subjected to the same prescribed surface heat flux of 400 W/m², and their temperature contours use the same numerical colour scale.

Design 1 shows a progressive temperature pattern along the serpentine flow path, while Design 2 displays more spatially varied temperature regions. These differences indicate that the channel configuration influences the thermal distribution across the cold plate.

**Based on the available contours, Design 1 appears to provide a more progressive thermal distribution, whereas Design 2 exhibits more localized temperature variations.**

A more progressive temperature distribution can be useful for understanding how the coolant warms along its path. However, it does not automatically mean that Design 1 dissipates more total heat. The total heat removed depends on factors such as coolant mass flow rate, inlet and outlet temperatures, and the energy transferred from the plate.

The heat absorbed by the coolant can be estimated using:

\[
\dot{Q}=\dot{m}c_p(T_{\mathrm{out}}-T_{\mathrm{in}})
\]

where:

- \(\dot{Q}\) is the heat-transfer rate in watts.
- \(\dot{m}\) is the coolant mass flow rate in kg/s.
- \(c_p\) is the coolant specific heat capacity in J/(kg·K).
- \(T_{\mathrm{out}}\) and \(T_{\mathrm{in}}\) are the outlet and inlet coolant temperatures.

Although the contours allow qualitative comparison, numerical temperature and heat-transfer data would be needed to establish which design removes more heat.

## 10. Residual Convergence Assessment

Both simulations show a substantial reduction in residuals from their initial values, followed by fluctuations during the later stages.

The residual plots provide insight into the numerical behavior of each solution. However, residual reduction alone is insufficient to establish complete physical convergence.

A stronger assessment would include:

- Mass-flow balance between inlets and outlet.
- Pressure difference across the cold plate.
- Maximum and average plate temperatures.
- Coolant outlet temperature.
- Heat-transfer rate and energy balance.

The 5000-second simulation duration provides an extended interval for observing the solution behavior, but the duration itself does not guarantee convergence.

## 11. Limitations

- Exact maximum and average temperatures were not extracted because of limitations in the available SimScale package.
- Pressure-drop comparisons were not quantified.
- Heat-transfer rates and thermal resistance were not calculated.
- Individual channel mass-flow rates were not extracted.
- Coolant properties were treated as constant.
- A mesh-independence study was not performed.
- Residual histories alone do not establish complete physical convergence.
- The comparison is based primarily on qualitative contour interpretation rather than quantitative performance metrics.

## 12. Future Work

- Extract maximum and average plate temperatures for both designs.
- Monitor coolant inlet and outlet temperatures.
- Calculate pressure drop and total mass flow rate.
- Determine heat-transfer rate and thermal resistance.
- Investigate flow distribution among individual channels.
- Verify the energy balance between the heated plate and coolant.
- Perform mesh-independence and convergence studies.
- Investigate the effects of channel width, spacing, and manifold geometry.
- Explore cold-plate applications in hydrogen fuel-cell thermal management.

## 13. Key Findings

- Both channel configurations produce distinct velocity and temperature distributions.
- Design 1 provides numerous closely spaced serpentine passages and a progressive thermal pattern along the flow path.
- Design 2 uses a central distribution manifold and shows more localized variations in velocity and temperature.
- Both residual plots show substantial initial reduction followed by later fluctuations.
- The same numerical temperature scale enables direct qualitative comparison between the two designs.
- Channel geometry influences both flow distribution and thermal behavior.
- Quantitative heat-transfer and hydraulic metrics are still required to determine which design provides superior overall cooling performance.

## 14. Skills Demonstrated

- Computational Fluid Dynamics (CFD)
- Conjugate Heat Transfer (CHT)
- SimScale
- Internal Flow Simulation
- Thermal Management
- Cooling-Channel Design
- Mesh Generation
- k-ω SST Turbulence Modelling
- Pressure-Driven Flow
- Temperature-Field Analysis
- Velocity-Field Analysis
- Residual Convergence Assessment
- Comparative Engineering Analysis
- CFD Post-Processing

## 15. Conclusion

This project presents a comparative CFD and conjugate heat transfer investigation of two aluminium cold-plate channel configurations simulated over 5000 seconds.

The results demonstrate that channel geometry influences coolant velocity distribution and the resulting temperature field. Design 1, with its closely spaced serpentine passages, exhibits a progressive thermal pattern along the flow path. In contrast, Design 2, with its central distribution manifold and fewer serpentine passages, shows more localized variations in flow and temperature.

**Based on the available velocity and temperature contours, Design 1 appears to provide a more progressive thermal distribution, while Design 2 exhibits greater spatial variation across the plate.** This suggests that the channel arrangement plays an important role in thermal management.

Further quantitative analysis of maximum plate temperature, pressure drop, coolant mass flow rate, and heat-transfer rate would be required to determine which configuration delivers better overall cooling performance.


## 16. Simulation Platform

The simulations were performed using **SimScale**.

[SimScale](https://www.simscale.com/projects/mehwish_akhtar/cfd_and_thermal_analysis_of_a_cold_plate_for_hydrogen_fuel_cell_cooling_1654571654/)


## 17. Acknowledgment

The cold-plate concept and tutorial workflow were based on the SimScale cold-plate simulation tutorial. The present work was independently configured and analyzed to study the behavior of two channel configurations.

The project is intended as a CFD learning and portfolio study and does not represent a validated experimental design.
