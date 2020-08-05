# COVID-19 Literature Search
Methodology for automated COVID-19 literature search to identify AI-related articles.


## The CORD-19 dataset

We retrieve articles from the CORD-19 open research dataset, available at: 

> COVID-19 Open Research Dataset (CORD-19). 2020. Version 2020-08-04. Retrieved from https://www.semanticscholar.org/cord19/. Accessed 2020-08-04. doi:10.5281/zenodo.3715505

The query used by CORD-19 to retrieve results is as follows:

    "COVID-19"[All Fields] OR ("coronavirus"[MeSH Terms] OR "coronavirus"[All Fields]) OR 
    "Corona virus"[All Fields] OR "2019-nCoV"[All Fields] OR "SARS-CoV"[All Fields] OR 
    "MERS-CoV"[All Fields] OR "Severe Acute Respiratory Syndrome"[All Fields] OR 
    "Middle East Respiratory Syndrome"[All Fields]
    
The latest metadataset can be accessed [here](https://ai2-semanticscholar-cord-19.s3-us-west-2.amazonaws.com/latest/metadata.csv). A historical dataset archive is available [here](https://ai2-semanticscholar-cord-19.s3-us-west-2.amazonaws.com/historical_releases.html). The preprint describing the dataset is available [here](https://www.semanticscholar.org/paper/CORD-19%3A-The-Covid-19-Open-Research-Dataset-Wang-Lo/bc411487f305e451d7485e53202ec241fcc97d3b).

## Filtering and results

We kept only articles containing either a title and an abstract, and only articles with a publication year of 2019 or 2020. We removed articles with a duplicate dataset ID, SHAm DOI, PubMed ID, URL, S2 ID, Arxiv ID, PMC ID, or WHO Covidence ID (these fields are described [here](https://github.com/allenai/cord19)). For the time period between 1st January 2020 and 1st August 2020, the search retrieved 36,292 COVID-related articles and 1,305 AI-related articles. 

![literature over time](automated_lit_review_updated.png)
