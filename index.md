
<img src="https://avatars.githubusercontent.com/u/30407294" style="width:10em" alt="Profile picture">


## Papers

<div itemscope itemtype="https://schema.org/Person"><a itemprop="sameAs" content="https://orcid.org/0000-0001-7911-1659" href="https://orcid.org/0000-0001-7911-1659" target="orcid.widget" rel="me noopener noreferrer" style="vertical-align:top;"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width:1em;margin-right:.5em;" alt="ORCID iD icon">https://orcid.org/0000-0001-7911-1659</a></div>

<https://scholar.google.com/citations?user=kKonjBYAAAAJ>

Web of Science ResearcherID: ABE-8823-2021



## Letters collected so far

BA MSci MRes MA (Cantab), PhD (Cantab, minor corrections)

## Summary

I recently completed my PhD at the University of Cambridge at the Department of Applied Mathematics and Theoretical Physics, funded through the @ai4er-cdt MRes+PhD program. I passed my viva in January 2026, subject to minor corrections.

My thesis *The Potential Height of Tropical Cyclone Storm Surges* asked what the worst possible hurricane storm surge given a climate is, and how this could be useful for risk assessment and for testing the extreme extrapolation of deep learning surrogates.

I studied Natural Sciences (Physics, BA+MSci) at the University of Cambridge. I am currently an ML researcher at Goldman Sachs in London.


## Blog

- [London has better weather than New York City](https://sdat2.github.io/lon_nyc/) — a data-driven analysis of 20 years of hourly weather records that debunks the "drizzly London" myth.
- [A simple model for upwind sailing](https://sdat2.github.io/sailing-upwind/)just using force diagrams and trigonometry. Was my IB Maths coursework in 2014! Seems to work pretty well.

## Contact
 
Feel free to get in touch. My email address is ${my github handle}g at gmail dot com .


## Research interests

### Extreme extrapolation in ML for natural hazards

ML models for weather and climate [need greater focus on extremes](https://doi.org/10.1088/1748-9326/ac9d4e). A model that works well on average can fail badly on rare events. In SurgeNet I built a fun toy example showing why: a ReLU network is piecewise linear, so it extrapolates beyond physical bounds as a tangent — predicting impossible values. This showed up in practice too: swapping TanH for ReLU in our graph neural network increased extreme test error 5×, while barely affecting average performance. I also explored similar ideas at RMS for winterstorms. Small architectural choices matter a lot at the tails.

### Thermodynamics vs. dynamics in climate projections

Climate models have well-known biases in tropical cyclone frequency, intensity, and seasonality — mostly because they can't resolve the small-scale dynamics of TC genesis and structure at typical ~1° grid spacing. But broad-scale thermodynamic fields like sea surface temperature are much more reliable. My thesis leans into this asymmetry: instead of trusting the TCs that climate models produce directly, we use thermodynamic theory (potential intensity, potential size) applied to the large-scale fields to calculate what the worst possible storm *could* be. These idealised theories make strong assumptions (steady-state Carnot engines, etc.), but they let you sidestep the messy dynamical biases entirely. I think this thermodynamic-first approach — trust the fields climate models are good at, use theory for the rest — is underexplored and could be useful beyond tropical cyclones.

### Physical bounds and tail risk

Many extreme phenomena are bounded — a pandemic can only kill everyone ([Cirillo & Taleb, 2020](https://doi.org/10.1038/s41567-020-0921-x)), and a tropical cyclone can only extract so much energy from the ocean. If you know (or can estimate) that bound, does it actually help with risk estimation? My statistical simulations suggest yes, a lot: knowing the upper bound of storm surge heights reduces uncertainty in the 1-in-100 year return period by roughly 3×, even when the bound itself is imperfect. The improvement is robust to moderate errors and only breaks down if the bound estimate is extremely noisy. This is intuitive — fitting a Weibull-class GEV distribution with a known endpoint is a much better-constrained problem than fitting one without. The open question is whether this translates cleanly into real-world risk management with more complex models, real observations, and non-stationarity from climate change. I think it should, and it's something I'd like to explore further.



## Current projects

*"Finding the potential height of tropical cyclone storm surges in a changing climate using Bayesian optimization"*
Read our preprint <https://doi.org/10.31223/X57T5R> and code <https://github.com/sdat2/worstsurge> ([docs](https://worstsurge.readthedocs.io/en/latest/MAIN_README.html)) to hear about a method for calculating the worst possible storm surge and its benefits!

*SurgeNet*: A spatio-temporal graph neural network for emulating storm surge models. Datasets available on HuggingFace: [train/val/test](https://huggingface.co/datasets/sdat2/surgenet-train), [extreme test](https://huggingface.co/datasets/sdat2/surgenet-test-ph).


## Past projects

- Risk Management Solutions (UK) Ltd.: Deep learning for extreme wind superresolution/downscaling.
- Detecting fronts in the Southern Ocean using different algorithms.
  - <https://os.copernicus.org/preprints/os-2021-40/>
  - <https://doi.org/10.5281/zenodo.4740752>
- Detecting habitat fragmentation using ML algorithms on earth observation products.
  - <https://geograph.readthedocs.io/>
- Using sensitivity analysis on simplified global physical models to understand CMIP biases in the tropics.
  - <https://seager19.readthedocs.io/>
 - Looking at the return periods of storm surges produced by tropical cyclones in climate models.
   - <https://gitlab.com/sdat2/new-orleans>
   - <https://gitlab.com/sdat2/surge>
   - <https://github.com/sdat2/surge>


## Reviews

I have reviewed articles for:

- Journal of Physical Oceanography (JPO) (x1)
- Journal of Advances in Modeling Earth Systems (JAMES) (x1)

I have reviewed abstracts for:

- Climate Informatics 2024 (x2)


## Funding

My PhD was supported by studentship 2413578 from the UKRI Centre for Doctoral Training in Application of Artificial Intelligence to the study of Environmental Risks (grant no. EP/S022961/1). I received funding from the NERC ACSIS project (grant no. NE/N018028/1), and a Natural Environment Research Council (NERC) Research Experience Placement (REP) project funded by the SPITFIRE Doctoral Training Partnership (grant no. NE/S007210/1). I am also grateful for many years of support from Peterhouse.
