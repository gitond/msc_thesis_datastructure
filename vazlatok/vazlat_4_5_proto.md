# 4.5 Prototype Description

## 4.5.1 (Our Prototype: Need and User-perspective)

[](Purpose_of_the_Prototype_&_Research_Motivation_BEGINNING)
Justication for RQ2 should be included in this chapter [](From_4.1)
RQ2: can such a system be used in cooking? [](From_4.1)
[](Purpose_of_the_Prototype_&_Research_Motivation_END)
[](User-Perspective_Description_of_the_Application_BEGINNING)
 - High-level description of the application as a user would encounter it. [](NEW)
 - “An AR application which guides the user through the preparation of a fruit salad.” [](From_last_session's_notes)
 - Goal: offer **real-time** guidance for **actions** involved in making the dish [](From_4.1)
   - adding ingredients to pots, handling kitchen appliances, peeling and chopping ingredients
   - These actions as AR-annotations (animations)
 - Similar step-by-step approach as other prototypes in the education field [](From_4.1)
   - pylvanainen, reyesEtAl2016: step-by-step instrument teaching tutorial approach
 - Emphasize: user interaction is passive—camera + system guidance only. [](NEW)
 - Describe end-to-end usage flow from user POV. Could be a diagram [](NEW)
[](User-Perspective_Description_of_the_Application_END)

## 4.5.2 How Technical Challenges Affected Prototype Development 

[](Challenge1:_What_to_track)
 - What to track? [](From_4.2)
 - Case for using CV in tracking: lots of things to track [](From_4.1)
   - Ingredients
     - These have different states
   - Different kitchenware
     - bowl, knives
 - The whole action detection problem: even if we can track each object separately, a step in the recipe would be something like "chop the apple to pieces". How does the system know this is done? [](From_4.2)
[](Challenge2:_Data_availability_and_recipe_design)
 - Data availability strongly shaped which recipe steps were feasible. [](NEW)
 - Data Quality [](From_4.2)
 - Data Specificity (coco has relevant labels bowl, apple, orange, banana) but it also has a million other categories unrelated to our wants. There exist application specific datasets (Lakshay Tyagi Fruit detection dataset), however if we choose to track objects outside of their domain, they are no longer enough [](From_4.2)
 - No need for costly data creation stage: MS COCO already has suitable data [](From_5.1)
*Algorithm 5.1: the recipe*
[](OLD5.2_HERE)
 - MS COCO dataset downloaded using fiftyone
 - Only the pictures that match our trackable categories (filtering code)
[](OLD5.2_END)

## 4.5.3 Architecture and Technology Stack

[](Ready_parts)
 - (estrada) use MobileNet-SSD v2 for tracking in their application [](From_4.3)
 - Tensorflow used for training CV module. Specifically MobileNet-SSD v2. [](From_5.3)
[](Future_parts)
 - trained model to tf.js conversion [](From_5.3)
[](5.4_HERE)
 - How is the CV module integrated into the mobile app?
 - How does the app track the steps of the recipe?
[](5.4_END)
 - State machine or step progression system determines next instruction. [](NEW)
[](AR-UI_ALL_From_4.3)
 - AR-UI
   - Superimposition based AR
   - We basically need to render augmentations on top of a camera feed. The location of the rendered stuff will come from the object detection model
   - A-frame

*Figure 4.1: Visual Representation of the Proposed Architecture*

## 4.5.4 How Technical Challenges Affected Experimental Setup

[](May_move_this_to_5.5)

[](From_4.2)
 - Limitations of CV in practice
   - environmental variables (lighting conditions etc) may affect the effectiveness of CV (ghasemi)
   - trackable object moving may present a problem (ghasemi)
 - Need to perform CV in real time
 - Perofrming CV tasks on mobile
   - Issues with computation time, effectiveness (ghasemi)
   - Energy consumption (ghasemi)
 - Portability between platforms
   - One solution is to build for the web
     - But this creates its own set of challenges
       - How to build AR or CV for web?
   - Platform specific issues
     - Mobile: discussed
     - HoloLens: unpleasant, uncomfortable, limited battery capacity, sometimes has online connectivity requirement (ghasemi)
[](NEW)
 - Limitations of TensorFlow.js performance across browsers.
 - Model size constraints for mobile browsers.
