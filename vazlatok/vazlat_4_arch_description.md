# 4 Architecture description

## 4.1 Problem description

Justication for RQ2 should be included in this chapter
RQ2: can such a system be used in cooking?
 - Goal: build a demo system thet uses CV with AR
[](Issue #29 Prototype Description)
 - Our prototype will guide the user through the recipe...
 - Computer Vision is used to...
 - To test the prototype we'll
[](Close issue #29)
Justifying CV & discussing our recipe
 - Goal: offer **real-time** guidance for **actions** involved in making the dish
   - adding ingredients to pots, handling kitchen appliances, peeling and chopping ingredients
   - These actions as AR-annotations (animations)
 - Case for using CV in tracking: lots of things to track
   - Ingredients
     - These have different states
   - Different kitchenware
     - bowl, knives
Why cooking?
 - Real world problem where CV with AR could be useful.
 - Similar step-by-step approach as other prototypes in the education field
   - pylvanainen, reyesEtAl2016: step-by-step instrument teaching tutorial approach
 - If the end product here is successful the general approach could be adapted to different fields

 - We want our prototype to run on mobile
 - We want our prototype to be easily portable between platforms
[](Issue #32 how to run on mobile)
 - At this time we are focused on building a web app

## 4.2 Perceived Challenges 

 - What to track?
 - Data Availability
 - Data Quality
 - Data Specificity (coco has relevant labels bowl, apple, orange, banana) but it also has a million other categories unrelated to our wants. There exist application specific datasets (Lakshay Tyagi Fruit detection dataset), however if we choose to track objects outside of their domain, they are no longer enough
 - Limitations of CV in practice
   - environmental variables (lighting conditions etc) may affect the effectiveness of CV (ghasemi)
   - trackable object moving may present a problem (ghasemi)
 - Need to perform CV in real time
 - Perofrming CV tasks on mobile
   - Issues with computation time, effectiveness (ghasemi)
     - Specifically with more advanced tasks such as detection, segmentation (ghasemi)
   - Energy consumption (ghasemi)
 - Portability between platforms
   - One solution is to build for the web
     - But this creates its own set of challenges
       - How to build AR or CV for web?
   - Platform specific issues
     - Mobile: discussed
     - HoloLens: unpleasant, uncomfortable, limited battery capacity, sometimes has online connectivity requirement (ghasemi)
 - The whole action detection problem: even if we can track each object separately, a step in the recipe would be something like "chop the apple to pieces". How does the system know this is done?

## 4.3 Proposed Architecture

 - CV stuff
   - (estrada) use MobileNet-SSD v2 for tracking in their application
     - How well does it perform?
     - This is probably a right way for us to go because...
   - Train with COCO
     - high quality dataset
   - but only with images that contain: bowl, spoon, knife, apple, orange, banana
     - lighter, faster to train model
 - Devtools
   - Tensoflow.js
 - AR-UI
   - Superimposition based AR
   - We basically need to render augmentations on top of a camera feed. The location of the rendered stuff will come from the object detection model
   - A-frame

*Figure 4.1: Visual Representation of the Proposed Architecture*
