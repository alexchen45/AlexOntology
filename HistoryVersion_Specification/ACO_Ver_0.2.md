# Alex's Cinematic Ontology Specification 0.2
<!-- omit in toc -->
### Namespace Document 01 June 2021 - _Second Draft_

**This version:**  
http://alex.myontology.info/spec/20210601.html

**Latest version:**  
http://alex.myontology.info/spec/

**Previous version:**  
http://alex.myontology.info/spec/20210526.html

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
|[`CameraSensor`](####CameraSensor)| [`Codec`](####Codec) | [`CinemaCamera`](####CinemaCamera)|
| [`CameraSignalProcessing`](####CameraSignalProcessing)|[`Resolution`](####Resolution) |[`Footage`](####Footage)
| [`ColorFilterArray`](####ColorFilterArray)  |  [`PictureSetting`](####PictureSetting) | [`Lens`](####Lens)
| | [`ColorSpace`](####ColorSpace) |[`LensMount`](####LensMount)
|| [`Gamma`](####Gamma) |[`Lighting`](####Lighting)



### A-Z of ACO terms (current and archaic)


This is a complete alphabetical index of ACO classes.

* **Classes:**  [`CameraSensor`](####CameraSensor)| [`CameraSignalProcessing`](####CameraSignalProcessing)| [`CinemaCamera`](####CinemaCamera)| [`Codec`](####Codec)| [`ColorFilterArray`](####ColorFilterArray)| [`ColorSpace`](####ColorSpace)| [`Footage`](####Footage)| [`Gamma`](####Gamma)| [`Lens`](####Lens)| [`LensMount`](####LensMount)| [`Lighting`](####Lighting)|  [`PictureSetting`](####PictureSetting)｜[`Resolution`](####Resolution) 

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

* **Classes:**  [`CameraSensor`](####CameraSensor)| [`CameraSignalProcessing`](####CameraSignalProcessing)| [`CinemaCamera`](####CinemaCamera)| [`Codec`](####Codec)| [`ColorFilterArray`](####ColorFilterArray)| [`ColorSpace`](####ColorSpace)| [`Footage`](####Footage)| [`Gamma`](####Gamma)| [`Lens`](####Lens)| [`LensMount`](####LensMount)| [`Lighting`](####Lighting)| [`PictureSetting`](####PictureSetting)｜ [`Resolution`](####Resolution) 
* **Properties:**  [`AutoFocus`](####AutoFocus)|[`BitDepth`](####BitDepth)|[`BlueRatio`](####BlueRatio)|[`Codec`](####Codec)|[`ColorSampling`](####ColorSampling)|[`ColorTemp`](####ColorTemp)|[`DataRate`](####DataRate)|[`Diameter`](####Diameter)|[`DynamicRange`](####DynamicRange)|[`FlangeDistance`](####FlangeDistance)|[`Framerate`](####Framerate)|[`FrontDiameter`](####FrontDiameter)|[`FullFrameCapable`](####FullFrameCapable)|[`FunctionType`](####FunctionType)|[`Gamma`](####Gamma)|[`GreyLevel`](####GreyLevel)|[`HDR`](####HDR)|[`Height`](####Height)|[`IlluminationType`](####IlluminationType)|[`ImageCircle`](####ImageCircle)|[`LensMount`](####LensMount)|[`LightSource`](####LightSource)|[`Luminance`](####Luminance)|[`MagifyingRatio`](####MagifyingRatio)|[`Manufacturer`](####Manufacturer)|[`MaxAperture`](####MaxAperture)|[`MaxDataRate`](####MaxDataRate)|[`MaxFocalLength`](####MaxFocalLength)|[`MaxFramerate`](####MaxFramerate)|[`MaxResolutionFPS`](####MaxResolutionFPS)|[`MinFocalLength`](####MinFocalLength)|[`Model`](####Model)|[`MountType`](####MountType)|[`Name`](####Name)|[`NativeISO`](####NativeISO)|[`PhysicalMedium`](####PhysicalMedium)|[`ProtocolType`](####ProtocolType)|[`RedRatio`](####RedRatio)|[`ReleaseDate`](####ReleaseDate)|[`Resolution`](####Resolution)|[`S35Capable`](####S35Capable)|[`SignalProcessingType`](####SignalProcessingType)|[`Standard`](####Standard)|[`TypeName`](####TypeName)|[`Wattage`](####Wattage)|[`WhitePoint`](####WhitePoint)|[`Width`](####Width)|[`Zoom`](####Zoom)

## Classes and Properties (full detail)

### Classses
<!-- omit in toc -->
#### CameraSensor
The part of camera which transform light rays into electronic signals.

| Property Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Manufacturer`](#preda1_1) | `xsd:string` | The company making the sensor. |
| [`Model`](#preda1_1) | `xsd:string` | The specific model of the sensor. |
| [`IlluminationType`](#preda1_1) | `xsd:string` | How sensor surface recieve lumination. |
| [`Width`](#preda1_1) | `xsd:int` | The physical width of sensor in millimeter. |
| [`Height`](#preda1_1) | `xsd:int` | The physical height of sensor in millimeter. |
| [`ColorFilterArray`](####ColorFilterArray) | `ACO:ColorFilterArray` | Filter in front of the sensor which generates colors. |
| [`Resolution`](####Resolution) | `ACO:Resolution` | Pixel count of the image.  |

#### CameraSignalProcessing

Knowledge regarding the how camera output image signals.

| Property Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`ProtocolType`](#preda1_1) | `xsd:string` | The type of protocol of which camera use to transmit image signal. |
| [`MaxResolutionFPS`](#preda1_1) | `xsd:string` | Highest possible frame per second and the highest possible resolution. |
| [`PhysicalMedium`](#preda1_1) | `xsd:string` | Physical medium on which the signal is carried. |

#### CinemaCamera

A list of mainstream cinema cameras.

| Property Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Manufacturer`](#preda1_1) | `xsd:string` | The company making the camera. |
| [`Model`](#preda1_1) | `xsd:string` | The specific model of the camera. |
| [`ReleaseDate`](#preda1_1) | `xsd:date` | The date on which camera is being released. |
| [`Sensor`](####Sensor) | `ACO:CameraSensor` | The part of camera which transform light rays into electronic signals. |
| [`SignalProcessingType`](####CameraSignalProcessing) | `ACO:CameraSignalProcessing` | Knowledge regarding the how camera output image signals. |
| [`MaxFramerate`](#preda1_1) | `xsd:int` | Max possible frame per second recorded with the maxium resolution. |
| [`MaxDataRate`](#preda1_1) | `xsd:int` | Maxium possible data rate of the image recorded. |
| [`Codec`](####Codec) | `ACO:Codec` | The method of which image is being recorded and encoded as digital files. |
| [`LensMount`](####LensMount) | `ACO:LensMount` | The mount connecting cameras and lenses. |
| [`NativeISO`](#preda1_1) | `xsd:int` | Base ISO of which the camera has maximum dynamic range. |
| [`DynamicRange`](#preda1_1) | `xsd:int` | Range of luminance of which the camera is capable of recording.(in stops) |
| [`ColorSpace`](#ColorSpace) | `ACO:ColorSpace` | The volumn of color of which the image is capable of displaying. |
| [`Gamma`](#Gamma) | `ACO:Gamma` | The way luminance in real world converted to luminance level on the image. |

#### Resolution
Pixel count of the image.

| Property Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Name`](#preda1_1) | `xsd:string` | Commonly known name for the resolution. |
| [`Standard`](#preda1_1) | `xsd:string` | Standard used to define the resolution. |
| [`Width`](#preda1_1) | `xsd:int` | Number of pixels on the width of the image. |
| [`Height`](#preda1_1) | `xsd:int` | Number of pixels on the height of the image. |


#### Codec

A list of formats used for encoding image captured by cameras.

| Property Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Resolution`](####Resolution) | `ACO:Resolution` | Pixel count of the image. |
| [`DataRate`](#preda1_1) | `xsd:int` | Size of the image recorded per second(In Magebits per second). |
| [`BitDepth`](#preda1_1) | `xsd:int` | Number of bits used to record single color channel. |
| [`ColorSampling`](#preda1_1) | `xsd:string` | The method of which color is being sampled. |

#### ColorFilterArray
Filter in front of the sensor which generates colors.

| Property Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`TypeName`](#preda1_1) | `xsd:string` | Name of the type of CFA. |
| [`RedRatio`](#preda1_1) | `xsd:float` | Ratio of red signal collected by the sensor.|
| [`GreenRatio`](#preda1_1) | `xsd:float` | Ratio of green signal collected by the sensor. |
| [`BlueRatio`](#preda1_1) | `xsd:float` | Ratio of blue signal collected by the sensor. |

#### ColorSpace
The volumn of color of which the image is capable of displaying. Also known as color gamut.

| Property Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Name`](#preda1_1) | `xsd:string` | Name of the color space. |
| [`HDR`](#preda1_1) | `xsd:boolean` | If the color space is capable of displaying HDR content. |
| [`Standard`](#preda1_1) | `xsd:string` | Standard used to define the color space. |
| [`WhitePoint`](#preda1_1) | `xsd:string` | Definition of white in this color space. |


#### Gamma
The way luminance in real world converted to luminance level on the image. 

| Property Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`FunctionType`](#preda1_1) | `xsd:string` | Type of mathematic function of this gamma. |
| [`HDR`](#preda1_1) | `xsd:boolean` | If the gamma is capable of displaying HDR content. |
| [`DynamicRange`](#preda1_1) | `xsd:int` | Range of luminance of which the gamma is capable of recording.(in stops) |
| [`GreyLevel`](#preda1_1) | `xsd:int` | The level on the gamma curve of which 18% grey is mapped on. |

#### PictureSetting
The setting camera use to record image

| Property Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Gamma`](####Gamma) | `ACO:Gamma` | The way luminance in real world converted to luminance level on the image.  |
| [`ColorSpace`](####ColorSpace) | `ACO:ColorSpace` | The volumn of color of which the image is capable of displaying. Also known as color gamut. |
| [`Codec`](#Codec) | `ACO:Codec` | A list of formats used for encoding image captured by cameras. |
| [`Resolution`](####Resolution) | `ACO:Resolution` | Pixel count of the image. |

#### Footage

The parameters which cause direct effect on image. 

| Property Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Resolution`](####Resolution) | `ACO:Resolution` | Pixel count of the image. |
| [`Framerate`](#preda1_1) | `xsd:float` | Frame recorded per second. |
| [`ColorSpace`](####ColorSpace) | `ACO:ColorSpace` | The volumn of color of which the image is capable of displaying. Also known as color gamut. |
| [`Gamma`](####Gamma) | `ACO:Gamma` | The way luminance in real world converted to luminance level on the image. |
| [`Codec`](####Codec) | `ACO:Codec` | A list of formats used for encoding image. |
| [`DataRate`](#preda1_1) | `xsd:int` | Size of the image recorded per second(In Magebits per second). |

#### Lens

Component used to mapped light from real world on an image surface.

| Property Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Manufacturer`](#preda1_1) | `xsd:string` | The company making the sensor. |
| [`Name`](#preda1_1) | `xsd:string` | Name of the lens. |
| [`Zoom`](#preda1_1) | `xsd:boolean` | If the lens has the ability of changing focal length. |
| [`FullFrameCapable`](#preda1_1) | `xsd:boolean` | If the lens is capable of recording image for a full frame sensor. |
| [`S35Capable`](#preda1_1) | `xsd:boolean` |If the lens is capable of recording image for a S35 sensor. |
| [`MaxFocalLength`](#preda1_1) | `xsd:int` | Maximum possible focal length of the lens in millimeter. |
| [`MinFocalLength`](#preda1_1) | `xsd:int` | Maximum possible focal length of the lens in millimeter. |
| [`FrontDiameter`](#preda1_1) | `xsd:int` | Size of the filter ring diameter of the lens in millimeter. |
| [`MagifyingRatio`](#preda1_1) | `xsd:float` | Ratio of the size of real world object and the size it appears on the image through lens. |
| [`ImageCircle`](#preda1_1) | `xsd:float` | Diameter of the imaging circle in millimeter. |
| [`MaxAperture`](#preda1_1) | `xsd:float` | Maximum possible size of the hole on the lens through which light goes in (as F/MaxAperture). |
| [`AutoFocus`](#preda1_1) | `xsd:boolean` | If the lens is capable of automaticly focusing. |
| [`MountType`](####LensMount) | `xsd:string` | The mount connecting cameras and lenses. |

#### Lighting

Equipment used to create luminance in movie production.

| Property Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Manufacturer`](#preda1_1) | `xsd:string` | The company making the light. |
| [`Name`](#preda1_1) | `xsd:string` | Name of the light. |
| [`LightSource`](#preda1_1) | `xsd:string` | The source of generation of light |
| [`Luminance`](#preda1_1) | `xsd:int` | Luminance level the light is able to generate |
| [`Wattage`](#preda1_1) | `xsd:int` | Power consumed by the light. |
| [`ColorTemp`](#preda1_1) | `xsd:int` | Color temperature of the light. |

#### LensMount
The mount connecting cameras and lenses.

| Property Name           | Expected Type                                             | Description                                                                                                                 |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [`Manufacturer`](#preda1_1) | `xsd:string` | The company designing the mount. |
| [`TypeName`](#preda1_1) | `xsd:string` | Type of the lens mount. |
| [`Diameter`](#preda1_1) | `xsd:float` | The diameter of the lens mount in millimeter. |
| [`FlangeDistance`](#preda1_1) | `xsd:float` | The distance between end of the lens and the sensor in millimeter. |
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

## Recent Changes
<!-- omit in toc -->
0.2:
Important changes of the class list and properties.

0.1:
Original draft.