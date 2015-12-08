# Data in ARIES
## data upload
Data are uploaded [here](https://integratedmodelling.org/collaboration/#/datamanager/upload).
You can then find the "urn" [here](https://integratedmodelling.org/collaboration/#/datamanager/table), when you try editing the layer.

## declare
I am not sure whether declaring is the right term, but the idea is that data in ARIES need to be explained to the system in terms of its ontology. It is this inclusion of the data in the ontology that make the data useable for other models.

### vector data (e.g. shapefile)
In this example I have a shapefile with hydropower reservoirs.

You can declare a local shapefile with:
```
model each vector (file = "somepath/Vannkraft_Magasin.shp")
    named reservoirs as earth:Lake;
```

Or you can upload a shapefile to the server [here](https://integratedmodelling.org/collaboration/#/datamanager/upload), and then use the following code to declare it:
```
model each wfs(urn = "im:bram.vanmoorter:eu.no.landcover:norway_hydropowerreservoirs")
    named reservoirs as earth:Lake;
```


## questions:
how do we include data that are in a database?

