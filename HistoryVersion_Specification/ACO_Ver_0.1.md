# Alex's Cinematic Ontology Specification 0.1
<!-- omit in toc -->
### Namespace Document 20 May 2021 - _Initial Draft_

**This version:**  
http://alex.myontology.info/spec/20210526.html

**Latest version:**  
http://alex.myontology.info/spec/

**Previous version:**  
None

**Author:**  
[陳澤宇](mailto:alexchen.ms07@nctu.edu.tw), National Yang Ming Chiao Tung University  


**Contributors:**  
Members of NYCU Workshop: [A Computational Journey Towards Humanities and Creativity: Starting from Graphs](http://e.cctcc.art/c1632).
<!-- omit in toc -->
## Abstract
Alex's Cinematic Ontology(ACO) specification describe a way to describe dictionary of named properties and classes related to cinematography, video production and digital imaging technology.

<!-- omit in toc -->
## Table of Contents
[TOC]

## Alex's Cinematic Ontology at a glance

ACO describes cinema items and technologies in a practical manner. The relationship between an item and another item or an item and a technology is described as classes and properties.

The gear-related terms of ACO is based on the open resource of ARRI Group, a Germany company famous for manufactoring cinema gears and making industry standard for movie production. ARRI manufactors cinema camera, lenses, lighting equipment and other accessories, their product has been held as gold standard for movie equipment.

The technology-related terms of ACO is based on standard provided by Society of Motion Picture and Television Engineers(SMPTE) and International Telecommunication Union(ITU). SMPTE and ITU make the most widely recognized standard for digital cinema and broadcasting.

Main MyOntology terms, grouped in categories. (按分類排列，附連結)

- **Fundamental Knowledges** – Fundemental knowledge behind the technology of how cinema equipment works. They are not necessarily directly related to movie production, but understanding them is a huge part of understanding digital imaging process.  
- **Technologies** – Practical skills that are directly related to movie production. The use of technologies is correlated to the skills of cinematographer.
- **Physical Objects** – Tangible objects related to movie production. They might be used on movie set or in the post production processes.

| Fundemental Knowledges  | Technologies | Physical Objects |
| ------------------------- | ---------- | ---------- |
| [`Color Management`](#classa1_1) | [`Exposure`](#preda1_2) | [`Cinema Cameras`](#preda1_2)|
| [`Digial Imaging`](#classa1_2) | [`Resolution`](#preda1_2) |[`Lenses`](#preda1_2)
| [`Image Processing`](#preda1_1)   | [`Codex`](#preda1_2) | [`Support System`](#preda1_2)
| [`Optical Components in Lenses`](#preda1_2)   | [`Picture Setting`](#preda1_2)|[`Motion Control`](#preda1_2)
| [`Camera Sensors`](#preda1_2)              | [`SMPTE Standards`](#preda1_2) | [`Virtual Production`](#preda1_2)
| [`Electronic Components in Lenses`](#preda1_2)             | [`ITU Standards`](#preda1_2) | [`Lighting`](#preda1_2)
| [`Camera Signal Processing`](#preda1_2)| [`Imaging Quality`](#preda1_2)|[`Signal Transmission Devices`](#preda1_2)


### A-Z of ACO terms (current and archaic)

(未來若有改版或淘汰可加註：current and archaic，參考 [foaf:dnaChecksum](http://xmlns.com/foaf/spec/#term_dnaChecksum) )

This is a complete alphabetical index of ACO classes.

* **Classes:** | [`Camera Sensors`](#classa1_1) | [`Camera Signal Processing`](#classa1_2) | [`Cinema Cameras`](#classa1_2) |[`Codex`](#classa1_2) |[`Color Management`](#classa1_2) |[`Digital Imaging`](#classa1_2) |[`Electronic Components in Lenses`](#classa1_2) |[`Exposure`](#classa1_2) |[`Imaging Processing`](#classa1_2) |[`Imaging Quality`](#classa1_2) |[`ITU Standards`](#classa1_2) |[`Lenses`](#classa1_2) |[`Lighting`](#classa1_2) |[`Motion Control`](#classa1_2) |[`Optical Components in Lenses`](#classa1_2) |[`Picture Setting`](#classa1_2) |[`Resolution`](#classa1_2) |[`Signal Transmission Devices`](#classa1_2) |[`SMPTE Standards`](#classa1_2) |[`Support System`](#classa1_2) |[`Virtual Production`](#classa1_2) 

### Example

(to be updated)

```XML
<foaf:Person rdf:about="#danbri" xmlns:foaf="http://xmlns.com/foaf/0.1/">
  <foaf:name>Dan Brickley</foaf:name>
  <foaf:homepage rdf:resource="http://danbri.org/" />
  <foaf:openid rdf:resource="http://danbri.org/" />
  <foaf:img rdf:resource="/images/me.jpg" />
</foaf:Person>
```

## Introduction: MyOntology Basics

Alex's Cinematic Ontology is proposed by Alex Chen, with ultimate goal of standardizing all cinema-realetd data in a Linked Open Data(LOD) format.

### Background

Alex's Cinematic Ontology started as a platform used to organizing Alex Chen's personal experience regarding movie production. As the data complicated, he wish to build an ontology for all digial cinema related knowledge.

### The Basic Idea

In ACO, digital cinema-related knowledge are divided into three catogories: Fundemental Knowledges, Technologies and Physical Objects. The property of one vocabulary may related to another vocabulary, so users of ACO can know the "whole picture" regarding the vocabulary they've chosen.

### What’s ACO for?

ACO is for anyone interested in looking up digital-cinema related term. It can be used as database for digital cinema education. Alex Chen designed ACO with the purpose of education in mind.

### MyOntology cross_reference: Listing Classes and Properties

ACO introduces the following classes

* **Classes:** | [`Camera Sensors`](#classa1_1) | [`Camera Signal Processing`](#classa1_2) | [`Cinema Cameras`](#classa1_2) |[`Codex`](#classa1_2) |[`Color Management`](#classa1_2) |[`Digital Imaging`](#classa1_2) |[`Electronic Components in Lenses`](#classa1_2) |[`Exposure`](#classa1_2) |[`Imaging Processing`](#classa1_2) |[`Imaging Quality`](#classa1_2) |[`ITU Standards`](#classa1_2) |[`Lenses`](#classa1_2) |[`Lighting`](#classa1_2) |[`Motion Control`](#classa1_2) |[`Optical Components in Lenses`](#classa1_2) |[`Picture Setting`](#classa1_2) |[`Resolution`](#classa1_2) |[`Signal Transmission Devices`](#classa1_2) |[`SMPTE Standards`](#classa1_2) |[`Support System`](#classa1_2) |[`Virtual Production`](#classa1_2) 

## Classes and Properties (full detail)

### Classses
<!-- omit in toc -->
#### Camera Sensors
The part of camera which transform light rays into electronic signals

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`CMOS`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`CCD`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |

#### Camera Signal Processing

Knowledge regarding the how camera output image signals.

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`HDMI`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`SDI`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`WiFi`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Ethernet`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |

#### Cinema Cameras

A list of mainstream cinema cameras.

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Arri Alexa mini`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Arri Alexa mini LF`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Canon C200`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Panasonic S1H`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Sony A7SIII`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Blackmagic Pocket Cinema Camera 4K`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Blackmagic Cinema Camera 2.5K`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
#### Codex

A list of codex used for encoding image captured by cameras.

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`H.264`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`H.265`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`ProRes`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`CinemaDNG`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`EXR`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`RAW`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
#### Color Management

The standard used to describe colors in images.

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Color Space`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Gamma`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`White Point`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`CIE Standard`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
#### Digital Imaging

The process of image formed from physical light rays to electronic signals.

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Color Filter Array`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Digial to Analog Conversion`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Color Sampling`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`OETF`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |

#### Electronic Components in Lenses

The electronic components used in modern lenses.

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Focus Motor`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Metadata Recorder`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Image Stabilization System`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
#### Exposure
The setting which affect the brightness of images.

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Iris`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Shutter Angle`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`ISO`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Neutral Density Filter`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
#### Image Processing
The process after image being captured by sensor and before recorded by camera.
| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Debayering`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`EOTF`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Encoding`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Denoising`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |


#### Imaging Quality

The parameters which cause direct effect on image. 

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Resolution`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Dynamic Range`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Latitude`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Framerate`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Date Rate`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |

#### ITU Standards

Standards made by International Telecommunication Union regarding movie production.
| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`ITU 709`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`ITU 2020`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`ITU 1886`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
#### Lenses

A list of commonly used lens sets.

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Zeiss Compact Prime`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Zeiss Ultra Prime`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Zeiss Milvus`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Arri Signature Prime`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Arri Signature Zoom`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Sigma Art`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Canon CN-E`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
#### Lighting

Equipment used to create luminance in movie production.

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`LED Light`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`HMI Light`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Florence Light`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Tungsten Light`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
#### Motion Control

Eletronic systems used to precisely control the physical movement of cameras.

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Gimbal`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Electornic Slider`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`MOCO System`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
#### Optical Component In Lenses

The optical components used in modern lenses.

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Glass`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Coating`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Floating Lens Group`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
#### Picture Setting

The setting of how image is displayed.

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Color Space`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Color Matrix`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Gamma Curve`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Middle Grey`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
#### Resolution

The amount of pixels on an image.

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`8K`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`4K`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Full HD`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`HD`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`CinemaScope`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Academy`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
#### SMPTE Standard

Standards made by Society of Motion Picture and Television Engineers.

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`SMPTE 2084`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`SMPTE 2086`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`SMPTE 2036`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
#### Support System

Equipment used to physically support cameras and lenses.

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Rig`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Tripod`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Crane`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Steadicam`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
#### Virtual Producion

Technologies related to computer graphics in the post production process of movie production.

| Instance Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Cinema4D`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Keying`](#preda1_2) | [`schema:Person`](https://schema.org/Person) `xsd:string` | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |
| [`Projection Tracking`](#preda1_1) | `xsd:string`                                              | Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. |


## External Vocabulary References

The description ACO used mainly referred from open document of cinema equipment companies and internation organizations.

### [ARRI Group](https://www.arri.com/en/)

### [Red Digital Cinema LLC.](https://www.red.com/)

### [Carl Zeiss AG](https://www.zeiss.com/)

### [SMPTE Standard Index](https://www.smpte.org/standards/document-index/st)

### [ITU Telecommunication Standardization Sector](https://www.itu.int/en/ITU-T/Pages/default.aspx)

## Acknowledgments

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. 

Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

## Recent Changes (未來改版時用)
<!-- omit in toc -->
