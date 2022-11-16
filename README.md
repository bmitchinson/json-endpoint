# json-endpoint

## Datasets

The following ingestion sources can all be ingested to the this dataset definition:

<details>
  <summary>Dataset</summary>
  
  ```elixir
  %Andi.InputSchemas.Datasets.Dataset{
  __meta__: #Ecto.Schema.Metadata<:loaded, "datasets">,
  access_groups: #Ecto.Association.NotLoaded<association :access_groups is not loaded>,
  business: %Andi.InputSchemas.Datasets.Business{
    __meta__: #Ecto.Schema.Metadata<:loaded, "business">,
    authorEmail: nil,
    authorName: nil,
    benefitRating: 0.0,
    categories: nil,
    conformsToUri: nil,
    contactEmail: "benjamin.mitchinson@accenture.com",
    contactName: "test",
    dataTitle: "xml_example_1",
    dataset: #Ecto.Association.NotLoaded<association :dataset is not loaded>,
    dataset_id: "8f507c6a-ea36-491d-a044-2566e3467a43",
    describedByMimeType: nil,
    describedByUrl: nil,
    description: "test",
    homepage: nil,
    id: "abb90192-7e80-4823-81dc-2caff92efa0b",
    issuedDate: ~D[2022-11-16],
    keywords: [],
    language: "english",
    license: "https://creativecommons.org/licenses/by/4.0/",
    modifiedDate: ~D[2022-11-16],
    orgTitle: "Org1",
    parentDataset: nil,
    publishFrequency: "test",
    referenceUrls: nil,
    rights: nil,
    riskRating: 0.0,
    spatial: nil,
    temporal: nil
  },
  data_dictionaries: #Ecto.Association.NotLoaded<association :data_dictionaries is not loaded>,
  datasetLink: nil,
  dlq_message: nil,
  id: "8f507c6a-ea36-491d-a044-2566e3467a43",
  ingestedTime: ~U[2022-11-16 22:49:13Z],
  owner: %Andi.Schemas.User{
    __meta__: #Ecto.Schema.Metadata<:loaded, "users">,
    access_groups: #Ecto.Association.NotLoaded<association :access_groups is not loaded>,
    datasets: #Ecto.Association.NotLoaded<association :datasets is not loaded>,
    email: "benjamin.mitchinson@accenture.com",
    id: "46fa7eab-2773-4990-b414-7d79512a5562",
    name: "benjamin.mitchinson@accenture.com",
    organizations: #Ecto.Association.NotLoaded<association :organizations is not loaded>,
    subject_id: "auth0|634d86c8c6b9d65e5b0015ad"
  },
  owner_id: "46fa7eab-2773-4990-b414-7d79512a5562",
  submission_status: :published,
  technical: %Andi.InputSchemas.Datasets.Technical{
    __meta__: #Ecto.Schema.Metadata<:loaded, "technical">,
    allow_duplicates: true,
    authBody: %{},
    authBodyEncodeMethod: nil,
    authHeaders: %{},
    authUrl: nil,
    credentials: false,
    dataName: "xml_example_1",
    dataset: #Ecto.Association.NotLoaded<association :dataset is not loaded>,
    dataset_id: "8f507c6a-ea36-491d-a044-2566e3467a43",
    id: "891f7164-1a39-4b29-8d4e-0127302ab2be",
    orgId: "4c70dad2-499d-463e-bfab-69aa91666ff3",
    orgName: "org1",
    private: false,
    protocol: nil,
    schema: [
      %Andi.InputSchemas.Datasets.DataDictionary{
        __meta__: #Ecto.Schema.Metadata<:loaded, "data_dictionary">,
        biased: nil,
        bread_crumb: "name",
        data_dictionary: #Ecto.Association.NotLoaded<association :data_dictionary is not loaded>,
        dataset: #Ecto.Association.NotLoaded<association :dataset is not loaded>,
        dataset_id: "8f507c6a-ea36-491d-a044-2566e3467a43",
        default_offset: nil,
        demographic: nil,
        description: nil,
        format: nil,
        id: "39f42ccc-7662-489e-a780-88b8550e48da",
        ingestion: #Ecto.Association.NotLoaded<association :ingestion is not loaded>,
        ingestion_id: nil,
        itemType: nil,
        masked: nil,
        name: "name",
        parent_id: nil,
        pii: nil,
        rationale: nil,
        selector: nil,
        sequence: 2,
        ...
      }
    ],
    sourceHeaders: [],
    sourceQueryParams: [],
    sourceType: "stream",
    sourceUrl: "N/A",
    systemName: "org1__xml_example_1",
    topLevelSelector: nil
  },
  version: "0.6"
}
  ```
</details>

## Ingestions

<details>
  <summary>XML Test</summary>
  
  ### [Link to xml to ingest](https://github.com/bmitchinson/json-endpoint/blob/main/sample.xml)

  ### Corresponding ingestion definition
  ```elixir
  %Andi.InputSchemas.Ingestion{
  __meta__: #Ecto.Schema.Metadata<:loaded, "ingestions">,
  allow_duplicates: nil,
  cadence: "*/20 * * * * *",
  dataset: #Ecto.Association.NotLoaded<association :dataset is not loaded>,
  extractSteps: [
    %Andi.InputSchemas.Ingestions.ExtractStep{
      __meta__: #Ecto.Schema.Metadata<:loaded, "extract_step">,
      context: %{
        "action" => "GET",
        "body" => "",
        "headers" => [],
        "protocol" => nil,
        "queryParams" => [],
        "url" => "https://raw.githubusercontent.com/bmitchinson/json-endpoint/main/sample.xml"
      },
      id: "4d68738c-b629-4c6e-81c7-3d8d9b117fd7",
      ingestion: #Ecto.Association.NotLoaded<association :ingestion is not loaded>,
      ingestion_id: "3a502098-f40e-4e65-b44f-47a73e1ab008",
      sequence: 2,
      type: "http"
    }
  ],
  id: "3a502098-f40e-4e65-b44f-47a73e1ab008",
  name: "xml_sample_ing_a",
  schema: [
    %Andi.InputSchemas.Datasets.DataDictionary{
      __meta__: #Ecto.Schema.Metadata<:loaded, "data_dictionary">,
      biased: "",
      bread_crumb: "name",
      data_dictionary: #Ecto.Association.NotLoaded<association :data_dictionary is not loaded>,
      dataset: #Ecto.Association.NotLoaded<association :dataset is not loaded>,
      dataset_id: "8f507c6a-ea36-491d-a044-2566e3467a43",
      default_offset: nil,
      demographic: "",
      description: "",
      format: nil,
      id: "b42415b1-194e-497a-905a-e12fa49c0940",
      ingestion: #Ecto.Association.NotLoaded<association :ingestion is not loaded>,
      ingestion_id: "3a502098-f40e-4e65-b44f-47a73e1ab008",
      itemType: nil,
      masked: "",
      name: "name",
      parent_id: nil,
      pii: "",
      rationale: "",
      selector: "//person/firstName/text()",
      sequence: 3,
      subSchema: [],
      technical: #Ecto.Association.NotLoaded<association :technical is not loaded>,
      technical_id: nil,
      type: "string",
      use_default: nil
    }
  ],
  sourceFormat: "text/xml",
  submissionStatus: :published,
  targetDataset: "8f507c6a-ea36-491d-a044-2566e3467a43",
  topLevelSelector: "top/middle/rows/person",
  transformations: []
}
  ```
</details>



Making collapsable headers
```
<details>
  <summary>Click me</summary>
</details>
```
