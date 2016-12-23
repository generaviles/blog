---
layout: post
section-type: post
title: Cellular Automatas and Medical Images
category: image processing
tags: [ 'medical images' ]
---

Cellular Automata (CA) are models that are <a href="https://en.wikipedia.org/wiki/Discrete_mathematics"> discrete </a> in time and space, also known as tessellation automata, homogenous strucures, cellular structures, iterative arrays, etc.
Mathematically, they can be defined as a 3-tuple where N is a set containing the neighborhood values, S is a set containgin the possible states and <i>delta</i> being the transition function.

<p style="text-align:center;"><i>CA={S,N,delta}</i></p>

In the medical world, CA are used to mimic tumor growth, data encriptation, image processing, among others.

It is this last application that caught the attention of a friend of mine and I at a discrete mathematics class here at school. We were given a paper by <a href= "http://yadda.icm.edu.pl/yadda/element/bwmeta1.element.baztech-6e271df5-f264-47c9-9017-d6808ff2f1b4"> Płaczek </a> where CA are used to find the edges images or components of images. This has tremendous implications in the medical datsphere, it could be applied in the automatization of the analysis of <a href= "http://www.medical-labs.net/normal-blood-smear-649/">blood smear samples </a>, <a href= "http://boneandspine.com/types-fracturesa-simple-classification-fractures-long-bones/">francture identification </a>, <a href="http://www.crios.be/genotoxicitytests/micronucleus_test.htm">genetic damage evaluated through micronucleus </a>, etc, etc, etc.

We set out to propose a CA with the least amount of rules possible that still could do a decent job at identifying fractures of long bones. After going over some theory and long hours of discussion, two rules emerged as the winners for this automaton, we decided that our CA was going to work on binary (black & white) images and identify borders in the objects of the image.
In orther for the rules to be understood we have to declare some concepts before:
<ul>A greyscale image can be represented by a matrix of data<i> F={W x M} </i>where<i>F<sub>W,M</sub> belong to the set of numbers <i>{0,1,2,...,255}.</i></i> </ul>
The following image summarises the rules:

<image src= "../img/carules.jpg" width="600" height="300">

<i>N </i>being a matrix of <i>3x3.</i>

With this approximation we were able to obtain preliminary results that reflected the power of working with a CA showing significant results with simple rules.

I will just show you one image of what this CA can produce, on the left you will see an image of an X-Ray of a femur with an oblique fracture, the next image is the binary version of the first. The one on the right hand side is an image produced entirely by the cellular automaton designed by us.

<image src="/img/fractura.jpg" width="600" height= "160">

As you can si it was able to find the borders of the structred represented in the original image. Eventhough it is imposible to miss this fracture, the fact that a mathematical model with <i>just</i> two rules can generate this is impresive and talks to the potential for it's use in more advnaced applications.
