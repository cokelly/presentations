---
marp: true
title: Considerations on the spatial and temporal spread of infectious pathogens in the COVID-19 era
description: Presentation on issues related to the spatial and temporal spread of infectious pathogens in the COVID-19 era
theme: default
paginate: false
size: 4K
---

# Considerations on the spatial and temporal spread of infectious pathogens in the COVID-19 era

5 November 2021

Julien Arino ([Julien.Arino@umanitoba.ca](mailto:Julien.Arino@umanitoba.ca))

Department of Mathematics & Data Science Nexus
University of Manitoba*

<div style = "font-size:18px; margin-top:-10px; padding-bottom:30px;"></div>

Canadian Centre for Disease Modelling
Canadian COVID-19 Mathematical Modelling Task Force
NSERC-PHAC EID Modelling Consortium (CANMOD, MfPH, OMNI/RÉUNIS)

<div style = "text-align: justify; position: relative; bottom: -8%; font-size:18px;">
The University of Manitoba campuses are located on original lands of Anishinaabeg, Cree, Oji-Cree, Dakota and Dene peoples, and on the homeland of the Métis Nation.

We respect the Treaties that were made on these territories, we acknowledge the harms and mistakes of the past, and we dedicate ourselves to move forward in partnership with Indigenous communities in a spirit of reconciliation and collaboration.</div>

---

# <!-- fit --> Pathogens have been mobile for a while

<!--<div style = "text-align: justify">-->
It first began, it is said, in the parts of **Ethiopia** above Egypt, and thence descended into **Egypt** and **Libya** and into most of the King's country [**Persia**]. Suddenly falling upon Athens, it first attacked the population in **Piraeus** [..] and afterwards appeared in the **upper city**, when the deaths became much more frequent.
<!--</div>-->

<div style = "text-align: right; position: relative; bottom: -15%; ">
Thucydides (c. 460 BCE - c. 395 BCE)

History of the Peloponnesian War</div>

![bg 90% right:30%](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/various/Thucydides-bust-noBG.png)

--- 

# Outline
- Human habitat fragmentation, mobility and the spread of infectious diseases
- The first wave of COVID-19
- Case importations
- Spread of SARS-CoV-2 variants
- Role of transport restrictions
- Role of quarantine
- Lessons learned and key knowledge gaps

---

# Human habitat fragmentation, mobility and the spread of infectious diseases

---

# <!-- fit -->The human world is fragmented not only because of geography

- Political divisions (jurisdictions): nation groups (e.g., EU), nations, provinces/states, regions, counties, cities..
- Travel between jurisdictions can be complicated or impossible
- Data is integrated at the jurisdicional level
- Policy is decided at the jurisdictional level
- Long range mobility is a bottom$\to$top$\to$top$\to$bottom process

---

![bg contain](https://www.cmaj.ca/content/cmaj/182/6/579/F2.large.jpg)

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/transportation/world_graph-degree.png)

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/transportation/passengers_transported_worldwide.png)

---

# <!-- fit -->Mobility is complicated but determinant in disease spatialisation

- Multiple modalities: foot, bicycle, personal vehicle, bus, train, boat, airplane
- Various durations: trip to the corner shop $\neq$ commuting $\neq$ multi-day trip for work or leisure $\neq$ relocation, immigration or refuge seeking
- Volumes are hard to fathom

And yet **mobility drives spatio-temporal spread**:
- Black Death 1347-1353 arrived in Europe and spread following trade routes
- SARS-CoV-1 spread out of HKG following the GATN
- Khan, Arino, Hu *et al*, Spread of a novel influenza A (H1N1) virus via global airline transportation, *New England Journal of Medicine* (2009)
</div>

---
<div style = "position: relative; top: -55%; padding-bottom:60px; font-size:40px">
The spread process in a jurisdiction-based world
</div>

![bg 95%](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/importations/importation_process3.png)

---

# <!-- fit -->The first wave of COVID-19

<div style = "position: relative; bottom: -40%; font-size:18px;">
J. Arino. Describing, modelling and forecasting the spatial and temporal spread of COVID-19 - A short review. To appear in Fields Institute Communications.</div>

---

# Amplification in Wuhan (Hubei province)

- Details of emergence and precise timeline before amplification started unknown
- Amplification in Wuhan
	- Cluster of pneumonia cases mostly related to the Huanan Seafood Market
	- 27 December 2019: first report to local government
	- 31 December 2019: publication
	- 8 January 2020: identification of SARS-CoV-2 as causative agent
-  $\sim$ 23 January 2020: lockdown Wuhan and Hubei province + face mask mandates

By 29 January, virus was found in all provinces of mainland China

---

# First detections outside China

<style scoped>
table {
    height: 100%;
    width: 100%;
    font-size: 20px;
}
</style>

| Date | Location | Note |
|------|----------|------|
| 13 Jan. | Thailand | Arrived 8 Jan. |
| 16 Jan. | Japan | Arrived 6 Jan. |
| 20 Jan. | Republic of Korea | Airport detected on 19 Jan. |
| 20 Jan. | USA | Arrived Jan. 15 |
| 23 Jan. | Nepal | Arrived 13 Jan. |
| 23 Jan. | Singapore | Arrived 20 Jan. |
| 24 Jan. | France | Arrived 22 Jan. |
| 24 Jan. | Vietnam | Arrived 13 Jan. |
| 25 Jan. | Australia | Arrived 19 Jan. |
| 25 Jan. | Malaysia | Arrived 24 Jan. |

---

# Caveat : evidence of earlier spread

- Report to Wuhan authorities on 27 December 2019
- First export detections in Thailand and Japan on 13 and 16 January 2020 (with actual importations on 8 and 6 January)

$\implies$ amplification must have been occuring for a while longer

- France: sample taken from 42-year-old male (last foreign travel to Algeria in August 2019) who presented to ICU on 27 December 2019
- Retrospective studies in United Kingdom and Italy also showed undetected COVID-19 cases in prepandemic period

---

# Untangling the first case issue

- Robert, Rossman & Jaric. Dating first cases of COVID-19. *PLoS Pathogens* (2021). Find likely timing of first case of COVID-19 in China as November 17 (95% CI October 4)
- Pekar, Worobey, Moshiri, Scheffler & Wertheim. Timing the SARS-CoV-2 index case in Hubei province. *Science* (2021). Period between mid-October and mid-November 2019 is plausible interval when the first case of SARS-CoV-2 emerged in Hubei province.

Important when trying to understand global spread, so let me illustrate with the model I used (J. Arino & S. Portet. A simple model for COVID-19. *Infectious Disease Modelling* 2020) [taking into account model evolution since]

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/flow-diagrams/figure_SLDURM_base_model_with_different_epsilon_and_infectious_compartments.png)

---

# <!-- fit -->Back-calculating the start of spread (example of China)

Cumulative confirmed case counts in China as reported to WHO was $c=547$ cases on $t_c=\textrm{2020-01-22}$

Let $u$ be a point in parameter space. Solve ODE numerically over $[0,t]$, with $S(0)$ the population of China, $L_1(0)=1$ and other state variables 0. This gives a solution $x(t,t_0=0,u)$. Extracting $L_2(t,t_0=0,u)$ from this solution, obtain cumulative number of new detections as
$$
C(t) = \int_{t_0=0}^{t} p\varepsilon L_2(s,t_0,u)\ ds
$$
Let $t^*$ be s.t. $C(t^*)=547$; then $t_i=\textrm{2020-01-22}-t^*$

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/importations/start_time_vs_R0_and_p.png)

---

- For SARS-CoV-1 (2003), the point of introduction on the GATN is known with certainty (Metropole Hotel, HKG, 2003-02-21)
- For SARS-CoV-2, uncertainty remains and will probably never be lifted


Back to the spatio-temporal spread of the **detected** first wave..


---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/sars-cov-2/CT_extent_2020-07-30.png)

---

# <!-- fit -->Transmission within national jurisdictions was heterogeneous

Moving from ISO-3166-3 (nation or territory) level to smaller sub-national jurisdictions, the picture is more contrasted

Next slide: Example of activation of North American health regions/municipios/counties

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/sars-cov-2/pct_active_21days_with_pct_activations_zoom.png)

---

<video controls autoplay loop width="100%">
<source src="https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/sars-cov-2/USA_incidence.mp4" type="video/mp4">
</video>

---

# <!-- fit --> Case importations


<div style = "position: relative; bottom: -30%; font-size:18px;">
J. Arino & S. Portet. A simple model for COVID-19. Infectious Disease Modelling, 2020

J. Arino, N. Bajeux, S. Portet & J. Watmough. Quarantine and the risk of COVID-19 importation. Epidemiology & Infection, 2020
</div>

---

# Importations

- In Ecology, importations are called *introductions* and have been studied for a while, because they are one of the drivers of evolution and, more recently, because of *invasive species*

- An importation occurs when an individual who acquired the infection in a jurisdiction makes their way to another jurisdiction while still infected with the disease

- Geographies greatly influence reasoning
	- At the country level, importations quickly become less relevant
	- Consider an isolated location of 500 people.. disease may become extinct then be reimported

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/sars-cov-2/pct_active_21days_with_pct_activations.png)

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/importations/figure_variant_importation_base_model_with_stimulations_noQ.png)

---

![bg 98%](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/importations/variant_noImport_increasingImport.png)

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/importations/successful_attack_rate.png)

---

# <!-- fit -->Spread of SARS-CoV-2 variants

<div style = "position: relative; bottom: -35%; font-size:18px;">
J. Arino, P.-Y. Boëlle, E.M. Milliken & S. Portet. Risk of COVID-19 variant importation - How useful are travel control measures? Infectious Disease Modelling, 2021

S.P Otto, T. Day, J. Arino, C. Colijn *et al*. The origins and potential future of SARS-CoV-2 variants of concern in the evolving COVID-19 pandemic. Current Biology, 2021
</div>

---

# <!-- fit --> Understanding variant dynamics and how to control it

- Suppose a *resident variant* is propagating in a population, say, the original wild type or, now, B.1.1.7
- A *novel variant* comes along, say B.1.617.2 (SARS-CoV-2 Delta) that is more transmissible

**Q:**

- How long until novel replaces resident variant in terms of propagation?
- What role do importations play in this?
- How does one diminish role of importations and how useful are measures used to do so?

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/sars-cov-2/gisaid_variants_2021-09-21_Europe.png)

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/sars-cov-2/gisaid_variants_2021-09-21_mixed.png)

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/flow-diagrams/figure_variant_no_importation_1patch.png)

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/importations/new_variant_vs_resident_variant.jpg)

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/flow-diagrams/figure_variant_importation_1patch_simplified.png)

---

![bg 98%](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/importations/importation_vs_community_new_variant_means_withInset.png)

--- 

# Measures to control spatial spread

- Almost exclusively attacked from the perspective of would-be importer

In practice:
- Travel interruptions
- Quarantine
---

# <!-- fit -->Role of transport restrictions

<div style = "position: relative; bottom: -35%; font-size:18px;">
J. Arino, P.-Y. Boëlle, E.M. Milliken & S. Portet. Risk of COVID-19 variant importation - How useful are travel control measures? Infectious Disease Modelling, 2021
</div>

---

<div style = "position: relative; bottom: -55%; left: 15%; font-size:38px; color: black;">Mur de la Peste in Cabrières-d’Avignon</div>

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/epidemio/Cabrières-d'Avignon_902.jpg)

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/epidemio/peste_Provence.png)

---

# Interruption of travel 

<style scoped>
table {
    height: 100%;
    width: 100%;
    font-size: 23px;
}
</style>

|Country          |Date travel suspension |Date first case |
|:----------------|:-----------------|:----------|
|Seychelles       |2020-03-03        |2020-03-14 |
|El Salvador      |2020-03-17        |2020-03-18 |
|Cape Verde       |2020-03-17        |2020-03-20 |
|Sudan            |2020-03-17        |2020-04-05 |
|Marshall Islands |2020-04-22        |2020-10-29 |
|Vanuatu          |2020-03-20        |2020-11-11 |
|North Korea      |2020-01-21        |Unreported |
|Turkmenistan     |2020-03-20        |Unreported |
|Tuvalu           |2020-03-26        |           |

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/flow-diagrams/figure_variant_importation_1patch_simplified.png)

---

![bg 98%](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/importations/importation_vs_community_new_variant_means_withInset.png)

---
<div style = "position: relative; top: -55%; font-size:40px">
Variant importation in a metapopulation model
</div>

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/importations/exporter_importer_panel_zoom.png)

<div style = "position: relative; bottom: -45%; font-size:20px">
Left: low movement rate. Right: higher movement rate
</div>

---

# <!-- fit --> Effect of quarantine

<div style = "position: relative; bottom: -35%; font-size:18px;">
J. Arino, N. Bajeux, S. Portet & J. Watmough. Quarantine and the risk of COVID-19 importation. Epidemiology & Infection, 2020

J. Arino, P.-Y. Boëlle, E.M. Milliken & S. Portet. Risk of COVID-19 variant importation - How useful are travel control measures? Infectious Disease Modelling, 2021
</div>

---

# Quarantine $\neq$ Isolation

- *Quarantine* is indiscriminate and applies to all incoming flux
- *Isolation* is imposed to known or suspected cases and known contacts
- First used in (the lazzarettos of) Dubrovnik in 1377
- Name comes from Venitian *quarantena*

---

<div style = "position: relative; bottom: -55%; left: 5%; font-size:38px; color: black;">Lazzaretto vecchio</div>

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/epidemio/Lazzaretto_Vecchio-good_view.jpg)

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/flow-diagrams/figure_SLDURM_importation_base_withQcompartments.png)

---

<div style="width:100%; height:100%">
  <iframe src="https://daytah-or-dahtah.ovh:3838/Q_calculator_updated/" style="position:absolute; top:0px; left:0px; 
  width:100%; height:100%; border: none; overflow: hidden;"></iframe>
</div>

--- 

# Effect of quarantine on importation rates

$1/\lambda$ the mean time between case importations, $1/\lambda_q$ the mean quarantine-regulated time between case importations, $c$ the efficacy of quarantine (in \%). Then
$$
\lambda_q = 
(100-c)\times
\lambda
$$
Suppose $1/\lambda=$ 5 days and efficacy of quarantine is 90\% at 7 days and 98\% at 14 days, respectively

Then $1/\lambda_q=$ 50 and 250 days, respectively

---

# <!--- fit ---> Lessons learned & key questions/knowledge gaps

---

# Lessons learned

- Airport screening sometimes worked to detect the first imports
- Travel interruptions work .. sometimes (e.g., ISL, NZL, CAN-NL)
- Travel interruptions often do not work (e.g., world $\setminus$ very few)
- Governments like travel interruptions regardless
- Quarantine seems to work quite well but needs to be applied homogeneously
- Open Data has finally landed in public health. Still some issues (e.g., Canadian data), but we're moving in the right direction. Also saw emergence of scientist/journalistic/citizen data collection and dissemination initiatives

---

# Key questions/knowledge gaps

- How to get governments to understand that a pandemic is a **global** phenomenon with **local** "phenotypes", so that uncoordinated unilateral travel policies have virtually no chance of success (*treat the symtoms, not the cause*)
- How to apprehend/model the absolutely colossal amount of mobility taking place and the not less consequent variety of transport modalities and purposes 
- What are the necessary conditions for travel interruptions to work?
- Because of scapegoating, the borders were closed *in theory*. However, because of .. real life, they were not *in practice*. How closed is closed? 

---

# Arrival into CAN from 2020-04-01 to 2021-03-31

(border was "closed")

|Traveller characteristics      | Total       |
|:------------------------------|------------:|
|Total non-resident travellers  |    1,491,233|
|Total Canadian residents       |    3,653,592|
|Total other travellers         |    5,963,285|
|Total international travellers |   11,108,110|

80/100K/day on average (678/100K/day 2019-04 $\to$ 2020-03)

---

# Key questions/knowledge gaps (cont.)

- Effect of heterogeity of vaccination methods/protocols (vaccine type/number of doses/ages)
- What is the effect of local vaccine uptake discrepancies?
- Variants emerge typically in high propagation areas. How will the vaccine divide play into this?

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/sars-cov-2/MB_vacc_2021-09-20.png)

---

![bg contain](https://raw.githubusercontent.com/julien-arino/presentations/main/FIGS/sars-cov-2/share-people-fully-vaccinated-covid.png)

---

# In conclusion

Space is a fundamental component of the epidemic spread process and **cannot** be ignored, both in modelling **and** in public health decision making

---

# <!-- fit --> Merci / Miigwech / Thank you