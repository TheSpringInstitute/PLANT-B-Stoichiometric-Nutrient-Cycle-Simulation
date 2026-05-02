## Background
This is a repository by Livian Von Dran, one of the entomologists for the PLANT-B CubeSat Terrarium Mission. Livian is making this repository as part of their final project for their Professional Graduate Certificate in Earth Data Analytics program. 

The PLANT-B CubeSat Terrarium Mission is an initiative by The Spring Institute for Forests on the Moon to send a bioactive terrarium into low-Earth orbit for two to five years. In an effort to support The Spring Insitite's mission of creating a self-sustaining terrarium ecosystem that can function in space without outside intervention, this repository was created to simulate stoichiometric nutrient cycles occurring inside the PLANT-B terrarium.  This project is divided into two parts: habitat mapping and nutrient cycle simulation. Mapping spatiotemporal data is a requirement for the final project, so mapping has been performed to identify an area of habitat overlap near the German-Polish-Czech border. Determination of optimal soil nutrient concentration for PLANT-B's species is pending due to limited soil samples taken in the habitat area. A literature review is also being undertaken to find missing stoichiometric data.

Please feel free to use any data generated in this repository as needed. If you feel that changes need to be made to the repository to better suit the PLANT-B mission, email Livian at lvondran23@gmail.com with your suggestions or create a fork of this repository.

## DOI
This repository is private, but a DOI was made for a public mirror of it to comply with school project requirements: https://doi.org/10.5281/zenodo.19963779 A fully public release of the finalized repository may be made at the discretion of The Spring Institute. 

## Python Environment Creation
This repository's data was originally processed in the earth-analytics-python environment found in [this repository](https://github.com/earthlab/earth-analytics-python-env). A tutorial to set up this Conda environment can be found at [this link](https://earthdatascience.org/workshops/setup-earth-analytics-python). An updated yml may eventually be added to this repository at Livian's discretion, but folder names will be kept the same to enhance the reproducibility of the code.

<ins>Environment Creation Instructions</ins>

1. Download the installers for [Git Bash](https://git-scm.com/install/windows) and [Miniconda](https://www.anaconda.com/download/success). Run both installers.
2. Open the Git Bash terminal. Run the below commands in sequence:
   
   a.  mkdir earth-analytics

   This creates a directory called "earth-analytics."
   
   b. cd earth-analytics
    
      mkdir data

   This changes your working directory to "earth-analytics" and creates a directory inside it called "data."
   
3. Create a fork of [this repository](https://github.com/earthlab/earth-analytics-python-env).
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

   This creates the "earth-analytics-python" environment using the yml file.

   f. conda activate earth-analytics-python

   This activates the newly created Python environment.
   

6. Download and run the [Visual Studio Code installer](https://code.visualstudio.com/download). The created Python environment is accessible when ipynb files are opened in VS Code.





