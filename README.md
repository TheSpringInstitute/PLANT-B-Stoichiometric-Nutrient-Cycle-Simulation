### Simulation of Stoichiometric Nutrient Cycles for the PLANT-B CubeSat Terrarium Mission

## Project Background

This is a repository by Livian Von Dran, one of the entomologists for the PLANT-B CubeSat Terrarium Mission. Livian is making this repository as part of their final project for their Professional Graduate Certificate in Earth Data Analytics program. 

The PLANT-B CubeSat Terrarium Mission is an initiative by The Spring Institute for Forests on the Moon to send a bioactive terrarium into low-Earth orbit for two to five years. In an effort to support The Spring Insitite's mission of creating a self-sustaining terrarium ecosystem that can function in space without outside intervention, this repository was created to simulate stoichiometric nutrient cycles occurring inside the PLANT-B terrarium. The PLANT-B project is unique in that it is one of the first attempts to maintain a self-sustaining, Earth-like ecosystem directly in the space environment; experiments involving terrariums have been conducted inside the International Space Station (ISS), but no such experiments have occurred on a satellite. Such experiments further our understanding of bioregenerative life suppport systems—a necessary techology to support self-sustaining space settlements.

The influence of low-Earth orbit will pose multiple challenges to the terrarium's inhabitants. The orbital path dictates that the sealed ecosystem will be subject to rapidly shifting 60-30 minute light-dark cycles—similar to the daylight cycle occupants of the ISS experience. Additionally, the space environment will subject the terrarium's occupants to microgravity. The chosen invertebrates—*Trichorhina tomentosa* and *Folsomia candida*—are common fixtures in bioactive terrariums, serving as the detritivorous clean up crew that break down waste like feces and mold. These detritivores will play an essential role in removing the leaf litter of *Physcomitrium patens*, the primary producer candidate for the terrarium. This moss species is known for its remarkably resilient spores, which are capable of germinating after surviving in the vacuum of space for over nine months (Maeng et al., 2025). Unfortunately, this tolerance has its limits; the light cycle is anticipated to negatively impact the circadian rhythms of all organisms in the terrarium, and as a C3 photosynthetic producer, *P. patens* will likely struggle with the limited exposure of the "daylight" windows. Both invertebrates display photophobic behavior that will impact their movement through the ecosystem, but the lack of soil in the terrarium—Hygrolon is being used to reduce the weight of the final payload—will impact their burrowing behaviors (Ruiz, 2017). Literature on the impacts of microgravity on isopods and springtails is nonexistent, but microgravity may reduce the photosynthetic productivity of *P. patens* (Takemura, 2017). The true impact of the space environment cannot be quantified until simulations are complete, but the terrarium ecosystem is anticipated to be less productive than an identical exosystem on Earth.

## Data Background

This project is divided into two parts: habitat mapping and nutrient cycle simulation. A literature review is being undertaken to find missing stoichiometric data.

<ins>Global Biodiversity Information Facility (GBIF)</ins>

Mapping spatiotemporal data is a requirement for the final project, so observation data from GBIF was used to find an area of habitat overlap and extract soil nutrient concentrations in that area. An appropriate overlap area was found near the German-Polish-Czech border, but due to the scarcity of nitrogen in the soil sample, other locations are being sought out.

<ins>European Soil Data Centre (ESDAC)</ins>

The dataset being used from ESDAC is the LUCAS 2018 TOPSOIL dataset. This dataset consists of soil sample data that, among other variables, provides a measurement of the nutrient contents in a given soil sample. This provides a baseline for starting nutrient concentrations in an environment where the three selected species can coexist.

<ins>TRY Plant Trait Database</ins>

This database was used to find the nutrient concentration preferences for *P. patens*. As the database contains limited information on this specific species, a phylogenetic tree constructed by Rensing et al. was used to request information on closely related species (2020). 

<ins>StoichLife Database</ins>

The StoichLife data was used to determine the elemental compositions of closely related species to *Trichorhina tomentosa* and *Folsomia candida*. The relevance of this data is yet to be determined.

## Repository Replication Instructions

This repository's data was originally processed in the earth-analytics-python environment found in [this repository](https://github.com/earthlab/earth-analytics-python-env). A tutorial to set up this Conda environment can be found at [this link](https://earthdatascience.org/workshops/setup-earth-analytics-python). An updated yml with a new environment has been added to this repository.

<ins>Environment Creation Instructions</ins>

1. Download the installers for [Git Bash](https://git-scm.com/install/windows) and [Miniconda](https://www.anaconda.com/download/success). Run both installers.
2. Open the Git Bash terminal. Run the below commands in sequence:
   
   a.  mkdir earth-analytics

   This creates a directory called "earth-analytics."
   
   b. cd earth-analytics
    
      mkdir data

   This changes your working directory to "earth-analytics" and creates a directory inside it called "data."
   
3. Create a fork of [this repository](https://github.com/TheSpringInstitute/PLANT-B-Stoichiometric-Nutrient-Cycle-Simulation).
4. Return to Git Bash and run the below commands in sequence:
   
   a. cd ~

   This refreshes your working directory to default.
   
   b. cd earth-analytics

   This makes earth-analytics your working directory again.
    
   c. git clone https://github.com/[YOUR-GITHUB-USERNAME]/earth-analytics-python-env

   This clones your forked directory and downloads it to your computer.
   
   d. cd earth-analytics-python-env

   This turns "earth-analytics-python-env" into your working directory.

   e. conda env create -f environment.yml

   This creates the "plant-b-simulation" environment using the yml file.

   f. conda activate plant-b-simulation

   This activates the newly created Python environment.
   
6. Download and run the [Visual Studio Code installer](https://code.visualstudio.com/download). The created Python environment is accessible when ipynb files are opened in VS Code.

<ins>Notebook Parts and Data Download Info</ins>

The coding pipeline for the project can be found in the "notebooks" folder. Two separate notebooks have been created to correspond to the two phases of the project and are numbered to indicate the correct order for which they should be run. 

The first notebook that should be run is "part-1-gauging-habitat-nutrient-levels.ipynb." The purpose of this notebook is to determine appropriate soil nutrient concentrations in the area of habitat overlap for the PLANT-B species. The data sources used in this notebook are GBIF and ESDAC. At present, the Global Biodiversity Information Facility (GBIF) is the only database whose data was able to be downloaded through a function; ESDAC's LUCAS 2018 Topsoil Dataset requires a request to be submitted at https://esdac.jrc.ec.europa.eu/content/lucas-2018-topsoil-data#tabs-0-description=1. The TRY Plant Trait Database indicated that *Physcomitrium* species prefer moderate to high levels of nitrogen, so the original bounding box is being reconfigured to find more areas of habitat overlap to find more suitable nitrogen concentrations. Soil microbe data from ESDAC's Soil Biodiversity dataset may be incorporated into the final dataset if the large dataset can be downloaded successfully.

The second notebook that should be run is "part-2-simulating-nutrient-cycles.ipynb." The purpose of this notebook is to construct stoichiometric chemical equations and model the nutrient cycles inside the terrarium. This notebook is still under construction because some stoichiometry data is still missing. The stoichiometry data for the invertebrates can be found in the StoichLife dataset at https://datadryad.org/dataset/doi:10.5061/dryad.3tx95x6r2.

## DOI and Licensing
This repository is private, but a DOI was made for a public mirror of it to comply with school project requirements. A fully public release of the finalized repository may be made at the discretion of The Spring Institute. 

Under the Creative Commons Attribution-NoDerivatives (CC BY-ND) license, redistribution, replication, or alteration of the source code is strictly forbidden.

## Data Sources and Citations

González, A. L., Merder, J., Andraczek, K., Brose, U., Filipiak, M., Harpole, W. S., Hillebrand, H., Jackson, M. C., Jochum, M., Leroux, S. J., Nessel, M. P., Onstein, R. E., Paseka, R., Perry, G. L. W., Rugenski, A., Sitters, J., Sperfeld, E., Striebel, M., Zandona, E., Aymes, J.-C., Blanckaert, A., Bluhm, S. L., Doi, H., Eisenhauer, N., Farjalla, V. F., Hood, J., Kratina, P., Labonne, J., Lovelock, C. E., Moody, E. K., Mozsár, A., Nash, L., Pollierer, M. M., Potapov, A., Romero, G. Q., Roussel, J.-M., Scheu, S., Scheunemann, N., Seeber, J., Steinwandter, M., Susanti, W. I., Tiunov, A., & Dézerald, O. (2025). StoichLife: A Global Dataset of Plant and Animal Elemental Content. *Scientific Data*, *12*(1). https://doi.org/10.1038/s41597-025-04852-w

González, A. L., Merder, J., Andraczek, K., Brose, U., Filipiak, M., Harpole, W. S., Hillebrand, H., Jackson, M. C., Jochum, M., Leroux, S. J., Nessel, M. P., Onstein, R. E., Paseka, R., Perry, G. L. W., Rugenski, A., Sitters, J., Sperfeld, E., Striebel, M., Zandona, E., Aymes, J.-C., Blanckaert, A., Bluhm, S. L., Doi, H., Eisenhauer, N., Farjalla, V. F., Hood, J., Kratina, P., Labonne, J., Lovelock, C. E., Moody, E. K., Mozsár, A., Nash, L., Pollierer, M. M., Potapov, A., Romero, G. Q., Roussel, J.-M., Scheu, S., Scheunemann, N., Seeber, J., Steinwandter, M., Susanti, W. I., Tiunov, A., & Dézerald, O. (2025). StoichLife: A global database of plant and animal elemental content [Dataset]. *Dryad*. https://doi.org/10.5061/dryad.3tx95x6r2

Kattge, J., Bönisch, G., Díaz, S., Lavorel, S., Prentice, I. C., Leadley, P., Tautenhahn, S., Werner, G. D. A., Aakala, T., Abedi, M., Acosta, A. T. R., Adamidis, G. C., Adamson, K., Aiba, M., Albert, C. H., Alcántara, J. M., Alcázar C., C., Aleixo, I., Ali, H., Amiaud, B., . . . van der Plas, A. L. D. (2020). TRY plant trait database – enhanced coverage and open access. *Global Change Biology*, *26*(1), 119–188. https://doi.org/10.1111/gcb.14904

Labouyrie, M., Ballabio, C., Romero, F., Panagos, P., Jones, A., Schmid, M. W., Mikryukov, V., Dulya, O., Tedersoo, L., Bahram, M., Lugato, E., van der Heijden, M. G. A., & Orgiazzi, A. (2023). Patterns in soil microbial diversity across Europe. *Nature Communications*, *14*(1), 3311. https://doi.org/10.1038/s41467-023-37937-4

Maeng, C., Hiwatashi, Y., Nakamura, K., Matsuda, O., Mita, H., Tomita-Yokotani, K., Yokobori, S., Yamagishi, A., Kume, A., & Fujita, T. (2025). Extreme environmental tolerance and space survivability of the moss, *Physcomitrium patens*. *IScience*, *28(12), 113827. https://doi.org/10.1016/j.isci.2025.113827

Orgiazzi, A., Ballabio, C., Panagos, P., Jones, A., & Fernández-Ugalde, O. (2017). LUCAS Soil, the largest expandable soil dataset for Europe: a review. *European Journal of Soil Science*, *69*(1), 140–153. https://doi.org/10.1111/ejss.12499

Panagos P., Van Liedekerke M., Jones A., & Montanarella, L. (2012). European Soil Data Centre: Response to European policy support and public data requirements. *Land Use Policy*, *29*(2), 329-338. https://doi.org/10.1016/j.landusepol.2011.07.003

Panagos, P., Van Liedekerke, M., Borrelli, P., Köninger, J., Ballabio, C., Orgiazzi, A., Lugato, E., Liakos, L., Hervas, J., Jones, A., & Montanarella, L. (2022). European Soil Data Centre 2.0: Soil data and knowledge in support of the EU policies. *European Journal of Soil Science*, *73*(6), e13315. https://doi.org/10.1111/ejss.13315

Rensing, S. A., Goffinet, B., Meyberg, R., Wu, S.-Z., & Bezanilla, M. (2020). The Moss *Physcomitrium* (*Physcomitrella*) *patens*: A Model Organism for Non-Seed Plants. *The Plant Cell*, *32*(5), 1361–1376. https://doi.org/10.1105/tpc.19.00828

Takemura, K., Hiroyuki Kamachi, Kume, A., Fujita, T., Ichirou Karahara, & Hanba, Y. T. (2016). A hypergravity environment increases chloroplast size, photosynthesis, and plant growth in the moss Physcomitrella patens. *Journal of Plant Research*, *130*(1), 181–192. https://doi.org/10.1007/s10265-016-0879-z

Gallardo Ruiz, M., Le Galliard, J.-F., & Tully, T. (2017). Genetic variation in light vision and light-dependent movement behaviour in the eyeless Collembola *Folsomia candida*. *Pedobiologia*, *61*, 33–41. https://doi.org/10.1016/j.pedobi.2016.12.001

