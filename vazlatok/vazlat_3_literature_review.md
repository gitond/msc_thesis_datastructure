# 3 Literature review

## 3.1 Client-Server Architectures

## 3.2 Computer Vision (CV)

## 3.3 Augmented Reality (AR)

## 3.4 Prototypes Similar to Ours

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
