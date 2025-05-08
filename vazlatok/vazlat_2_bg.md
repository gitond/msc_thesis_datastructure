# 2 Background

## (2.1 Justification for RQ1 (come up with a better title later))

RQ1: technological challenges in combining CV & AR
 - Introduce CV & AR
 - Why do we want to combine these techs?
   - Traditional AR tracking: built to detect specific things in environment
   -  CV: larger computer model used for image analysis could theoretically be used to perform this task
     - Solves some problems but creates others
       - This is what we aim to map out

## (2.2 AR in a nutshell (come up with a better title later))

Definitions for AR:
 - AR can be defined as “a real-time direct or indirect view of a physical real world environment that has been enhanced/augmented by adding virtual computer generated information to it. (reyesEtAl2016)
 - extended version of the physical world overlaid with digital content bridging the real and virtual environments (ghasemi)
 - interactive experience, where real world objects are enhanced by computer-added information (minaeeLiangYan)
 - Software that superimposes information on top of the real world to create interactive experiences, often in forms of 3D objects. (estrada, VanGestel2024)

Needed for AR:
 - According to  (reyesEtAl2016)
   1. computing device
   2. software
   3. camera
   4. display device
 - According to (ghasemi)
   1. computing unit: produces virtual content
   2. projection surface: displays virtual content to users
 - According to (minaeeLiangYan)
   1. processor
   2. display
   3. sensors
   4. input devices

Types of AR:
 - marker-based AR
   - AR triggered by pre-defined markers such as barcodes or QR-codes (estrada)
   - markers are used to register a position of a virtual object into the user's perceptions of the real world (reyesEtAl2016)
   - markers often attached to real-world objects (ghasemi)
   - On top of the four components listed by (reyesEtAl2016), marker based AR also requires physical markers. (reyesEtAl2016)
 - markerless AR
   - markerless AR doesn't use pre-defined markers, instrad it collects data from sensors such as a camera or a GPS and uses advanced algorithms to determine where to render the augmentations. Typically these algorithms are computer vision based. (estrada)
   - needs to obtain a spatial map of its environment (ghasemi)
   - needs to do flat surface detection (ghasemi)
   - (ghasemi) proposes the use of deep-learning based methods
   - Types of markerless AR: (estrada)
     - Location-based AR
       - AR content locked to geographical areas which is obrained through GPS, compass other sensor (Batuwanthudawa and Jayasena)
       - Typically use Simultaneous Localization and Mapping (SLAM) algorithms are used to map the local area, keep track of the users position within it and show the augmentations (estrada, Bailey and Durrant-Whyte)
     - Superimposition-based AR
       - Object detection algorithms are used to detect an object from a camera feed and then an augmentation is superimposed on top of it (estrada)
     - Projection-based AR (aka projection mapping, spatial AR)
       - A type of AR where a projector is used to project the augmentation onto a surface rather than using a screen with a camera feed to show the augmentations (estrada)
       - An example project used various CV algorithms for tracking, including geometric shape detection and hand gesture detection (KimSeoHan)
     - Outlining-based AR
       - Tracking is done by CV algorithms that specialize in detecting outlines, contours and forms. In other words: real world targets are recognized by their shape (estrada)
