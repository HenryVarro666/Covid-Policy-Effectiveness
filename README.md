# Studying Effectiveness of Covid Policies 

## Team Members 
- [Samarth Negi](https://github.com/tigboatnc)
- __Ally__
- __Chao Cao__
- __Jinhua Yang__


## BIG PICTURE `sam`
The idea mainly evolved after reading [this](https://coronavirus.jhu.edu/from-our-experts/evaluating-the-effectiveness-of-covid-19-policies-a-q-and-a-with-dr-elizabeth-stuart) article from __JHU__ regarding effectiveness of policies 

FEATURES = Census(Demographic)+ Covid (Covid Specific Demographic) + Policy 

STRUCTURE 
1. Exploration 
2. Processing 
3. Model 


## Running Instructions 
1. __Locally__
    1. Clone the Repository.
    2. Set up the needed python dependencies using the env file [environment.yml](./extras/environment.yml)
        ```bash
        conda install -f environment.yml
        ```
2. Alternatively most notebooks can be viewed here on github. 

## Data Gathering `chao`
>  For the sake of saving time, we are skipping most of the _data gathering_ and _source verification_ as it we feel it is trivial and would like to focus more on the feature engineering and data analytics part. A rough summary can be found [here](./extras/dataacq.md) . 

> Most of the data used in our datasets is api based which allows us to get fresh data and run them through our pipelines with just running the notebooks and replacing the existing data with fresh data. [see here]()

## Notebooks
The following table lists the notebooks in order of work done to shed light on some of the approaches taken. 




### STATE COVID PROFILING `X1`
|Serial|Notebook | `Stage` | `Author` | Description | 
|- |- |- |- |- |
|1|[Case Exploration](./notebooks/case-exploration.ipynb) |`EDA` |`Jinhua` |Getting the state wise covid data in and checking for continuity breaks  |
|2|[Case Visualisation and Metrification](./notebooks/case-visualisation-metrification.ipynb)|`Feature Engineering`|`Samarth` |Finding a good interpolation of daily cases as the raw cases were unusable for prediction |
|3|[Peaks in Cases](./notebooks/case-peaks-in-cases.ipynb) |`Feature Engineering` |`Jinhua` |The final feature (peak times) is calculated in this notebook and some visualisations are created for it -  [see the visualisations here](./outputs/peak_visualisations)|
|4|[Vaccination Data Processing](./notebooks/vaccine-data-process.ipynb) |`Feature Engineering` |`Ally`|This notebook deals with processing the vaccine data and creating a state classification metric from it. |


### STATE DEMOGRAPHIC PROFILING `X2`
|Serial|Notebook | `Stage` | `Author` | Description | 
|- |- |- |- |- |
|5|[Data Scraping](./notebooks/census_scraping.ipynb) | `Acquisition` | `Chao` | This notebook scrapes the census website for one shot data gathering | 



### POLICY `X3`
|Serial|Notebook | `Stage` | `Author` | Description | 
|- |- |- |- |- |
|6|[Policy Exploration Visualized](./notebooks/policy-exploration-visual.ipynb)|`EDA`,`Feature Engineering` |`Ally` |-|
|7|[Policy Exploration Data Extraction](./notebooks/policy-exploration-visual.ipynb)|`Feature Engineering` |`Samarth` |This notebook creates the final outputs for the State Policy Data|

### METRICS FOR EFFECTIVENESS OF A POLICY `Y`
|Serial|Notebook | `Stage` | `Author` | Description | 
|-|- |- |- |- |
|10|[Creating Metrics For Effectiveness](./notebooks/train-finalisation.ipynb) | `Plumbing` `Feature Engineering`| `Samarth` | Description | 


### INSIGHTS 

|Serial|Notebook | `Stage` | `Author` | Description | 
|- |- |- |- |- |
|11|[Correlations in Census Data](./notebooks/census-correlations.ipynb) |`Analytics` |`Jinhua`|This notebook does internal corellation of census data. _not really a pertaining to the overarching idea but interesting_. Essentially  _obviousness is obvious_ |
|12|[Hypothesis Testing : Demographic to State Covid Correlation](./notebooks/h1-kmeans.ipynb) | `Analytics` | `Chao` | This notebook tests the hypothesis : __A states covid response will be dependent on its demographic__ | 
|13 |[MODEL 1](./notebooks/model1.ipynb)|`Analytics` |`Ally` |Random Model 1 |
|14 |[MODEL 2 - __will add this soon__]()|`Analytics` |`Jinhua` |Random Model 2|

### EXTRA - TOOLING 
|Serial|Notebook | `Stage` | `Author` | Description | 
|- |- |- |- |- |
|-1|[State Code - Name Merging]() | `Plumbing` | `Ally` | Description | 
|8|[merger1](./notebooks/merger.ipynb) | `Plumbing` | `Samarth` | Description | 
|9|[merger2](./notebooks/merger-two.ipynb) | `Plumbing` | `Samarth` | Description | 





## Conclusions 