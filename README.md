TensorFlow.js Boilerplate
=================

This very simple skeleton simply loads in TensorFlow.js and prints out the version once loaded to the DOM.

From these humble beginnings you can do some really great things. 

Feel free to fork this and use it as a quick way to start coding with TensorFlow.js directly or following some other tutorial that needs TensorFlow.js to run.


Your Project
------------

### ← index.html

We simply have a script tag in our HTML to grab the latest version of TensorFlow.js

In this case we simply reference the following:

```HTML
<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs/dist/tf.min.js" type="text/javascript"></script>
```

However, if you want to pull in a particular version of TensorFlow.js you can do so like this:

```HTML
<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@1.4.0/dist/tf.min.js" type="text/javascript"></script>
```

Optionally, if you want to include our TF.js visualization library you can do so using this import:

```HTML
<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs-vis/dist/tfjs-vis.umd.min.js" type="text/javascript"></script>
```
However feel free to remove if you are not using this for visualizing training etc. [More details here](https://github.com/tensorflow/tfjs/tree/master/tfjs-vis).

### ← style.css

Nothing to see here. Just styles to make the demo look prettier. You can use or ignore these as you please.

### ← script.js

This simply grabs a reference to a paragraph in the DOM and then prints out the TensorFlow.js version number to it once loaded.


-------------------


### Notes

Inference is simply the act of taking some input and running it through the machine learning model 
(essentially a lot of mathematical operations), and then providing some results. With the TensorFlow.js
pre-made models we return our predictions in the form of JSON objects, so it is easy to use.

You can find the full details of this predict function in our GitHub documentation for the COCO-SSD model here..
This function does a lot of heavy lifting behind the scenes: 
It can accept any "image like" object as its parameter, such as an image, a video, a canvas, and so on.
Using pre-made models can save you a lot of time and effort, because you won't need to write this code yourself and can work it "out of the box".

### Recap


In this codelab we:

Learnt the benefits of using TensorFlow.js over other forms of TensorFlow.
Learnt the situations in which you may want to start with a pre-trained machine learning model.
Created a fully working web page that can classify objects in real time using your webcam, including:
Creating a HTML skeleton for content
Defining styles for HTML elements and classes
Setting up JavaScript scaffolding to interact with the HTML and detect the presence of a webcam
Loading a pre-trained TensorFlow.js model
Using the loaded model to make continuous classifications of the webcam stream and drawing a bounding box around objects in the image.


### Notes


Bounding Boxes

Bounding Boxes are drawn with the origin at the top left corner of the box, and their dimensions include the width and height, represented by 'x' and 'y' respectively 

Bounding boxes are rectangles that are drawn around objects of interest in an image. The COCO-SSD model, in addition to detecting objects, also returns four pieces of information about each object. These are parameters of the rectangles or bounding boxes that can be drawn around each object. The parameters are:

The ‘x’ coordinate of the top left corner of each box.
The ‘y’ coordinate of the top left corner of each box.
The width of each box.
The height of each box.