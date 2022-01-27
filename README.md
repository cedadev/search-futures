# search-futures
Future Search Architecture

## Key Repositories and Development Strands

### Indexing

- [Asset Scanner](https://github.com/cedadev/asset-scanner) - Asset scanning framework. Provides the input/output plugins, item-description interface and holds shared utilities.
- [Asset Generator](https://github.com/cedadev/asset-generator) - Converts a stream of URIs (filepaths) into assets. Outputs Asset dictionary and `tuple(<item_id>,<filepath>)`
- [Item Generator](https://github.com/cedadev/item-generator) - Summarises Assets to form Items. Can also run its own processors to enrich the item content.  Input is a stream of `item_id`s and `filepaths`. Outputs `Item` and `tuple(<collection_id>,<filepath>)
- [Colletion Generator](https://github.com/cedadev/collection-generator) - Summarises Items to form Collections. Can also run its own processors to enrich the Collection content. Input is a stream of `collection_id`s and `filepaths`. Outputs `Collections`
- [Item Descriptions](https://github.com/cedadev/item-descriptions) - Configuration files for the indexing workflow. They describe how to construct the assets, items and collections. 
- [Item Descriptions Depoyment](https://breezy.badc.rl.ac.uk/stac/stac-item-descriptions) - Descriptions are also pushed here to build a data container for the indexing process.
- [Asset Scanner Example](https://github.com/cedadev/asset-scanner-example) - Example repo which launches in Binder to demonstrate the indexing workflow.
- [STAC Indexing Deployment](https://breezy.badc.rl.ac.uk/rsmith013/stac-indexer-deploy) -  Deployment of the STAC indexers in Kubernetes.

### API

[Server Implementation]
[Deployment]
Extensions:
- [free-text]
- [context-colletions]
- [asset-search]
- [discoverable-facets]
[Asset Spec]

### UI
[Application]
[Deployment]

### Vocabularies
[Vocabulary Generator]
[Vocabulary API]
[Deployment]

### Upstream Repos to keep an eye on
[stac-fastapi]
[pygeofilter]



NOTE: PlantUML was used to generate diagrams.

## Search API Interfaces and Middleware
![Search API](out/uml/search/Search%20API%20Interfaces%20and%20middleware.png)

## Media Crawler and Ingest
![Search API](out/uml/crawler/Media%20Crawler%20and%20Ingest.png)

## Facet Extraction
![Facet Extraction](out/uml/facet_extraction/facet_extraction.png)
