# Vision AI
Derive insights from your images in the cloud or at the edge with AutoML Vision or use pre-trained Vision API models to detect emotion, understand text, and more.

[Full docs here](https://cloud.google.com/vision/)

## Auto ML Vision
* Automate custom model training
* Has UI Console for ease of use
* Optimise models to increase:
    * Latency
    * Accuracy
    * Size
* Export to the cloud or devices on the edge

## Vision API
* Pre-trained models
* REST and RPC APIs
* Detect:
    * Objects
    * Face
    * Printed text
    * Hand written text


## Benefits
### Detect objects automatically
* Classify object
* Detect location of object

### Gain intelligence at the edge
* AutoML Vision Edge to deploy high accuracy models
* Trigger real time acitons
* Supports many edge devices

### Reduce purchase friction
* [Vision Product search]() can create and engaging mobile experience for customers to upload an image of what they want.


### Understand text and act on it
* Detect text with in and image
* More than 50 languages
* Various file types
* Part of [Document Understanding](./document_understanding_ai.md) AI

### Detect explicit content
* Review images using [Safe Search](./safe_search.md)
    * Estimates the chances that the images is explicit

### Data labelling service
* Team of people that annotate images



## Which Vision ML is good for you?
||AutoML Visiion|VisionAPI|
|-|-------------|----------|
|User Interface|||
|
|**Use APIS** <br> REST AND RPC API|X|X|
|**GUI**|X||
||
|Predefined or custom labelling|
|**Classify using pre defined labels**<br> Leverage vast libraries of pre-defined labels||x|
|**Classify using custom labels**<br> Traing models to use custom labels|X|
|**Use Google’s data labeling service**|X|X|
||
|Deploy at the edge|
|Deploy machine learning models at the edge|X|Integrate with [ML Kit](../firebase_ml_kit/ml_kit.md)|
||
|Additional features|
|**Detect objects**<br>Detect objects, where they are, and how many.|X|X|
|**Enable vision product search**<br>Compare photos to images in your product catalog, and return a ranked list of similar items.||X|
|**Detect printed and handwritten text**<br>Use OCR and automatically identify language.||X|
|**Detect faces**||X|
|**Identify popular places and product logos**||X|
|**Assign general image attributes**||X|
|**Detect web entities and pages**||X|
|**Moderate content**||X|

