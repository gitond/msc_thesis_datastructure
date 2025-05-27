# 3 Literature review

## 3.1 Computer Vision (CV)

### CV: Intro

- Computer Vision: a field of tudy where cameras and computer systems are used to extract information from the real world. (concise computer vision)
- In 1966 Rosenfeld and Pfaltz had already used computers to perform pattern recognition on images (ghasemi)
- Early CV used stuff like pattern recognition, part-based algorithms, matching techniques and statistical classifiers to analyze images (ghasemi)
- Nowadays DL-based methods are being used (ghasemi)
- Deep Learning (DL): a sub-field of Machine Learning (ML) where algorithms modeling the structure and function of the human brain, known as deep neural networks are used to complete various tasks (estrada)
- Main difference between DL and early CV: in early CV you had to manually come up with an algorithm to track the objects. In DL you feed a large number of data to an existing method and it will learn the patterns by which to recognize the trackable object. (ghasemi)

### Object detection as a task

  - a popular research topic within DL in the past decade, due to its potential in several heavily researched applications such as Autonomous driving and robotics (estrada, ghasemi)
 - goal: given an image frame, find one or multiple pre-defined objects within it (ghasemi)
 - sub-tasks according to (ghasemi):
   - object localization: determining the exact location of the object within the frame
   - object classification: determining which kind of object has been found, when using object detection to detect multiple different kinds of objects

### Object detection: Relevance to AR; Early CV vs DL based Object detection

 - The tracking of markers in Marker-Based AR can be thought of as an example of object detection (ghasemi)
 - However this is typically not done with DL algorithms, but with older CV techniques such as statistical classifiers (ghasemi)
 - Example: (zhang, fronz, navab) compare different tracking systems and while they don't describe each of their internal workings in depth, they build a "checking" system on top using openCV corner tracking, which is based on a traditional non-DL CV corner detection algorithm from 1988 (opencv, harris corner detection)
 - While DL-based object detection methods require more computation (ghasemi, minaee2022modernaugmentedrealityapplications) showed that there are methods suitable for running on low powered hardware such as mobile phones or AR-glasses, at a high enough framerate, that these could also be used to achieve markerless AR on mobile devices
 - In fact (estrada) does this in 3.2!
 - <mark>We might want a picture comparing early CV vs DL-based methods ability to detect objects such as in (ghasemi) Fig.3 somewhere</mark>

### (minaee2022modernaugmentedrealityapplications)
- (minaee2022modernaugmentedrealityapplications) went through DL-techniques used in AR-applications
- They found DL was used in AR applications for use cases such as:
  - Face and body transformations (essentially using DL image-to-image transformations to generate photography filters and then feed the images with the filters back to the users)
    - in shopping apps: clothing try-on, makeup try-on
  - Tracking and user pose estimation
  - Human reconstruction
  - Face transformation
  - Scene reconstruction
  - Traditional pattern recognition and geometry application
- They mention several datasets that can be used to train DL-models:
  - Deepfashion1, a high quality dataset of over 800 000 pieces of clothing which can be used to train a DL-model to track pieces of clothing (liuziwei7 deepfashion1 poster)
- They also mention several AR applications powered by DL-algorithms:
  - VITON an AR application which let's the user choose a piece of clothing and then shows the user in that piece of clothing (han viton arxiv)
  - Deep Localized Makeup Transfer Network which can recommend makeup products to users and show them how'd they look with that makeup on (liu makeup arxiv)
- x

### Object detection methods

 - A Convolutional Neural Network (CNN) takes an image, divides it into pieces, analyses the pieces through convolution and pooling and then performs object classification through this analysis (ghasemi)
 - A Region-based Convolutional Neural Network (RCNN) first analyses the image using another method to define Regions of interest, then applies a CNN to the detected regions of interest (ghasemi, estrada)
 - (You Only Look Once) YOLO divides the input image into S*S grids and searches each grid for the object. It is considerably more light-weight than region-based methods like RCNN (ghasemi, estrada)
 - Technologies mentioned by (ghasemi) being suitable for real-time (AR) use on mobile hardware: MobileNet v2 (CNN based), tiny YOLO v2 (YOLO based)

[](Now-including-CSA-stuff)

## 3.2 Prototypes Similar to Ours

 - bg ok, now prototypes

### (Pylvänäinen et al., 2023)

#### Goal & need for proto

 - Observation: there are no mobile apps for microscopy education that incorporate AR/VR features and step-bystep guidance (Pylvänäinen et al., 2023) 
 - They sent out a needs assessment survey to students and 70% of the respondents showed interest in using such an app in their microscopy studies. (Pylvänäinen et al., 2023)
 - App should:
   1. Teach microscopy
   2. Help to operate microscope
   3. Help with troubleshooting
   4. Be a tool to revive knowledge after a long pause (Pylvänäinen et al., 2023)

#### Technical details

 - App structure (Pylvänäinen et al., 2023):
   - Teach me microscopy (For independent studying)
   - Help me at the microscope
     - Virtual microscope
       - 3D model of an actual microscope (Leica DM RXA microscope)
       - Interactive step-by-step tutorials (usable while working on microscope)
         - microscopy parts
         - how to set optimal Köhler alignment
         - how to focus on the sample
     - Test your knowledge
     - Learn more
   - Help me to troubleshoot

 - "Help me at the microscope" also acts as an AR-environment (marker based); AR-markers help students find different parts of the microscope and their functions; (Pylvänäinen et al., 2023)
 - Support for microscope specific information through AR

#### Experiment results
 
 - the team then conducted a questionnaire based usability study and found that
 - students that used the app were more confident at using the microscope (Pylvänäinen et al., 2023)
 - statistics (Pylvänäinen et al., 2023):
   - app helped learning microscopy? 64% definitely; 36% somewhat
   - app helped recall microscopy skills? 90% definitely 10% somewhat

### (Estrada et al., 2022)

#### Goal & need for proto

 - Goal: Enable students to have a better experience when learning how to use electrical engineering lab equipment (Estrada et al., 2022)
 - How? Offer AR-based tutorials for various electrical engineering lab equipment. Use Deep Learning (DL) methods to detect such equipment in the laboratory. (Estrada et al., 2022)
 - Long term-goal: Develop interactive smartphone apps for different laboratory devices integrating this concept. (Estrada et al., 2022)

#### Technical details

 - What was built for this prototype (Estrada et al., 2022):
   - Superimposition based AR-app
   - DL-based component (DL-model integrated into AR-app)
   - Per-equipment
     - AR-UI
     - Step-by-step tutorials using AR-UI
   - Supported equipment (DL-based object detection):
     - multimeters
     - oscilloscopes
     - wave generators
     - power supplies
   - Supported equipment (object detection + step-by-step tutorials):
     - "real multimeters"

 - Application logic: How does this prototype work? (Estrada et al., 2022)
   1. DL-model detects (classifies & localizes) compatible equipment
   2. UI notifies user that app has tutorial available for detected equipment
   3. User decides to view tutorial
   4. AR-based tutorial is loaded
   5. 3D-object gets superimposed on top of real object, UI-panels (AR-UI) are used to display tutorial content

### (van Gestel et al, 2024)

#### Goal & need
 - Orthopedic procedures, use of power tools in surgery, guidance techniques & safety measures, new AR based real time safety solution (Van Gestel et al, 2024)
 - Existing AR-based and robotic surgery systems are often bulky (with a sizeable screen, camera and/or computer unit), expensive, and time-consuming, limiting their use in orthopedic surgery^13,14^." (Van Gestel et al, 2024)
 - HMDs exist, but can't do accurate enough tracking (millimeter scale) for surgical procedures (Van Gestel et al, 2024)

#### Technical details
 - solution developed on Microsoft HoloLens, using infrared sensor rather than RGB camera (tracking accuracy reasons) (Van Gestel et al, 2024)
 - infrared-reflective markers using the HoloLens’ on-board infrared sensor, (mean tracking error of 0.78 mm ± 0.74 mm; unpublished Vicon validation testing) (Van Gestel et al, 2024)
 - markers are not physical markers, rather markers registered by an infrared-tracked stylus at each of the 12 entry points (Van Gestel et al, 2024)
 - AR-guidance vector showed correct drilling direction. If drilling direction aligned with the one showed by guide vector guide vector was green, otherwise it was orange/red depending on how big the difference between the actual & desired drilling directions was (Van Gestel et al, 2024)

#### Experiment & results
- Developed tool tested by letting 18 people drill on wooden models & comparing the drilled output itself between AR & other guidance techniques (Van Gestel et al, 2024)
- three guidance techniques: freehand drilling, proprioception-guided and AR-guided drilling. Freehand: no guidance, proprioception: participants drilled based on tactile and proprioceptive feedback on the exit point using the contralateral index finger, AR-guidance: AR solution shows correct drilling direction
- Drilling objective: connect entry and exit point on wooden model. To simulate limited exposure in the operating field, a fenestrated cloth covered the logs, revealing only the entry points (Van Gestel et al, 2024)
- we assessed drilling performance in terms of error magnitude and error direction. Two blinded investigators (FVG, FVA) measured the values independently. If the measurements differed within 1 mm for _r_ and 5° for _θ_, we averaged the results. An error magnitude below 0.1 mm without a discernable error direction was considered an on-target drilling performance. (Van Gestel et al, 2024)
- Statistical analysis on drilling session results (Van Gestel et al, 2024)
- The deviation angle (α) was considered as a dependent variable and guidance technique, experience level, and drilling direction as predictors. Interactions between predictors were also analyzed (Van Gestel et al, 2024)
- The use of AR guidance for directional drilling yielded a higher angular accuracy compared to freehand and proprioceptive guidance. Regardless of experience, AR reduced the angular error by nearly half and led to more on-target drilling outcomes. Particularly in oblique drilling, AR proved highly beneficial, greatly reducing scatter along the Y-axis. (Van Gestel et al, 2024)
- Out of a total of 216 drillings, 5 (2.31%) were on-target (r < 0.1 mm). None of the drillings were on-target in the freehand group, 1 in the proprioception group and 4 in the AR group (χ^2^, p = 0.074). (Van Gestel et al, 2024)
- AR reduced angular uncertainty during directional drilling, improved drilling accuracy, particularly for complex trajectories and angles, observed across all experience levels (Van Gestel et al, 2024)

### (Reyes et al, 2016)

#### Goal & need
 - Project goals:
   1. Develop AR system to aid novice users in using milling & lathe machines in a school manufacturing laboratory
   2. measure the acceptance rate and performance of the system 
 (Reyes et al, 2016)
  - Requirement for using both hands with the machinery simultaneously with the AR-system. (Reyes et al, 2016)

#### Technical details
 - Mobile Augmented Reality (MAR) system (mobile app for Android) (Reyes et al, 2016)
 - Tutorials for a milling & a lathe machine:
   - tool setup
   - working material setup
   - machinery setup
   - starting the machines in question
 (Reyes et al, 2016)
 - AR-elements:
   1. 3D models of machinery (milling & lathe machines) and tools such as spanners and Allen wrenches.
   2. Text instructions to describe how to perform the basic tasks.
   3. Labels, which help the user for locating machinery components and tools.
   4. 3D arrows to indicate flow direction.
   5. Real time videos that include task explanations performed by experts
 (Reyes et al, 2016)
  - Not to be run on smarthphones as such (two hands requirement).
    - Hardware options:
      - optical see-through glasses where the real world is observed through transparent mirrors placed in front of the eyes of the user (ORA-1 AR glasses)
      - video see-through HMD (VR-PRO AR HMD)
 (Reyes et al, 2016)
  - Marker-based (M)AR (Reyes et al, 2016)
  - Two kinds of markers
    - Frame markers (FM) traditional AR-markers: frame patterns with encoded data in the frame
    - Item Targets (IT) real world objects that the system tries to match to a 2D image using CV-algorithms such as edge and corner detection
 (Reyes et al, 2016)
  - Marker purposes:
    1. machinery detection
    2. showing augmentations
    3. showing explanation videos
 (Reyes et al, 2016)

Application flow:
```mermaid
flowchart TD
A[Main menu marker] --> B[Main menu]
B --> C[Start application]
B --> D[Get system help infromation]
D --> E[User gets info on how to use app]
C --> F[User can scan device markers]
F --> G[Corresponding tutorial starts, lesson markers activated]
G --> H[Lesson markers]
H --> I[Multimedia markers]
```
 (Reyes et al, 2016)

#### Experiment & results
 - tested by 16 students and teachers at the university manufacturing laboratory through a survey (Reyes et al, 2016)
 - Experiment flow:
   - General introduction to AR
   - Introduction to AR system in this study
   - Completing lessons in AR system on 1/2 hardware options
   - Completing a survey
   (Reyes et al, 2016)
 - 10 question survey with a Likert-scale style scoring system:
   - first 5 relating to acceptance metrics (satisfaction, precision, understandability, explanativeness, attractiveness)
   - next 3 relating to performance metrics (interface, speed, marker system)
   - a generic "Have you used mobile AR systems before?"
   - an open answer field
    (Reyes et al, 2016)
 - Results:
   - Averages (calculated by Likert-scale to point conversion where: very bad = 1, regular = 3, very good = 5)
     - satisfaction: 4
     - precision: 4
     - understandability: 4,5
     - explanativeness: 4
     - attractiveness: 4,5
     - interface: 3,5
     - speed: 4
     - marker system: 4,5
   - Interface was the weakest element. Only 50% rated it as good or very good
   - Open answer field notes:
     - Teachers & lab staff participating in this study were interested in using it as an educational tool later
     - Students also saw it as an appealing way to learn machine operation basics
     (Reyes et al, 2016)
 - Takeaways:
   - The system developed for this project has potential to be a real-life teaching-learning tool.
   (Reyes et al, 2016)


### (Lin & Lee, 2020)

#### Goal & need
 - Using AR-simulation as a practical aid to deepen students' understanding of CNC-machine operation independently. (Lin & Lee, 2020)
 - Solve resource limitation problems in education:
   - limited number of machines
   - insufficient space
   - limited amount of processing materials
   - machine tool wear
   - &rarr; students don't get enough practice on actual CNC-machines
   (Lin & Lee, 2020)
 - Certain problems are difficult to learn using traditional teaching methods such as: 
   - limitations of the physical size & capabilities of CNC machines vs how they compare to models of workpieces created by modelling software
   - different 3-Dimensional & complicated manufacturing processes and methods, such as turning over processing, mold hole processing, etc are hard to visualize with traditional methods.
   - understanding how the instructions sent to the machine actually affect the workpiece itself.
   (Lin & Lee, 2020)

#### Technical details
- Using AR to simulate CNC machine machining process and machine operation (Lin & Lee, 2020)
- The built-in virtual imaging technology can superimpose virtual 3D machining workpieces on the physical CNC machine using mobile hardware (tablets) as displays (Lin & Lee, 2020)
- AR markers for different operation processes, placed on the CNC machine (Lin & Lee, 2020)
- Pre-made animations for different manufacturing processes supported by the CNC machine (Lin & Lee, 2020)

#### Experiment & results
- Ten participant study consisting of tool-aided CNC machine operation followed by filling out System Usability Scale-type questionnaire (SUS) (Lin & Lee, 2020)
- The participants had prior CNC machine experience, but were still novice level students (Lin & Lee, 2020)
- The students used the app developed for this study to simulate operating a CNC machine to manufacture an example furniture piece (Lin & Lee, 2020)
- Questionnaire:
  - five different evaluation dimensions:
    - Understanding of Machining Procedures
    - Time of Operation
    - Accuracy of Operation
    - Sequence and Information of the CNC Operation Steps
    - Understanding of the Interface Knowledge of the CNC Cutting Machine Center
  - 20 questions in total
  - each secored 1-7 (1: high difficulty, 7: low difficulty)
  (Lin & Lee, 2020)
- Scores per evaluation dimension:
  - Understanding of Machining Procedures: 4,86
  - Time of Operation: 4,8
  - Accuracy of Operation: 5,52
  - Sequence and Information of the CNC Operation Steps: 4,98
  - Understanding of the Interface Knowledge of the CNC Cutting Machine Center: 5,6
  (Lin & Lee, 2020)
 - results showed that the students could understand the relationship between workpieces and methods on the CNC machining through the AR system (Lin & Lee, 2020)
 - Advantages found in using AR-based system for learning CNC machine operations: 
   1. students understood & were able to complete necessary steps of using CNC machine for making furniture
   2. students understood the relationship between the vitrual representations of processing objects and the real-world procedure
   3. the system reduced  the work needed to be done by the teachers to teach operating the CNC machine to students
   4. students were able to practice CNC machine operation more as they weren't limited by machine availability anymore. This also decreased material waste and safety risks
   5. students were able to preview the interaction between models done by them and the cutting path of the CNC machine.
   (Lin & Lee, 2020)
