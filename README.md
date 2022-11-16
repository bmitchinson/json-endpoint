# json-endpoint

## Dataset

The following ingestion sources can all be ingested to a single dataset to demonstrate selectors. The schema of that dataset has one top level string attribute, called "name".

## Ingestions

  #### [Link to xml to ingest](https://github.com/bmitchinson/json-endpoint/blob/main/sample.xml)

  #### Corresponding ingestion definition
  
  - topLevelSelector `top/middle/rows/person`
  - Schema: 1 attribute: 
    - name: `name`
    - type: `string`
    - selector: `//person/firstName/text()`
  
  #### [Link to json (no selector) to ingest](https://github.com/bmitchinson/json-endpoint/blob/main/name.json)
  
  #### Corresponding ingestion definition
  
  - topLevelSelector `{empty}`
  - Schema: 1 attribute: 
    - name: `name`
    - type: `string`
    - selector: `{empty}`

  #### [Link to json (with a selector) to ingest](https://github.com/bmitchinson/json-endpoint/blob/main/nested_name.json)
  
  #### Corresponding ingestion definition
  
  - topLevelSelector `$.sub.path`
  - Schema: 1 attribute: 
    - name: `name`
    - type: `string`
    - selector: `{empty}`
