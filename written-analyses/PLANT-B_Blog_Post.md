# Simulating Carbon and Nitrogen Cycles for a Space Terrarium

![The Spring Institute for Forests on the Moon logo.](https://github.com/TheSpringInstitute/PLANT-B-Stoichiometric-Nutrient-Cycle-Simulation/blob/main/img/The%20Spring%20Institute%20Logo.png)

<ins>Mission Overview</ins>

The PLANT-B CubeSat Terrarium Mission is a project by The Spring Institute for Forests on the Moon to send a bioactive—or self-sustaining—terrarium on a satellite into low-Earth orbit (LEO) for two to five years. PLANT-B is an acronym that stands for <b>P</b>assive <b>L</b>ight <b>a</b>nd <b>N</b>utrient <b>T</b>errarium-<b>B</b>iosphere, representative of the system's passive operations; the satellite is engineered to passively light and heat the 0.7 L terrarium. Inhabited by a plant and numerous microorganisms, this terrarium is unique in that it is one of the first attempts to maintain a self-sustaining, Earth-like ecosystem directly in the space environment; terrarium experiments have been conducted on the the International Space Station (ISS), but true biological payloads are rare, especially on satellites. By incorporating multiple trophic levels, the terrarium ecosystem grants us insight into the functioning of closed ecological life support systems (CELSS)—a biological space life support system that also incorporates multitrophic species assemblages to replenish life-sustaining resources for and maintain the habitability of a closed system. When space settlements become a reality, prospective inhabitants must be able to replenish their own resources to reduce dependence on resupply flights.

![An early PLANT-B terrarium prototype showing the spiral of Hygrolon the moss will grow on.](https://github.com/TheSpringInstitute/PLANT-B-Stoichiometric-Nutrient-Cycle-Simulation/blob/main/img/PLANT-B_Prototype.JPG)

To create a self-sustaining terrarium ecosystem that can function in space without outside intervention, all ecological processes must be accounted for. The "PLANT-B Stoichiometric Nutrient Cycle Simulation" GitHub repository was developed to simulate the terrarium ecosystem's carbon (C) and nitrogen (N) cycles. Initial simulations will provide a baseline reference point for understanding how nutrients flow throughout the terrarium ecosystem.

<ins>Meet the Residents</ins>

The LEO environment will pose two main challenges to the terrarium's inhabitants: rapidly shifting light-dark cycles and microgravity. The orbital path dictates that the sealed ecosystem will be subject to rapidly shifting 60-30 minute light-dark cycles—similar to the daylight cycle occupants of the ISS experience. Additionally, if the ISS is used as a reference point, the terrarium will experience gravity at approximately 90% the strength of Earth's gravity 

When conducting space experiments with biological organisms, a great degree of uncertainty is anticpated due to limited data, which is why model organisms are commonly used. One such model organism is *Physcomitrium patens*. This moss was selected as the producer for the terrarium because of its remarkably resilient spores, which are capable of germinating after surviving in the vacuum of space for over nine months (Maeng et al., 2025). Regrettably, this resilience has its limits; a study found that LEO daylight cycles inhibit plant development and photosynthetic productivity, and as a C3 plant, *P. patens* may have difficulty continuously "restarting" photosynthesis (Kalbacher & Gonzalez et al., 2016). *P. patens* is more photosynthetically productive in stronger-than-Earth gravity, so microgravity is expected to inhibit photosyntesis (Takemura et al., 2016).

![A cluster of Physcomitrium patens. Photo by Pirex at Wikimedia Commons.](https://upload.wikimedia.org/wikipedia/commons/d/dd/Physcomitrella.jpg?_=20101210214832)

*Trichorhina tomentosa* and *Folsomia candida* were the chosen invertebrates because they are common fixtures in bioactive terrariums, serving as the clean up crew that break down waste like feces and mold. Their primary role will be to break down the decomposing leaf litter of *P. patens*. It is difficult to infer how the space environment will impact these invertebrates because no space experiments involving isopods or springtails exist. *F. candida* is eyeless, but some of its movement behaviors are light dependent (Ruiz et al., 2017). It is reasonable to infer that the altered light-dark cycles will negatively impact the invertebrates' circadian rhythms. 

<ins>Gathering Data for the Simulations</ins>

To simulate carbon and nitrogen cycles, soil nutrient concentrations need to be known. To identify an appropriate area to take data from, observation data of *P. patens*, *T. tomentosa*, and *F. candida* was taken from the Global Biodiversity Information Facility (GBIF) and mapped out. This interactive map was used to identify an appropriate area of habitat overlap around the German-Polish-Czech border.

![PLANT-B species distribution near the German-Polish-Czech border.](https://github.com/TheSpringInstitute/PLANT-B-Stoichiometric-Nutrient-Cycle-Simulation/blob/main/plots/PLANT-B_Species_Border_Distribution.png)

To gather soil nutrient data for the overlap area, a request was submitted to the the European Soil Data Centre (ESDAC) for the LUCAS 2018 TOPSOIL data. When data within the set bounding box was examined, only one relevant soil sample was found. This soil sample yielded a C:N—or carbon: nitrogen—ratio of 9.86:1, indicating an environment where decomposition will occur very rapidly. Per an inquiry to the TRY Plant Trait database, *Physcomitrium* species have a nitrogen Ellenberg Indicator Value of 6 or 7 (Kattge et al., 2019)—indicating a preference for moderately fertile, nitrogen-rich soils—which corresponds to a C:N ratio of 10:1 (Sürmen et al., 2014).

![Carbon and nitrogen concentrations in a soil sample in the overlapping habitat area.](https://github.com/TheSpringInstitute/PLANT-B-Stoichiometric-Nutrient-Cycle-Simulation/blob/main/plots/PLANT-B_Species_Overlapping_Habitat_OC_and_N_Concentrations_Plot.png)

The StoichLife database was used to 

![Carbon and nitrogen compositions of the PLANT-B species by percent dry mass.](https://github.com/TheSpringInstitute/PLANT-B-Stoichiometric-Nutrient-Cycle-Simulation/blob/main/plots/PLANT-B_Species_Dry_Mass_Elemental_Composition.png)


<ins>Simulation Results</ins>


<ins>Analyzing and Discussing the Results</ins>

<ins>What Needs to be Done from Here?</ins>

<ins>References</ins>

Gallardo Ruiz, M., Le Galliard, J.-F., & Tully, T. (2017). Genetic variation in light vision and light-dependent movement behaviour in the eyeless Collembola Folsomia candida. *Pedobiologia*, 61, 33–41. https://doi.org/10.1016/j.pedobi.2016.12.001

Sürmen, B., Kutbay, H. G., Kılıç, D. D., Huseynova, R., & Kilinç, M. (2014). Ellenberg’s indicator values for soil nitrogen concentration and pH in selected swamp forests in the Central Black Sea region of Turkey. *Turkish Journal of Botany*, *38*(5), 883–895. https://doi.org/10.3906/bot-1311-43


