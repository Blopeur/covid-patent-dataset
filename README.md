# CORONAVIRUS PATENT DATASET 11-04-2020

Free and Open-source Provided by [blopeur LTD.](https://www.blopeur.com).
If you have any question or need help with patent related inquiry, feel free to drop us an email at [info@blopeur.com](mailto:info@blopeur.com)

This repository contains patents datasets related to the human coronaviruses and COVID-19.
It contains a cleaned and extended version of the [coronarovirus datasets](https://about.lens.org/covid-19/) provided by [lens.org](https://www.lens.org).
The `Lens.org` data was extended by running queries against the [public patent datastet available on Google bigquery](https://cloud.google.com/blog/products/gcp/google-patents-public-datasets-connecting-public-paid-and-private-patent-data).

Disclaimer : these collections are based on public dataset and search queries (see below), some manual editing and refining was also used to eliminate clearly irrelevant documents. It is important to keep in mind that these are draft collections and we will continue to refine and update them with each new data release. If you have any specific question, please email [info@blopeur.com](mailto:info@blopeur.com)


Description of the query for each dataset : 
* [Coronavirus-broad-keywords-based-patents.jsonl](Coronavirus-broad-keywords-based-patents.jsonl) : Contains the result for a broad keywords search in the title, claims and abstract for 
    * Coronavirus
    * Severe acute Respiratory syndrome
    * coronaviridae
    * SARS-CoV
    * MERS-CoV
    * COVID 19
    * Wuhan coronavirus
    * 2019-nCoV
    * Middle East respiratory
* [Coronavirus-limited-keywords-based-patents.jsonl](Coronavirus-limited-keywords-based-patents.jsonl) : Contains patents matching the limited keywords search : 
    * SARS
    * severe acute respiratory
    * Middle East respiratory
    * MERS
* [Coronavirus-MERS-patents.jsonl](Coronavirus-MERS-patents.jsonl) : Contains patents matching :
    * MERS
    * Middle East respiratory
* [Coronavirus-SARS-patents.jsonl](Coronavirus-SARS-patents.jsonl) : Contains patents matching :
    * SARS
    * severe acute respiratory
* [Respirators-and-surgical-masks.jsonl](Respirators-and-surgical-masks.jsonl) : Contains patents of the `A62B23\/025*` or `A41d13\/11*` CPC family
* [Ventilators.jsonl](Ventilators.jsonl) : Contains patents of the `A61M16\/*` CPC family 
* [Coronavirus-MERS-diagnosis-patents.jsonl](Coronavirus-MERS-diagnosis-patents.jsonl) : Contains subset of the MERS patents matching : 
    * diagnos* OR detect*
* [Coronavirus-MERS-treatment.jsonl](Coronavirus-MERS-treatment.jsonl) : Contains subset of the MERS patents matching : 
    * antiviral OR vaccin* OR treat*
* [Coronavirus-SARS-diagnosis-patents.jsonl](Coronavirus-SARS-diagnosis-patents.jsonl) : Contains subset of the SARS patents matching : 
    * diagnos* OR detect*
* [Coronavirus-SARS-treatment.jsonl](Coronavirus-SARS-treatment.jsonl) : Contains subset of the SARS patents matching : 
    * antiviral OR vaccin* OR treat*
* [Coronavirus-patents-SARS-MERS.jsonl](Coronavirus-patents-SARS-MERS.jsonl) : Contains patents matching :
    * coronavirus
    * severe acute respiratory
    * Middle East respiratory
* [Coronavirus-patents-SARS-MERS-TAC.jsonl](Coronavirus-patents-SARS-MERS-TAC.jsonl) : Contains patents matching :
    * SARS
    * MERS
    * severe acute respiratory
    * Middle East respiratory
    * Biologicals : 227859 , 228330
* [Coronavirus-CPC-based-patents.jsonl](Coronavirus-CPC-based-patents.jsonl) : Contains patents matching CPC classification :
    * C12N2770/20011*
    * C07K14/165*
    * A61K39/215*
    * G01N2333/165*
* [Coronavirus-declared-patseq-organism.jsonl](Coronavirus-declared-patseq-organism.jsonl) : Contains patents matching the sequence organism taxid : 
    * 227859
    * 228330
    * 693995
    * 277944
    * 11137
    * 1335626


The datasets are in [JSON Lines](http://jsonlines.org/) format and have the following schema : 

```json
[
  {
    "mode": "NULLABLE",
    "name": "nplResolvedCount",
    "type": "INTEGER"
  },
  {
    "mode": "REPEATED",
    "name": "nplResolvedLensIDs",
    "type": "STRING"
  },
  {
    "mode": "REPEATED",
    "name": "nplCitations",
    "type": "STRING"
  },
  {
    "mode": "REPEATED",
    "name": "ipcrClassifications",
    "type": "STRING"
  },
  {
    "mode": "REPEATED",
    "name": "cpcClassifications",
    "type": "STRING"
  },
  {
    "mode": "NULLABLE",
    "name": "familySize",
    "type": "INTEGER"
  },
  {
    "mode": "NULLABLE",
    "name": "citedByPatentCount",
    "type": "INTEGER"
  },
  {
    "fields": [
      {
        "description": "%E4Y-%m-%d",
        "mode": "NULLABLE",
        "name": "executionDate",
        "type": "DATE"
      },
      {
        "mode": "NULLABLE",
        "name": "name",
        "type": "STRING"
      }
    ],
    "mode": "REPEATED",
    "name": "owners",
    "type": "RECORD"
  },
  {
    "mode": "NULLABLE",
    "name": "seqCount",
    "type": "INTEGER"
  },
  {
    "mode": "REPEATED",
    "name": "inventors",
    "type": "STRING"
  },
  {
    "mode": "NULLABLE",
    "name": "filingNumber",
    "type": "STRING"
  },
  {
    "mode": "NULLABLE",
    "name": "title",
    "type": "STRING"
  },
  {
    "description": "%E4Y-%m-%d",
    "mode": "NULLABLE",
    "name": "filingDate",
    "type": "DATE"
  },
  {
    "mode": "REPEATED",
    "name": "usClassifications",
    "type": "STRING"
  },
  {
    "mode": "NULLABLE",
    "name": "url",
    "type": "STRING"
  },
  {
    "mode": "REPEATED",
    "name": "priorityFilingKeysActive",
    "type": "STRING"
  },
  {
    "description": "%E4Y-%m-%d",
    "mode": "NULLABLE",
    "name": "earliestPriorityDate",
    "type": "DATE"
  },
  {
    "description": "%E4Y-%m-%d",
    "mode": "NULLABLE",
    "name": "publicationDate",
    "type": "DATE"
  },
  {
    "mode": "NULLABLE",
    "name": "index",
    "type": "INTEGER"
  },
  {
    "mode": "NULLABLE",
    "name": "simpleFamilySize",
    "type": "INTEGER"
  },
  {
    "mode": "NULLABLE",
    "name": "docType",
    "type": "STRING"
  },
  {
    "mode": "NULLABLE",
    "name": "hasFullText",
    "type": "BOOLEAN"
  },
  {
    "mode": "REPEATED",
    "name": "nplResolvedExternalIDs",
    "type": "STRING"
  },
  {
    "mode": "REPEATED",
    "name": "applicants",
    "type": "STRING"
  },
  {
    "mode": "NULLABLE",
    "name": "displayKey",
    "type": "STRING"
  },
  {
    "mode": "NULLABLE",
    "name": "kindCode",
    "type": "STRING"
  },
  {
    "mode": "NULLABLE",
    "name": "nplCitationCount",
    "type": "INTEGER"
  },
  {
    "mode": "NULLABLE",
    "name": "lensId",
    "type": "STRING"
  },
  {
    "mode": "NULLABLE",
    "name": "publicationKey",
    "type": "STRING"
  },
  {
    "mode": "NULLABLE",
    "name": "jurisdiction",
    "type": "STRING"
  }
]
```