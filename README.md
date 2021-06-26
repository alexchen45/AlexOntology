# Alex's Digital Imaging Ontology (formerly known as Alex's Cinematic Ontology)

This project is Alex's term project for the course "A Computational Journey Towards Humanities and Creativity: Starting from Graphs" of National Yang Ming Chiao Tung University.  

Contect of this project included:  
  
1. SPARQL Endpoint (for both human and machine)
2. Specification for Alex's Digital Imaging Ontology 
3. Visualization  

## SPARQL Endpoint for ADIO
ADIO uses blazegraph, you can access the RDF here:

[http://45.79.90.173:9999/sparql](http://45.79.90.173:9999/sparql)

You can also make query via GUI here:

[Blazegraph Workbench](http://45.79.90.173:9999/blazegraph/) 

There we provide some sample code for your query:

To Find all the products in the database that's made by the manufacturer "ARRI":
```SPAQRL
#Find all objects made by ARRI
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX : <http://alexdigitalimagingontology.com/>

SELECT ?s ?m
WHERE {
  ?s :Manufacturer ?m .
  
  FILTER(?m="ARRI")
}
```
![](/img/screenshot1.png)

To Find all the lens of which we can use on a full frame cinema camera:
```SPAQRL
#Find all full frame-compatible lenses
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX : <http://alexdigitalimagingontology.com/>

SELECT ?s
WHERE {
  ?s :FullFrameCompatible ?f .
  
  FILTER(?f=true)
}
```
![](/img/screenshot2.png)

The list goes quite long. If you only wish to know the "Lens Set" that can be used on a full frame camera:
```SPAQRL
#Find all full frame-compatible lens sets
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX : <http://alexdigitalimagingontology.com/>

SELECT DISTINCT ?set
WHERE {
  ?s :FullFrameCompatible ?f ;
     :Set ?set .
  FILTER(?f=true)
}
```
![](/img/screenshot3.png)

Now, what if you want to know all the compatible lenses for each cinema cameras?
```
#All the compatible lenses for each cinema cameras.
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX : <http://alexdigitalimagingontology.com/>

SELECT DISTINCT ?cam ?width ?s1
WHERE {
  ?s1 a :Lens ;
 	:FullFrameCompatible ?f ;
     :S35Compatible ?s35c .
  ?s2 a :CinemaCamera ;
        :Model ?cam ;
        :Sensor ?sensor .
  ?s3 a :CameraSensor ;
        :Width ?width.
  FILTER((?sensor=?s3 && ?width>=36 && ?f=true)||(?sensor=?s3 && ?width<36 && ?s35c=true))
} ORDER BY ASC (?cam)
```
![](/img/screenshot4.png)
This is a little bit more complicated because we need to first check the size of the camera's sensor, then decide if it's compatible with specific lenses.

The .ttl file used for this SPARQL Endpoint can be downloaded [here](/ADIO_turtle.ttl).

## ADIO Specification

Check the Specification for the classes and properties of ADIO for detail information regarding this ontology.

[ADIO Specification 1.0](/ADIO_Specification.md)

Previous version are here (This ontology had been known as Alex's Cinematic Ontology before version 0.3):

[ADIO Specification 0.4](/HistoryVersion_Specification/ADIO_Ver_0.4.md)  
[ACO Specification 0.3](/HistoryVersion_Specification/ACO_Ver_0.3.md)  
[ACO Specification 0.2](/HistoryVersion_Specification/ACO_Ver_0.2.md)  
[ACO Specification 0.1](/HistoryVersion_Specification/ACO_Ver_0.1.md)  

## Visualization

ADIO uses WebVOWL to visualized the ontology.
![](/img/graph.jpg)


To view it:

1. Download [Visualization](/ADIO_Visualization.json) file
2. Open [WebVOWL](http://www.visualdataweb.de/webvowl/)
3. Click on "Ontology" on the bottom bar, and "Select Ontology File", then upload the Visualization file.
![](/img/screenshot5.png)

5. Knock yourself out!
