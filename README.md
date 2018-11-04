
# Pokemons and Data Visualization with R

## Context

Through this R notebook like document, we will try to learn R basics and use it to visualize data. However, we will not use R in its pure form. Indeed, there are several packages that make it much cleaner and much easier to use. Those powerful packages are : the ones in **tidyverse**, **dplyr** and **ggplot2**. To create interactive plots, we will also discover and use **shiny**. Finally, to create maps, we will need **leaflet**.

We’ve chosen our main dataset so that it will make this learning funnier, or at least that’s what we wanted. The dataset is about **Pokemons** ! More precisely, it is describing each of the Pokemons characteristics.

## Datasets


All our datasets are from Kaggle.

#### Our main dataset, describing Pokemons characteristics :
Name : pokemon.csv  
Size : 96 ko  
Source : https://www.kaggle.com/alopez247/pokemon  
Link used in the project : https://perso.esiee.fr/~ghidaglb/DRIO-4103C/pokemon.csv  


#### The dataset we’ll use to get Pokemon locations (in PokemonGO) :  
Name : 300k.csv  
Size : 497 646 ko  
**/!\ WARNING : the first time you'll run the project, it will have to download this file from the internet, so it may take a while ... But once it's done, the file is saved locally in a .csv /!\\**  
Source : https://www.kaggle.com/semioniy/predictemall#300k_csv.zip  
Link used in the project : https://perso.esiee.fr/~ghidaglb/DRIO-4103C/300k.csv  

#### A directory with an illustration of each Pokemon, to make our location plot nicer :  
Name : POKEMON.zip  
Source : https://www.kaggle.com/dollarakshay/pokemon-images  
Link used in the project : you'll download it with the repo  


## Required R packages installation

The following code is part of the projet :

    # Installing missing packages
	list.of.packages <- c("ggplot2", "RCurl", "shiny", "dplyr", "leaflet")
	new.packages <- list.of.packages[!(list.of.packages %in% installed.packages()[,"Package"])]
	if(length(new.packages)) install.packages(new.packages)

	# Importing libraries
	library(dplyr)
	library(ggplot2)
	library(leaflet)
	library(RCurl)
	library(shiny)

## How to run the project

You just need to open the *rapport.Rmd* file and hit the *Run Document* button in R studio. After a little while, a R notebook like document will be rendered.