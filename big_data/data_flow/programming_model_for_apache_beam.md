# Programming model for Apache Beam
[Full docs](https://cloud.google.com/dataflow/docs/concepts/beam-programming-model)
* Apache Beam is:
    * Open Source
    * Unified model for defining batch and streaming-data-parallel processing pipelines.
* Dataflow abstracts the low level handling away from the processing.


## Concepts
### Basic Concepts
* Pipelines
    * Encapusulates all of the steps from reading input data, to transforming the data, to writing that data to somewhere.
    * The input sink can be different types, allowing the conversion of data from one format to another.
    * Apache Beam starts by creating a Pipeline object and then that object is the basis for creating the datasets.
* PCollection
    * Represents a potentially distributed, multi-element dataset that acts as the pipelines data.
    * Can be a fixed size, or unbounded if it's coming from a continuesly updating datasource.
* Transforms
    * Represents the transforming operation that transforms the data.
    * Takes one or more PCollections as an input.
        * Performs an operation on eache element in that/those collections
    * Produces one or more PCollections as output.
    * Can perform nearly any kind of processing operation on the data.
* ParDo
    * Core parallel processing function in the Apache Beam SDK
    * Calls a user specified function on each element of a PCollection.
    * COllects the 0 or more outputs into an 'output' PCollection.
    * The ParDo transform processes elements independently and possibly in parallel.
* PipelineI/O
    * Beam I/O Connectors read data into the pipeline.
    * A connector consists of a `source` and a `sink`.
    * All beam `sources` and `sinks` are `transforms` that let the data pipeline work from several different storage formats.
* Aggregation
    * Aggregating is the proccess of computing some value from multiple input elements.
    * Primary aggregation technique is to group all the elements with a common key and window.
    * Then, it combines each group of elements using an associative and commutative operation.
* User-defined Functions(UDFS)
    * Some operations in Beam allow users to run their own code.
    * In a `ParDo` user defined code defines an operation that will be done against every element.
    * For a `Comnine` it defines how an element should be combined.
    * Can write UDFS in different language to the runner
* Runner
    * Runners are the software that accepts a pipeline and executes it. Most runners are translators or adapters to massively parallel big-data processing systems. Other runners exist for local testing and debugging.

### Advanced Topics
* Event time
    * The time that the data is captured, appose to the time that the data is processed.
* Windowing
    * Enables grouping of operations over unbounded data.
    * Divides the collection according to the timestamps of individual elements.
    * Windowing function tells the runner how to assign elements to an initial window.
        * How to group/merge windows
    * Apache Beam lets you define different kinds of windows or use the predefined windowing functions.
* Watermarks
    * system's notion of when all data in a certain window can be expected to have arrived in the pipeline.
    * Tracks watermark because data is not garunteed to arrive in the pipeline in the right order.
* Trigger
    * Determine when to emit aggregated results as data arrives.
    * For bounded data, data is emitted when the watermark passes the end of a window.
    * Apache Beam provides several predefined triggers and lets you combine them.
    








