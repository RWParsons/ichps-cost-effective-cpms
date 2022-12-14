
# Cost-effective clinical prediction models

This repository contains the code used to generate the results presented
in my [ICHPS2023](https://ww2.amstat.org/meetings/ichps/2023/) poster.

### Value-optimising cutpoint

In this project, we propose using a cutpoint which maximises the net
monetary benefit. A shiny app to select the cutpoint (among others)
using simulated or user-provided data is available
[here](https://aushsi.shinyapps.io/cost-effective-cpms-app/) and the
code for that app is
[here](https://github.com/RWParsons/cost-effective-cpms-app).

### {predictNMB} <a href='https://rwparsons.github.io/predictNMB/'><img src='https://raw.githubusercontent.com/RWParsons/predictNMB/ec40de8e9a08b49f2a22063e7f416cbd46a72155/man/figures/logo.png' align="right" height="139" /></a>

This work led to the development of an R package, `predictNMB`. It is a
wrapper package that lets the user perform a simulation study to
evaluate a hypothetical clinical prediction model that’s used to assign
patient interventions and evaluates it using the net monetary benefit
(NMB). For more details on this package, see the website:
<https://rwparsons.github.io/predictNMB/>

The analyses and the figures presented in the poster were made using
predictNMB.

### Inputs used for inpatient falls use case presented in the poster

| Input                             | Citation                                       | Value                                                                                                                                            | Transformed distribution     |
|-----------------------------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| Treatment cost of fall prevention | ([Hill et al. 2015](#ref-hill2015fall))        | Cost = 77.30                                                                                                                                     | N/A                          |
| Cost of in-hospital fall          | ([Morello et al. 2015](#ref-morello2015extra)) | Mean = 6669 \[95% CI: 3888, 9450\]                                                                                                               | Gamma(22.0516, 0.0033)       |
| Effectiveness of fall prevention  | ([Haines et al. 2011](#ref-haines2011patient)) | Adjusted HR = 0.43 \[95% CI: 0.24, 0.78\]                                                                                                        | Exp(Normal(-0.8440, 0.3038)) |
| Utility decrement of falling      | ([Latimer et al. 2013](#ref-latimer2013cost))  | <b>Utility (decrement, n):</b><br>No injury (-0.02, 40);<br>minor injury (-0.04, 31);<br>moderate injury (-0.06, 18);<br>major injury (-0.11, 9) | Beta(2.4253, 55.4053)        |

The model AUC of 0.75 seemed reasonable but there is a large spread in
reported levels of performance in the literature that we reviewed
([Parsons et al. 2022](#ref-parsons2022inpatient)).

The expected event rate of 0.008 is based on a summary of our own data
at Metro South Health hospitals. Across the 5 hospitals during 2018-2021
(inclusive), there were about 1.1 million admissions and 9200 falls,
which works out to be approximately 0.008 falls per admission.

### References

<div id="refs" class="references csl-bib-body hanging-indent">

<div id="ref-haines2011patient" class="csl-entry">

Haines, Terry P, Anne-Marie Hill, Keith D Hill, Steven McPhail, David
Oliver, Sandra Brauer, Tammy Hoffmann, and Christopher Beer. 2011.
“Patient Education to Prevent Falls Among Older Hospital Inpatients: A
Randomized Controlled Trial.” *Archives of Internal Medicine* 171 (6):
516–24.

</div>

<div id="ref-hill2015fall" class="csl-entry">

Hill, Anne-Marie, Steven M McPhail, Nicholas Waldron, Christopher
Etherton-Beer, Katharine Ingram, Leon Flicker, Max Bulsara, and Terry P
Haines. 2015. “Fall Rates in Hospital Rehabilitation Units After
Individualised Patient and Staff Education Programmes: A Pragmatic,
Stepped-Wedge, Cluster-Randomised Controlled Trial.” *The Lancet* 385
(9987): 2592–99.

</div>

<div id="ref-latimer2013cost" class="csl-entry">

Latimer, Nicholas, Simon Dixon, Amy Kim Drahota, and Martin Severs.
2013. “Cost–Utility Analysis of a Shock-Absorbing Floor Intervention to
Prevent Injuries from Falls in Hospital Wards for Older People.” *Age
and Ageing* 42 (5): 641–45.

</div>

<div id="ref-morello2015extra" class="csl-entry">

Morello, Renata T, Anna L Barker, Jennifer J Watts, Terry Haines, Silva
S Zavarsek, Keith D Hill, Caroline Brand, et al. 2015. “The Extra
Resource Burden of in-Hospital Falls: A Cost of Falls Study.” *Medical
Journal of Australia* 203 (9): 367–67.

</div>

<div id="ref-parsons2022inpatient" class="csl-entry">

Parsons, Rex, Robin D Blythe, Susanna M Cramb, and Steven M McPhail.
2022. “Inpatient Fall Prediction Models: A Scoping Review.”
*Gerontology*, 1–16.

</div>

</div>
