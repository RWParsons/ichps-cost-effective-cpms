# Cost-effective clinical prediction models

This repository contains the code used to generate the results presented in my [ICHPS2023](https://ww2.amstat.org/meetings/ichps/2023/) poster.

### Value-optimising cutpoint

In this project, we propose using a cutpoint which maximises the net monetary benefit. A shiny app to select the cutpoint (among others) using simulated or user-provided data is available [here](https://aushsi.shinyapps.io/cost-effective-cpms-app/) and the code for that app is [here](https://github.com/RWParsons/cost-effective-cpms-app).

### {predictNMB} <a href='https://rwparsons.github.io/predictNMB/'><img src='https://raw.githubusercontent.com/RWParsons/predictNMB/ec40de8e9a08b49f2a22063e7f416cbd46a72155/man/figures/logo.png' align="right" height="139" /></a>

This work led to the development of an R package, `predictNMB`. It is a wrapper package that lets the user perform a simulation study to evaluate a hypothetical clinical prediction model that's used to assign patient interventions and evaluates it using the net monetary benefit (NMB). For more details on this package, see the website: <https://rwparsons.github.io/predictNMB/>

The analyses and the figures presented in the poster were made using predictNMB.
