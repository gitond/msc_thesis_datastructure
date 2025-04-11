
## 3 Literature review

### 3.1 Client-Server Architectures

> "Deep learning is capable of making the AR/MR systems smarter. However, to implement deep learning-based object detection, some obvious considerations need to be considered when choosing between a remote server or a local device. Fig. 5 shows the two processes for the object detection computation. This section discusses some advantages and disadvantages of each approach and explains some use cases from the literature. Capability, computation cost, complexity, and size of the model are important factors in choosing the computation method."
(Ghasemi et al, 2022)

> "For the remote server-based computation, the client/user (i.e., AR device) captures frames and sends them to the remote server; then the model processes the data on the server. Then, the model sends the output back to the client/user. Network connection and delays are important factors during this process."
(Ghasemi et al, 2022)

> "Out of 69 studies collected for this review, 48 studies used cloud, edge, or GPU servers. 17 studies implemented their computation on the local AR devices, and 4 studies used both server and local devices for their computations."
(Ghasemi et al, 2022)

> "An android application to enable real-time AR was developed to perform object detection (Ran et al., 2017). They performed the object detection on both server and mobile devices and showed that factors affecting detection performance in these scenarios include model size, offloading decision, and video resolution. While the results using the server highly depend on the network condition, they concluded that offloading on the server improved frame rate and accuracy."
(Ghasemi et al, 2022)

> "Since time consumption is considered one of the main challenges of deep learning, studies used servers to increase the speed of computations even in the training process"
(Ghasemi et al, 2022)

> "Based on the reviewed studies and the tradeoffs each method entails, server-based object detection is more common and easier to implement."
(Ghasemi et al, 2022)

### 3.2 Computer Vision (CV)
> "Deep learning (DL), a sub-field of machine learning (ML), embraces artificial neural networks (ANN), which are algorithms inspired by the structure and function of the human brain"
(Estrada et al., 2022)

> "Object detection is primarily used in computer vision and has gained popularity in a variety of applications over the last decade, including autonomous vehicles, intelligent video, and surveillance systems<br/>&emsp;For object detection, a type of deep neural network called a convolutional neural network (CNN) [19] has been widely used."
(Estrada et al., 2022)

> "In recent years, object detection methods such as the region-based convolutional neural network (RCNN) [22], you only look once (YOLO) [23], and single shot detector (SSD) [24] have been proposed."
(Estrada et al., 2022)

> "The final goal of deep learning-based object detection is to recognize and locate one or multiple objects in a specific frame."
(Ghasemi et al, 2022)

> "Deep learning-based object detection identifies the existing objects in an image or video and demonstrates where they are located (i.e., object localization) and which category they belong to (i.e., object classification)"
(Ghasemi et al, 2022)

> "Furthermore, image segmentation can be applied to assign particular class labels to each pixel of an image (Chen et al., 2014). The performance of image segmentation is hampered when one image includes multiple objects of the same class. To overcome this issue, instance segmentation was proposed to provide a pixel- level localization distinction among the objects by discerning between the objects of the same class."
(Ghasemi et al, 2022)

> "Object detection is important in computer vision since it intelligently identifies and analyzes a scene in a given frame. Depending on the context, the detection task can be divided into several categories, such as face detection, pose detection, and pedestrian detection, all of which have been used in various applications such as autonomous vehicles (Y. Li et al., 2020), robotics (Choi et al., 2022; Zhou et al., 2022; Chen et al., 2008), and security (Jain, 2019)."
(Ghasemi et al, 2022)

> "Convolutional neural networks or CNNs in short are the simplest and most widely used deep learning algorithms for object detection. In CNN, first, an image should be divided into separate pieces. The algorithm takes each of these pieces as the input and after going through convolutions and pooling layers, it outputs the objects’ classes."
(Ghasemi et al, 2022)

> "Region-based Convolutional Neural Network or R-CNN works on a specific number of regions. The algorithm extracts a group of boxes or Regions of Interest (ROI) using proposal methods such as Selective Search (Uijlings et al., 2013) in the frame and checks whether an object exists in that specific region."
(Ghasemi et al, 2022)

> "To use the R-CNN algorithm, first, it is required to choose a pre-trained convolutional neural network. Then, based on the number of classes that need to be detected, the network's last layer should be re-trained. Next, the regions should be reshaped to be matched to the network input size. After retrieving the regions, typical classifiers such as Support Vector Machine (SVM) can be used to classify the objects. Finally, techniques such as linear regression are used to assign a bounding box to each predicted class."
(Ghasemi et al, 2022)

> "Fast R-CNN has been proposed to reduce the computational time of the R-CNN algorithm (Girshick, 2015). In this method, after taking an image as the input, a convolutional neural network should be applied to generate the ROI."
(Ghasemi et al, 2022)

> "YOLO takes an image as the input and divides it into S×S grids to predict if there is an object in that specific cell. Using this information, YOLO can predict the class of the objects. Unlike region- based methods, which require thousands of neural networks, in YOLO, the input frame passes through a single network evaluation."
(Ghasemi et al, 2022)

> "Traditional object detection in AR mainly consists of marker-based methods and statistical classifiers."
(Ghasemi et al, 2022)

> "One of the first studies on picture properties and pictorial pattern recognition was introduced by Rosenfeld and Pfaltz (1966), which elaborates on computer processing pictorial information techniques"
(Ghasemi et al, 2022)

> "Another early work in this field is an image processing approach proposed by decomposing an image into primitive pieces as a basis for reference component description (Fischler and Elschlager, 1973). These studies were primarily based on matching techniques and part-based algorithms. Later studies focused on classifiers"
(Ghasemi et al, 2022)

> "Recent research in AR leveraged deep learning-based object detection to alleviate such challenges, either replacing traditional object detection methods or as a complementary component to mitigate their shortcomings"
(Ghasemi et al, 2022)

> "The main difference between the detection based on neural networks and statistical classifiers is that the user designs the latter. In contrast, in neural networks, the algorithm should learn a large sample of data to represent the response variable successfully"
(Ghasemi et al, 2022)

> "Previous studies on deep learning-based object detection in AR are centered on several areas including but not limited to education, manufacturing, aerospace, and robotics. Among all areas, manufacturing, autonomous vehicles, and assistance are more common."
(Ghasemi et al, 2022)

> "Fig. 3 shows an example of object detection results using (a) a traditional method (Viola-Jones) and (b) a deep learning-based method (YOLO)."
(Ghasemi et al, 2022)

(Ghasemi et al, 2022) Fig. 3:
<img src="https://i.imgur.com/hkrMXlj.jpeg">

> "Since mobile devices have become relatively powerful to handle the computations near real-time, Tobías et al. (2016) proposed a method in which three lightweight CNN algorithms including AlexNet, GoogLeNet, and NIN are used for object recognition on GPU, CPU, and mobile devices."
(Ghasemi et al, 2022)

> "MobileNet v2 reduced CNN, was more appropriate for embedded devices, since it reduces the processing delay and is optimized for low-performance computing devices such as smart glasses with Android OS."
(Ghasemi et al, 2022)

> "This study showed that AR devices with embedded processing units could reach a decent amount of frames per second which is satisfactory if the task does not require too many movements"
(Ghasemi et al, 2022)

> "Other variations of deep learning algorithms can be used to comply with less powerful devices processors. In Corneli et al. (2019), a lightweight variation of YOLO (i.e., tiny YOLO v2) was used to perform the whole process on site and in real-time."
(Ghasemi et al, 2022)

> "In this section, we are going to review some of the recent prominent machine/deep learning algorithms developed for various AR applications. Many of the deep learning based models for AR applications are focused on:
> - AR for Shopping (clothing try-on, makeup try-on)
> - AR for Face/Body Transformations
> - Tracking and Pose Estimation for AR Applications
> - AR for 3D human Reconstruction
> - Geometry Applications
> - Scene Understanding and Reconstruction"
(Minaee, Liang & Yan, 2022)

### 3.3 Augmented Reality (AR)
> "AR superimposes three-dimensional objects on the physical world, requiring the use of mobile devices to create interactions. MR is a technology that combines the physical and digital worlds to create immersive physical experiences. Users interact with both the physical and digital worlds by using their five senses."
(Estrada et al., 2022)

> "There are diverse types of AR suitable for different applications despite the fact that they all have similar capabilities [32,33]. Figure 1 depicts the two primary types of AR: marker-based AR and marker-less AR"
(Estrada et al., 2022)

> "Marker-based AR works when it is triggered by pre-defined markers. It allows the user to choose where to place the virtual object. Barcodes and QR codes are commonly used as images or photo symbols to be placed on flat surfaces. The program recognizes the marker when the mobile device focuses the target image."
(Estrada et al., 2022)

> "Marker-less AR collects data from the device hardware such as a camera, a GPS, a digital compass, and an accelerometer for the AR program to function. Marker-less AR applications rely on computer vision algorithms to distinguish objects, and they can function in the real world without specific markers [37,38]."
(Estrada et al., 2022)

> "Location-based AR: In this type of AR, simultaneous localization and mapping (SLAM) technology is used to track the user’s location as the map is generated and updated on the user’s mobile device"
(Estrada et al., 2022)

> "Superimposition-based AR: Superimposition-based AR applications can provide an additional view along with the original view of the object. Object recognition is required to determine the type of object to partially or completely replace an object in the user’s environment with a digital image [43,44]."
(Estrada et al., 2022)

> "Projection-based AR: Projection-based AR (also known as projection mapping and augmented spatial reality) is a technique that does not require the use of head-mounted or hand-held devices. This method allows augmented information to be viewed immediately from a natural perspective. Using projection mapping, projection-based AR turns an uneven surface into a projection screen."
(Estrada et al., 2022)

> "Vuforia’s Model Target is an example of outlining-based AR. Vuforia is a platform that enables developers to quickly incorporate AR technology into their applications. Model Targets allow apps to recognize and track real-world objects based on their shape"
(Estrada et al., 2022)

> "Augmented reality (AR) is a technology which allows superposition of information atop the real world and has been an evolving field of research since the mid-1990s. During the last decade, several portable and fully integrated AR devices have become available, providing the wearer with virtual 3D data integration into their environment" 
(Van Gestel et al, 2024)

> "AR can be defined as “a real-time direct or indirect view of a physical real world environment that has been enhanced/augmented by adding virtual computer generated information to it.” Therefore, AR is a novel way of superimposing digital contents into the real context."
(Reyes et al, 2016)

> "Generally, a marker-based MAR requires a marker to register the position of a virtual object to be displayed into the user's perceptions of the real world. The system operates on five items: (1) computing device; (2) software; (3) marker label; (4) camera; and (5) display device."
(Reyes et al, 2016)
MAR = Mobile AR

>"AR can be defined as an extended version of the physical world overlaid with digital content bridging the real and virtual environments. AR systems should accurately identify the real environment and its components to work best."
(Ghasemi et al, 2022)

> "There is a rapid growth of marker-based and markerless techniques to identify real-world content in AR systems"
(Ghasemi et al, 2022)

> "In marker-based AR, objects can be localized and tracked using physical markers attached to real objects."
(Ghasemi et al, 2022)

> "To overcome such limitations, markerless AR was proposed to recognize the real environment based on spatial geometry and does not require any trigger markers attached to the space. This technique often results in more accurate detections by obtaining the spatial map of the environment and its components. However, markerless applications need to recognize a textured flat surface to augment the digital content effectively."
(Ghasemi et al, 2022)

> "Deep learning techniques can overcome typical marker-based and markerless AR deficiencies and provide faster and more accurate detections."
(Ghasemi et al, 2022)

> "all AR devices consist of two elements: an image generating optical unit producing the virtual content, and a projection surface displaying the produced virtual content to the users."
(Ghasemi et al, 2022)

>"Augmented reality (AR) is an interactive experience of real-world environments, where the objects of the real world are enhanced by computer-generated perceptual information, sometimes across multiple modalities, including visual, auditory, haptic, and somatosensory"
(Minaee, Liang & Yan, 2022)

>"Hardware components for AR includes a processor, display, sensors and input devices. Modern mobile computing devices like smartphones and tablet computers contain these elements, making them suitable AR platforms"
(Minaee, Liang & Yan, 2022)

### 3.4 Prototypes Similar to Ours
> "we developed a mobile application, Ocul-AR, for microscopy teaching and support" 
(Pylvänäinen et al., 2023)

> "Ocul-AR was designed by a multidisciplinary team to guide microscopy students and users to learn about microscopy, optimize light paths and operate light microscopes independently"
(Pylvänäinen et al., 2023)

> "All respondents (n=11) reported that Ocul-AR helped them to learn hands-on microscopy (64% replied that the application helped definitely, 36% that it helped somewhat), as well as helped them to recall microscopy skills (90% definitely, 10% somewhat). Students who used Ocul-AR during the course felt they gained confidence to operate the microscope during the hands-on session (82% definitely, 18% somewhat) and that it lowered their threshold for using the microscope independently (70% definitely, 30% somewhat)."
(Pylvänäinen et al., 2023)

> "To our knowledge, there are no AR/VR-based mobile applications for higher education that teach microscopy with a step-by-step approach. <br/>&emsp;To facilitate the development of researchers' and students' proficiency in using microscopes easily and cost-effectively, we developed a mobile application called Ocul-AR. The main aims of Ocul-AR are to 1) teach students about microscopy, 2) aid during microscope operation, 3) help in troubleshooting unexpected issues, and 4) help refresh skills after extended periods of not using a microscope"
(Pylvänäinen et al., 2023)

> "Here we show that students who used Ocul-AR during a microscopy course gained more confidence to operate the microscope and that Ocul-AR lowered their threshold for using the microscope independently"
(Pylvänäinen et al., 2023)

> "a Needs assessment survey was sent by email to the students in order to investigate the biggest challenges when trying to use a microscope independently"
(Pylvänäinen et al., 2023)

> "All respondents showed interest in using a mobile application for learning microscopy, 70% very much and 30% maybe. Students were interested in a feature that would allow them to track their progress during learning and said that getting rewards would inspire them to continue learning by using the application."
(Pylvänäinen et al., 2023)

> "At Level 1, there are three categories: Teach me microscopy, Help me at the microscope and Help me to troubleshoot (Figure 2, Figure 3A)."
(Pylvänäinen et al., 2023)

> "The first level 1 category, Teach me microscopy, is intended mainly for independent studies before or during microscopy sessions. This section is further divided into three sections (Level 2); Virtual microscope, Test your knowledge and Learn more. The Virtual microscope contains a 3D model of a typical brightfield microscope, the Leica DM RXA microscope (Leica Microsystems), with an interactive tutorial about microscopy parts, how to set optimal Köhler alignment and how to focus on the sample (Figure 3B). This feature can also be used as a step-by-step guide while at this specific microscope."
(Pylvänäinen et al., 2023)

> "After pressing Help me at the microscope, the application opens an AR environment, where it is possible to scan markers or QR codes that have been attached to the microscope beforehand (Figure 3C). These markers guide the student in finding different parts of the microscope and their functions and switching the microscope on and off."
(Pylvänäinen et al., 2023)

> "As a result of the VR and AR features, students could engage with the microscope and access microscope-specific information from their homes or while physically using the equipment"
(Pylvänäinen et al., 2023)

> "While practical hands-on training cannot be entirely replaced, our solution can supplement it by providing additional support."
(Pylvänäinen et al., 2023)

> "Deep learning (DL) algorithms have achieved significantly high performance in object detection tasks. At the same time, augmented reality (AR) techniques are transforming the ways that we work and connect with people. With the increasing popularity of online and hybrid learning, we propose a new framework for improving students’ learning experiences with electrical engineering lab equipment by incorporating the abovementioned technologies."
(Estrada et al., 2022)

> "The DL powered automatic object detection component integrated into the AR application is designed to recognize equipment such as multimeter, oscilloscope, wave generator, and power supply."
(Estrada et al., 2022)

> "When a piece of equipment is detected, the corresponding AR-based tutorial will be displayed on the screen"
(Estrada et al., 2022)

> "Furthermore, to demonstrate practical application of the proposed framework, we develop a multimeter tutorial where virtual models are superimposed on real multimeters"
(Estrada et al., 2022)

> "This work explores the idea of using equipment recognition and an AR-based tutorial to enhance student learning experiences with electrical equipment in their engineering laboratories. Our long-term goal is to develop interactive smartphones apps for lab equipment such as multimeters, oscilloscopes, wave generators, and power supplies. Object detection using DL methods fits our goal because the app can detect specific electrical equipment in the lab with high precision in real-time using state-of-art DL algorithms"
(Estrada et al., 2022)

> "In this work, we are using a deep neural network to detect objects"
(Estrada et al., 2022)

> "In this paper, we compared RCNN and MobileNet-SSD v2 [26] and observed that MobileNet-SSD v2 has better performance for real-time applications in terms of speed when implemented on mobile devices. It is important to note that MobileNet-SSD v2 is a lightweight deep neural network architecture designed specifically for mobile devices with high recognition accuracy. Therefore, we employed MobileNet-SSD v2 in this work."
(Estrada et al., 2022)

> "In our project, we built a superimposition-based AR app. We built user interfaces on top of lab equipment, allowing step-by-step instructions to be incorporated into the application for users to understand and learn how to use specific equipment."
(Estrada et al., 2022)

> "The inference will classify and localize lab equipment that has been targeted with the mobile camera. When an object is detected, a user interface (UI) button appears, indicating that an AR-guided tutorial is available for the object. Then, an AR scenario will be loaded, allowing students to use their mobile camera to aim at a specific target. Following that, a 3D object will superimpose on top of the physical object, activating UI panels with instructions on how to use the equipment"
(Estrada et al., 2022)

BREAK BETWEEN SESSIONS HERE

> "In several orthopedic procedures, the accurate use of surgical power tools is critical to avoid damage to surrounding tissues. As such, various guidance techniques and safety measures were developed. Augmented reality (AR) guidance shows promise but requires validation. We evaluated a new approach using an inside-out infrared tracking solution for the HoloLens to compensate for its limited tracking performance."
(Van Gestel et al, 2024)

> "Eighteen participants with varying levels of experience (student, trainee, expert) each drilled twelve trajectories (six perpendicular, six oblique) in equidimensional wooden logs. Three different techniques were evaluated: freehand drilling; proprioception-guided drilling towards the contralateral index finger; and AR-guided drilling using a tracked drill and a virtual overlay of the log with predefined guidance vectors"
(Van Gestel et al, 2024)

> "The angular errors between planned and performed trajectories were compared using a mixed-design ANOVA"
(Van Gestel et al, 2024)

> "The results demonstrated that guidance technique (p < 0.001) and drilling direction (p < 0.001) significantly affected drilling accuracy, while experience (p = 0.75) did not. AR outperformed both other techniques, particularly for oblique trajectories (p < 0.001). For perpendicular trajectories, it only outperformed proprioception guidance (p = 0.04)."
(Van Gestel et al, 2024)

> "AR guidance using inside-out infrared tracking reduced angular uncertainty during directional drilling, resulting in improved drilling accuracy. This improvement was particularly noticeable for complex trajectories and angles. The benefits of AR guidance were observed across all experience levels, highlighting its potential for orthopedic applications"
(Van Gestel et al, 2024)

> ""Alternatively, conventional intraoperative navigation devices, using infrared tracking through a stereoscopic camera to provide a link between the physical world and imaging information (both pre- and intraoperatively obtained), have shown to improve surgical accuracy by allowing the surgeon or a robotic assistant to follow certain predefined trajectories and take the surrounding tissues into account^12,13,14^. Nevertheless, these systems are often bulky (with a sizeable screen, camera and/or computer unit), expensive, and time-consuming, limiting their use in orthopedic surgery^13,14^."
(Van Gestel et al, 2024)

> "head-mounted device (HMD)^15,16,17^. However, their tracking performance is a well-known limitation of such off-the-shelf hardware; often several centimeters, falling short of the millimeter scale tracking required for surgical navigation, leaving the advantage of AR guidance uncertain. 
<br />
To overcome these challenges in drilling based surgical tasks, we developed a navigation approach using the HoloLens (Microsoft Corporation, USA)^18,19,20,21,22^. With the goal of precise operative tracking in mind, several studies have adopted tracking of QR-code markers using the device’s integrated RGB sensor^18,23,24,25,26,27,28^. However, these markers are often large and difficult to integrate into a surgical workflow due to sterility requirements. Moreover, the RGB sensor within the HoloLens has a limited field of view which makes consistent tracking of these markers difficult^19^. Infrared-based tracking approaches, on the other hand, can be integrated easily thanks to the widespread use of infrared tracking by conventional navigation systems, while the HoloLens’ infrared sensor also provides a larger field of view."
(Van Gestel et al, 2024)

> "To address the off-the-shelf tracking limitations of the AR-HMD, we integrated prior work on inside-out tracking of infrared-reflective markers using the HoloLens’ on-board infrared sensor^19,20,21,22^. This allowed accurate tracking (mean tracking error of 0.78 mm ± 0.74 mm; unpublished Vicon validation testing) of instrumentation, and image registration (mean registration error of 1.42 mm ± 0.42 mm and 0.95° ± 0.36°; a cumulative error integrating – among others – the tracking error and the surgeon error)^22^."
(Van Gestel et al, 2024)

> "Each participant drilled 12 trajectories in equidimensional wooden logs measuring 60 × 500 mm."
(Van Gestel et al, 2024)

> "Each trajectory was defined by an “entry” and “exit” point in the same cross-sectional YZ-plane, with the Z-axis indicating the perpendicular drilling direction (Fig. [1](https://www.nature.com/articles/s41598-024-76132-3#Fig1)). All 12 exit points were aligned along the log’s longitudinal X-axis. Six of the entry points were located on a line opposite the exit points (perpendicular to the XY-plane). The six remaining points were located about 1 cm on each side of that line (oblique to the XY-plane). Entry and exit points were marked by a 2.5 mm predrilled cavity of 2 mm—3 mm depth to make them visible on CT scans. The wooden logs were securely fastened to a workbench, with all the exit holes at the lowest point of the log. To simulate limited exposure in the operating field, a fenestrated cloth covered the logs, revealing only the entry points."
(Van Gestel et al, 2024)

> "Each participant drilled two perpendicular and two oblique trajectories with each of the three guidance techniques: freehand drilling, proprioception-guided and AR-guided drilling. During freehand drilling, participants did not receive supplementary guidance other than the information they received beforehand. In the second setting, participants drilled based on tactile and proprioceptive feedback on the exit point using the contralateral index finger. For the AR guided technique, participants used the HoloLens to project an AR overlay of the predefined guidance vectors registered to the log (Fig. [2](https://www.nature.com/articles/s41598-024-76132-3#Fig2))."
(Van Gestel et al, 2024)

> "To register the virtual 3D model of the log and guidance vectors to the physical world, participants pointed the tip of the infrared-tracked stylus at each of the 12 entry points, as well as an additional point at each end of the log. We then employed a pose estimation technique using the point-pairs least squares optimization method to align the virtual and real-world objects. The quality of the registration was monitored by calculating the mean registration error between the 3D model and the 14 sampled points"
(Van Gestel et al, 2024)

> "During the AR drilling process, participants positioned the drill at the entry point and aligned the drill bit with the corresponding guidance vector. As soon as the trajectory of the drill matched the guidance vector within a tolerance of 4°, the color of the vector changed from red to orange. When the alignment was within 2°, the vector changed to green, indicating that the drilling direction was appropriate. Visual feedback helped in finding the correct direction. Throughout the drilling process, the color of the vector continued to indicate the alignment, while a virtual white sphere displayed at the drill tip allowed participants to monitor the drill’s advancement inside the log along the virtual trajectory (Fig. [2](https://www.nature.com/articles/s41598-024-76132-3#Fig2))."
(Van Gestel et al, 2024)

> "During the experiment, we assessed drilling performance in terms of error magnitude and error direction. To acquire these values, we respectively measured the radial distance (_r_) and polar angle (_θ_) of each exit point (_O_) in relation to the target point (_T_). Two blinded investigators (FVG, FVA) measured the values independently. If the measurements differed within 1 mm for _r_ and 5° for _θ_, we averaged the results. Otherwise, both investigators remeasured together and reached a consensus. An error magnitude below 0.1 mm without a discernable error direction was considered an on-target drilling performance."
(Van Gestel et al, 2024)

> "We used digital calipers (accuracy: 0.02 mm) to measure the shortest radial distance (_r_) between the centers of the targeted (_T_) and obtained (_O_) drill holes (Fig. [3](https://www.nature.com/articles/s41598-024-76132-3#Fig3)A). The deviation angle (α) between the planned (ET) and obtained (EO) trajectories, calculated"
(Van Gestel et al, 2024)

> "analyzing the error direction"
(Van Gestel et al, 2024)

> "Statistical analysis was divided into two parts: the first part analyzed deviation angle α, representing error magnitude, in terms of accuracy and precision, while the second part analyzed the spread of cartesian coordinates x, y, representing error direction. Categorical data were compared using a χ^2^ test. Statistical analyses were performed using SPSS Statistics software version 26 (International Business Machines Corporation, USA) and Prism 9.0.0 (GraphPad Software, USA) for graph creation. Significance was defined as p < 0.05."
(Van Gestel et al, 2024)

>"To assess performance accuracy, we compared deviation angle sizes as ratio variables using means, standard deviations (SD), minimums (Min), and maximums (Max). Given the collection of both between-subject (experience level) and within-subject factors (guidance technique, drilling direction, repeated measures), a mixed-design analysis of variance (ANOVA) with random intercepts was applied, considering _α_ as dependent variable and guidance technique, experience level, and drilling direction as predictors. Interactions between predictors were also analyzed"
(Van Gestel et al, 2024)

> "The level of reported experience with bone drilling (p = 0.011) as well as the age (p < 0.001) were correlated to the participants’ experience level, which was to be expected. This was not the case for the participants’ sex, nor their experience with the HoloLens. None of the participants had extensive experience with AR before the experiment, but 5/18 had used some form of AR before (Table [1](https://www.nature.com/articles/s41598-024-76132-3#Tab1))."
(Van Gestel et al, 2024)

> "The mean overall accuracy, i.e. the mean angular deviation between planned and achieved trajectories of all measurements (quantifying the extent of deviation from the target regardless of the size of the drilled medium), was 5.14° (SD: 4.04°, Min. 0.00°—Max. 21.44°). Accuracy was significantly impacted by the guidance technique (mixed-model ANOVA, p < 0.001) and the drilling direction (p < 0.001), but not by the level of experience (p = 0.75) (Table [2](https://www.nature.com/articles/s41598-024-76132-3#Tab2)). Only the interaction between guidance technique and drilling direction was significant (p = 0.037). Although there was no significant effect from the participants’ experience level, we noticed that experts had the best overall performance when using AR guidance, both for perpendicular trajectories at 2.81° (SD: 1.32°, Min. 0.00°—Max. 4.90°) and oblique trajectories at 2.96° (SD: 1.57°, Min. 0.82°—Max. 5.55°)."
(Van Gestel et al, 2024)

> "The pairwise tests, with Bonferroni correction for multiple comparisons, indicated that AR performed significantly better than both proprioception-guided and freehanded drilling (both pairwise comparisons: p < 0.001). However, there was no significant difference between proprioception-guided and freehanded drilling (p = 0.14)."
(Van Gestel et al, 2024)

> "Looking within each drilling direction subgroup, the results showed that for perpendicular drilling directions the accuracy obtained through AR guidance was significantly better than proprioception-guided drilling (p = 0.04), while for oblique drilling directions it outperformed both techniques (both p < 0.001)."
(Van Gestel et al, 2024)

> "Looking within each guidance technique subgroup, the difference between the accuracy for perpendicular versus oblique drilling directions was only significant in the proprioception-guided subgroup, in favor of perpendicular drilling directions (p < 0.001)."
(Van Gestel et al, 2024)

> "Out of a total of 216 drillings, 5 (2.31%) were on-target (r < 0.1 mm). None of the drillings were on-target in the freehand group, 1 in the proprioception group and 4 in the AR group (χ^2^, p = 0.074)."
(Van Gestel et al, 2024)

> "Overall, the mean precision of our experiment, i.e. the mean distance between the two achieved exit points with a same set of predictors (quantifying the proximity of these points), was 6.71 mm (SD 6.93 mm, Min. 0.11 mm—Max. 36.40 mm). In general, perpendicular drilling was more precise than oblique drilling (mixed-model ANOVA, p < 0.001). However, guidance technique (p = 0.56) or level of experience (p = 0.23) had no significant impact."
(Van Gestel et al, 2024)

> "during freehand and proprioception-guided drilling, the scatter along the Y-axis was larger than along the X-axis. This was especially true for oblique drilling. On the other hand, AR-guided drilling resulted in a visually smaller and more uniform scatter along both axes"
(Van Gestel et al, 2024)

> "The overall model showed a significant variance (p = 0.032), indicating large inter- and intra-participant performance variabilities. AR reduced those variabilities, especially for the outliers"
(Van Gestel et al, 2024)

> "The use of AR guidance for directional drilling yielded a higher angular accuracy compared to freehand and proprioceptive guidance. Regardless of experience, AR reduced the angular error by nearly half and led to more on-target drilling outcomes. Particularly in oblique drilling, AR proved highly beneficial, greatly reducing scatter along the Y-axis. This can be attributed to the intuitive ease of drilling perpendicularly based on visual information, as opposed to drilling along a less clearly defined path."
(Van Gestel et al, 2024)

> "Another limitation was our focus solely on the final cumulative error, without considering the tracking error by the AR system and the registration error by the participant. Though internal testing found the tracking error to be sufficiently low (0.78 mm ± 0.74 mm), the registration error could introduce variability as it was performed by each participant individually. Nonetheless, considering that this step is common in navigated surgeries and contributes to the overall system performance, we believe it should be acknowledged as an inherent part of the final error."
(Van Gestel et al, 2024)

> "Nevertheless, AR presents a promising alternative to the existing navigation systems, which lack the ergonomics and ease-of-use for widespread adoption in orthopedic surgery. By utilizing AR HMDs with inside-out tracking, navigation could become more lightweight and cost-effective, potentially mitigating line-of-sight issues^24^. Furthermore, the compact size of AR HMDs opens up possibilities for exploring applications beyond the operating room."
(Van Gestel et al, 2024)

> "Lastly, before AR can be widely adopted in everyday surgical settings, it needs to undergo validation in a more clinical environment, such as testing on anatomical specimens, performing a direct comparison with gold-standard navigation solutions, optimizing the user interface for the operating room environment, and conducting performance evaluations through patient trials^37^."
(Van Gestel et al, 2024)

> "This paper proposes a mobile augmented reality (MAR) system aimed to support students in the use of a milling and lathe machines at a university manufacturing laboratory. The system incorporates 3D models of machinery and tools, text instructions, animations and videos with real processes to enrich the information obtained from the real world"
(Reyes et al, 2016)

> "The main goals of the project were (1) create an AR system that guides inexperienced users in machinery handling and (2) measure the acceptance rate and performance of the system in the school manufacturing laboratory"
(Reyes et al, 2016)

> "The system was implemented as a mobile app for Android devices and it was tested by 16 students and teachers at the university manufacturing laboratory through a survey"
(Reyes et al, 2016)

> "The proposed MAR system includes a tutorial on how to perform the basic tasks of tools setup, setup of working material, and machinery setup and start up for a milling and a lathe machine. The goal is to support students in machinery handling by providing virtual information (augmented) in real time."
(Reyes et al, 2016)

> "The augmented elements encompass (1) 3D models of machinery and tools such as spanners and Allen wrenches. (2) Text instructions to describe how to perform the basic tasks. (3) Labels, which help the user for locating machinery components and tools. (4) 3D arrows to indicate flow direction. (5) Real time videos that include task explanations performed by experts"
(Reyes et al, 2016)

> "In the first stage, a computing device to perform the typical AR processes such as rendering, recognition, and tracking is needed. Additionally, a display device for displaying the mixture of real and virtual content is also necessary.
<br />
When somebody is handling the machinery, it is important to keep both hands free to perform the tasks with accuracy and security. In the first stage, it is important selecting a hardware device that can meet this necessity. The smart phones were discarded because the user need holding the device with the hands to observe the AR"
(Reyes et al, 2016)

>"Two hardware devices were selected to implement and test the MAR system. The first one, consists of an optical see-through glasses where the real world is observed through transparent mirrors placed in front of the eyes of the user"
(Reyes et al, 2016)

> "The second one, consists of a video see-through HMD, where the real world view is captured with a video camera mounted on the head gear"
(Reyes et al, 2016)

> "For this research, a marker-based MAR system was developed. A marker system was selected due to the less computational power required to process each frame obtained from the camera of the hardware device. The markers are composed by defined patterns that are introduced in the real environment and are automatically recognized using the computer vision algorithms."
(Reyes et al, 2016)

> "FM and IT were used for three different purposes: (1) detect the machinery; (2) show machinery tools; and (3) show explanation videos to the user. Recognizing the machinery was made by scanning a specific IT defined for every machine, Figure [5](https://onlinelibrary.wiley.com/doi/full/10.1002/cae.21772#cae21772-fig-0005)c for the case of lathe, and Figure [5](https://onlinelibrary.wiley.com/doi/full/10.1002/cae.21772#cae21772-fig-0005)d for the case of milling"
(Reyes et al, 2016)
FM and IT: different kind of Vuforia AR-markers

> "At the beginning, the user needs to run the application and point the camera of the device to the main menu marker, which is an augmented menu as it is shown in Figure [5](https://onlinelibrary.wiley.com/doi/full/10.1002/cae.21772#cae21772-fig-0005)a. The menu displays two options: (1) start the application and (2) get system help information. By selecting the start button, the user can proceed to scan the marker ID corresponding to the machine that will be used, by pointing the device camera to the marker. On the other hand, by selecting the help option, the user will receive all the instructions to use the application. After scanning the ID, the corresponding machine tutorial (lathe or milling) starts and the lesson markers are activated. By pointing the camera of the device to one of the lessons markers (Fig. [5](https://onlinelibrary.wiley.com/doi/full/10.1002/cae.21772#cae21772-fig-0005)e–h), the related multimedia content is displayed to the user"
(Reyes et al, 2016)

> "Animations, 3D models, and instructions were used to explain to the user how to setup pieces, tools, and machines. The videos (Fig. [5](https://onlinelibrary.wiley.com/doi/full/10.1002/cae.21772#cae21772-fig-0005)b) were used to explain very complex tasks, or tasks where markers could not be placed, for example low places of the machine or recurrent moving parts."
(Reyes et al, 2016)

> "The complete flow diagram of the MAR system is shown in Figure [7](https://onlinelibrary.wiley.com/doi/full/10.1002/cae.21772#cae21772-fig-0007)."
(Reyes et al, 2016)

> "All the lessons presented in the system are shown in Table [3](https://onlinelibrary.wiley.com/doi/full/10.1002/cae.21772#cae21772-tbl-0003 "Link to table")."
(Reyes et al, 2016)

> "All the elements presented were introduced in a GUI, where the users can interact with the whole system."
(Reyes et al, 2016)

> "A total of 16 persons randomly selected at UACJ manufacturing laboratory participated in the study. The group was composed by students enrolled in mechatronics engineering, with an average age of 25 years. Although the main interest of the system is on students, school teachers and laboratory technicians were also included in the group. The experiments were performed to measure and asses the acceptance and performance, as an alternative learning tool, of the “MAR manufacturing tutor.”"
(Reyes et al, 2016)

> "An introduction to AR and the basic operation of the MAR system was offered to the group, and immediately each person had the opportunity to test the system using one of the devices (ORA-1 AR glasses or VR-PRO). The participants were able to test each of the lessons and then answer a survey."
(Reyes et al, 2016)

> "The items of the survey applied to the participants are shown in Table [4](https://onlinelibrary.wiley.com/doi/full/10.1002/cae.21772#cae21772-tbl-0004 "Link to table")."
(Reyes et al, 2016)

> "The results obtained for each question are shown in Table [5](https://onlinelibrary.wiley.com/doi/full/10.1002/cae.21772#cae21772-tbl-0005 "Link to table")."
(Reyes et al, 2016)

> "The percentages of response for each question are depicted in Figure [8](https://onlinelibrary.wiley.com/doi/full/10.1002/cae.21772#cae21772-fig-0008)."
(Reyes et al, 2016)

> "It should be noted from Figure [8](https://onlinelibrary.wiley.com/doi/full/10.1002/cae.21772#cae21772-fig-0008) that most of the characteristics of the system were rated as good or above by comparing both sides of the zero line."
(Reyes et al, 2016)

> "In terms of percentages, and by adding the blue bars in the plot, it should be noted that 75% of the respondents rated as good/very good the experience satisfaction while using the system, the system speed and thought that the information given by the system was precise and explanatory. Moreover, 93.75% of the people qualifies as good the understandability of the information offered by the system, and 87.5% qualify as good the system attractiveness. Talking about system interface, only 50% of the people rated the interface as good, which means that a system enhancement stage is imperative. Finally, 81.25% said that markers detection was good as well."
(Reyes et al, 2016)

> "Two plots were created by dividing the survey items in two groups: (1) questions 1–5 belonging to system acceptance and (2) questions 5–8 belonging to system performance"
(Reyes et al, 2016)

> "For the case of system acceptance, the Figure [9](https://onlinelibrary.wiley.com/doi/full/10.1002/cae.21772#cae21772-fig-0009) shows that central tendency was rating the system as good by obtaining a median value of 4.0"
(Reyes et al, 2016)

> "On the other hand, talking about performance, it should be noted from Figure [10](https://onlinelibrary.wiley.com/doi/full/10.1002/cae.21772#cae21772-fig-0010) that the GUI was the least rated characteristic with a median of 3.5. The users did not consider the interface and menu navigation very easy to use. However, speed and marker system were well rated by obtaining a median of 4 and 4.5, respectively, meaning that system speed was good and markers detection was fast."
(Reyes et al, 2016)

> "In addition, several opinions from the participants regarding to system characteristics, usability, performance, and some suggestions were obtained with question 10. It is important to mention that four persons in charge of the manufacturing laboratory including class teachers and technicians, were very interested in using the system as a teaching–learning tool"
(Reyes et al, 2016)

> "Based on the results and opinions offered, it was observed that most of the students rated the system as a valuable and appealing tool to learn the basics about lathe and milling manipulation"
(Reyes et al, 2016)

> "First of all, the system could be a potential teaching–learning tool, when it will be used in everyday laboratory scenario"
(Reyes et al, 2016)

> "Moreover, the system represents a real possibility to expand the machinery handling support offered by the instructor."
(Reyes et al, 2016)

> "Regards to student collaboration, we noticed that it will be difficult for two or more students manipulating the system at the same time. This is mainly because markers have to be pointed from a minimum distance, and angle to be detected, and display objects correctly"
(Reyes et al, 2016)

> "Finally, we detected that students can put a lot of attention in the AR system and ignore important parts of the experience (attention tunneling effect)."
(Reyes et al, 2016)

>"this research used augmented reality (AR) technology to simulate the complete operation flow and processing information of CNC processing machines, and combined the practical teaching courses to deepen the students’ understanding of CNC machine operation"
(Lin & Lee, 2020)

>"In this study, a total of ten participants were recruited to conduct AR system operation experiments"
(Lin & Lee, 2020)

>"The follow-up verification was conducted through real CNC machine operation and by filling in the System Usability Scale (SUS) to evaluate the experience feedback after using the AR-CNC training system"
(Lin & Lee, 2020)

>"due to the limited number of machines and insufficient space in teaching, students can only learn the knowledge and application of CNC machining by rotating operation or by watching the operation of teachers"
(Lin & Lee, 2020)

>"AR technology can be applied to the simulated operation of CNC machines. Students can use a personal tablet computer to perform a two-stage operation simulation in the factory classroom and the CNC machine. The built-in virtual imaging technology can superimpose virtual 3D machining workpieces on the physical CNC machine"
(Lin & Lee, 2020)

>"In addition, in the process of machine processing, a large amount of processing materials and machine tool wear are required, which results in the students only creating a piece of furniture in a group in order to save materials and reduce the storage space of finished furniture products, and the students cannot conduct multiple processing or diversified furniture production trials"
(Lin & Lee, 2020)

>"However, under the application of AR or virtual reality (VR), the machining process and machine operation can be simulated through a virtual CNC machine to simulate the actual machining situation"
(Lin & Lee, 2020)

>"The simulated operation process can solve many problems, including:"
...
"4) the 3D machining workpieces created by the processing software do not correspond to the actual machine during processing in space, and students cannot see the operation relationship and correspondence between the processing object and the software or the machine in real time"
(Lin & Lee, 2020)

>"All the processing details include different processes and methods, such as turning over processing, mold hole processing, and so on. It is difficult to express and explain concepts in a traditional 2D video image, but AR solves this problem. AR can especially allow students to superimpose 3D objects in the space of the CNC operating machine."
(Lin & Lee, 2020)

>"Students are unfamiliar with the use of machining tools and methods and it is difficult to directly see the relationship between the 2D tool path and the 3D machining workpiece). AR can effectively help learners understand the scale relationship of a 3D machining space, including the relationship between the machining machine and the workpiece (furniture parts). It can let students understand how to turn the surface or process the surface by superposing the virtual 3D processing workpiece onto solid wood or the solid workpiece itself. That is to say, the virtual object constructed by AR provides additional auxiliary information to strengthen the students’ cognition of the concept of workpiece turnover and the 3D processing space"
(Lin & Lee, 2020)

>"This study recruited ten students with experience in operating CNC to conduct the AR system operation"
(Lin & Lee, 2020)

> "The participants had previous CNC machine operation experience but were still unfamiliar with CNC machine operation procedures"
(Lin & Lee, 2020)

>"During the experiment, the students conducted AR machine operation training in groups, presented the AR system in the form of a tablet computer, and used the finished furniture product example of an online open CNC furniture company as the demonstration material for CNC machine learning"
(Lin & Lee, 2020)

>"The AR-CNC training system was developed to allow the students to learn independently and allow the operation of the machine and the control console to both be more clearly understood and practiced. The students experienced the operation of the CNC machine and the content of the furniture processing workpiece through the tablet computer in both the general classroom space and the actual factory space"
(Lin & Lee, 2020)

>"The AR-CNC training system could display the spatial relationship of the 3D virtual processing object and the real machine by using a tablet or a hand-held device. At the same time, it was similar to the environment in which the real machine operated, and it was in the actual teaching field show in Fig. [4](https://link.springer.com/chapter/10.1007/978-3-030-49698-2_9#Fig4)."
(Lin & Lee, 2020)

>"the operation process is shown in Fig. [5](https://link.springer.com/chapter/10.1007/978-3-030-49698-2_9#Fig5)."
(Lin & Lee, 2020)

>"Ten participants first operated the CNC woodworking engraving machine using a tablet. The course was mainly divided into the following six unit topics: 1) CNC machine introduction; 2) CNC machining application examples; 3) introduction of the AR teaching machine interface operation and simulation; 4) AR machine simulation processing and CNC machining operation practice; 5) making knock-down furniture (KD) furniture; and 6) finished products and other complete digital manufacturing processes. After training, the ten subjects were given the System Usability Scale (SUS) questionnaire to offer feedback for the analysis of the results and data."
(Lin & Lee, 2020)

>"In the questionnaire survey of this study, the researcher scored the system usability scale of AR-CNC system and established five different evaluation dimensions after expert interviews, including “Understanding of Machining Procedures”, “Time of Operation”, “Accuracy of Operation”, “Sequence and Information of the CNC Operation Steps”, “Understanding of the Interface Knowledge of the CNC Cutting Machine Center”, and other evaluation aspects. Each facet had five sub-questions for a total of twenty questions, and each topic was given a score of 1–7 (in which 1 represented high difficulty and 7 represented low difficulty)."
(Lin & Lee, 2020)

>"The results showed that in the aspect of Understanding of Machining Procedures, the participants believed that the AR-CNC system could improve their understanding of workpiece processing (4.86 points). In the aspect of Time of Operation, the participants thought that the AR-CNC system could make CNC learning more efficient (4.8 points).
<br/>
In the aspect of Sequence and Information of the CNC Operation Steps, the participants thought that the AR-CNC system could let them complete every operation step and task (5.52 points). In the aspect of Accuracy of Operation, the participants thought that the AR-CNC system could help them learn and improve their learning motivation (4.98 points). Finally, in the aspect of Understanding of the Interface Knowledge of the CNC Cutting Machine Center, the participants believed that the AR-CNC system could help to understand the functions corresponding to machine processing (5.6 points)."
(Lin & Lee, 2020)

>"The research results showed that the students could understand the relationship between workpieces and methods on the CNC machining through the AR system and could operate virtual machines through AR simulation"
(Lin & Lee, 2020)

>"After the AR machine operation training, this study confirmed that using the AR system for training had a number of advantages. First, through the AR teaching system, the students could understand the complete processing procedures and steps of woodworking furniture machine operation"
...
"Second, using AR for interactive learning allowed the students to smoothly integrate virtual and real concepts between the real processing operation environment and virtual 3D processing objects"
...
"Third, the AR system had a simple operation mode, and the students did not need to be instructed by the teacher. Even if the trainees did not have any previous experience with CNC processing machines, they could quickly understand the operation process and processing concepts. The trainees could learn and operate independently without imagination how to use CNC processing machine. Fourth, the AR system allowed the students to practice repeatedly and avoid unnecessary material waste in actual processing as well as safety concerns in operation. Fifth, the virtual 3D picture of the CNC cutting path could be previewed through AR, and the processing stage and additional production information could be understood"
(Lin & Lee, 2020)

## 4 Architecture Description

### 4.1 Perceived Challenges

> "However, implementation issues on mobile devices remains a challenge that need to be optimized to reduce computational time and improve the effectiveness of the algorithms to make them more lightweight, fast, and accurate"
(Ghasemi et al, 2022)

> "In general, energy consumption is the primary concern for mobile AR applications"
(Ghasemi et al, 2022)

> "Additional work must be done to reduce the detection and segmentation execution time."
(Ghasemi et al, 2022)

> "Another challenge is dealing with the limitations of wearable devices such as HoloLens. HoloLens’s hardware is unpleasant and uncomfortable for prolonged durations of wear. Also, HoloLens has a limited battery capacity and sometimes requires continuous and stable access to the network."
(Ghasemi et al, 2022)

> "Another limitation that needs more improvement is detection accuracy when there is a reflective medium or a shiny surface such as glass in the environment. The detection also may fail when the object being scanned moves."
(Ghasemi et al, 2022)

### (4.1.5 Technical details of prototypes)
This could be displayed as a table for example

> "The source code for the application was written in the Unity 2020.3.3 real-time development platform using the C# programming language, resulting in a mobile application based around a singleton class that manages various application states"
(Pylvänäinen et al., 2023)

> "The AR feature was implemented using EasyAR Sense 4.4. Quick response (QR) code markers placed on different parts of the microscope allow the user to scan and retrieve information about specific parts"
(Pylvänäinen et al., 2023)

> "The application was designed to run on the Android mobile operating system and was distributed to end-user devices via Android Package (APK) files."
(Pylvänäinen et al., 2023)

> "A deep neural network model, namely MobileNet-SSD v2, is implemented for equipment detection using TensorFlow’s object detection API"
(Estrada et al., 2022)

> "The Unity3D game engine is used as the primary development tool for this tutorial to integrate DL and AR frameworks and create immersive scenarios"
(Estrada et al., 2022)

> "Unity 3D combines the output of these systems by inferring the object detection model with OpenCV and using an AR dataset target with a Vuforia Engine. Furthermore, Unity 3D enables the development of interactive user interfaces"
(Estrada et al., 2022)

<img src="https://www.mdpi.com/applsci/applsci-12-05159/article_deploy/html/images/applsci-12-05159-g002-550.jpg">
(Estrada et al., 2022)

> "The development framework was integrated with a MobileNet-SSD DL model and a marker-less superimposition AR that activates immersive modules containing 2D/3D objects"
(Estrada et al., 2022)

> "MobileNet-SSDv2 [26] architecture was used to build a deep neural network model to detect electrical lab equipment. The architecture comprised MobileNet-v2 as the backbone network, an SSD detector, and feature pyramid network (FPN)"
(Estrada et al., 2022)

> "We developed a software workflow for AR-guided drilling on the HoloLens using the Unity development platform (Unity Technologies, USA). The process involved acquiring a CT scan of the wooden logs using a standard preoperative diagnostics protocol: CT scanner, SOMATOM Definition AS (Siemens, Munich, Germany);"
(Van Gestel et al, 2024)

> "From this scan, we generated a 3D surface model of the log and created virtual guidance vectors between the entry and exit points using the open-source 3D Slicer software package (version 4.10, [http://www.slicer.org](http://www.slicer.org))."
(Van Gestel et al, 2024)

> "To track the physical objects, including the log, the drill, and a stylus, we equipped them with a unique constellation of five disposable infrared-reflective marker spheres (Northern Digital Incorporated, Canada), which was tracked by the infrared camera of the HoloLens."
(Van Gestel et al, 2024)

> "In order to give the system the abilities to recognize and track the markers, Vuforia software developer kit (SDK) libraries were selected. Additionally, the Blender 3D graphics software was selected to create the virtual models that will be associated to each marker."
(Reyes et al, 2016)

> "On the other hand, the game creator engine Unity 3D was used to mix Vuforia computer vision algorithms, the AR markers, and the virtual objects created in blender"
(Reyes et al, 2016)

> "In Figure [3](https://onlinelibrary.wiley.com/doi/full/10.1002/cae.21772#cae21772-fig-0003), the architecture of the software system is shown"
(Reyes et al, 2016)

> "Two different kinds of markers, from the set offered by Vuforia, were selected to create the MAR system. The frame markers (FM) are default patterns with a binary code in the boundary. Vuforia includes 512 default FM which are incorporated in the SDK"
(Reyes et al, 2016)

> ". On the other hand, the image targets (IT) are 2D real world images defined by the user which are processed by Vuforia to detect features such as borders, corners, among others."
(Reyes et al, 2016)

> "Objects such as specific keypads or control pads of the machinery were selected as ITs, due that they are flat objects and also have defined characteristics that can be detected by Vuforia"
(Reyes et al, 2016)

> "ITs were stored in a local database"
(Reyes et al, 2016)

> "The main purpose and advantage of using Unity 3D was its integration with Vuforia and Blender. Unity allows to integrate Vuforia markers and *.blend files generated from Blender and set their position, rotation, and size regard to the markers."
(Reyes et al, 2016)

> "The application can run on devices with Android operating system 4.2.1 and up."
(Reyes et al, 2016)

> "The AR-CNC training system in Fig. [3](https://link.springer.com/chapter/10.1007/978-3-030-49698-2_9#Fig3) mainly used a tablet computer as a carrier for teaching and operation"
(Lin & Lee, 2020)

>"In the AR-CNC training system, Adobe Illustrator was used to draw 2D identification cards, and software such as C4D/3D MAX was used to make 3D animations. The system was developed through Unity and Vuforia to integrate and define actions"
(Lin & Lee, 2020)

## 6 Usability

### (6.1 Usability in prototypes)
> "All the participants indicated that the Ocul-AR application was aesthetically pleasing and simple to navigate. The participants noted that the application was appropriate for novice users but suggested that it should include more advanced content if intended for advanced users."
(Pylvänäinen et al., 2023)

<img src="https://cdn.discordapp.com/attachments/524629394208325642/1346074587619655690/image.png?ex=67c6dd26&is=67c58ba6&hm=562b16e90f7f502e7d35cf26b983db6e1e71e13dad0105470179cd66ffd5b130&">
(Pylvänäinen et al., 2023)

> "Following their initial independent use of the microscope supported by the Ocul-AR application, all participants reported that the application helped facilitate their understanding of microscopy. Specifically, 64% of participants reported that the application was definitely helpful, while 36% reported that it was somewhat helpful."
(Pylvänäinen et al., 2023)

> "3.4. Phase 2 results: Self-study with Ocul-AR application by the microscope helps students to follow the conventional microscopy hands-on training"
(Pylvänäinen et al., 2023)

> "Pilot study phase 3 was conducted to evaluate the long-term effectiveness of Ocul-AR in learning microscopy. During this phase, students were requested to perform the same tasks as in phase 1, but after a gap of three months following the guided hands-on session of the course"
(Pylvänäinen et al., 2023)

> "As the application was used for these specific tasks during teaching, the students reported that it was a familiar resource for revising how to perform these tasks. 64 % of the students felt that the Ocul-AR application definitely helped them in becoming independent microscopy users, whereas 27 % reported that the application helped somewhat. 9 % of the students felt that Ocul-AR did not significantly help them in becoming independent microscopy users"
(Pylvänäinen et al., 2023)

> "Firstly, in the authors’ experience, the use of the HoloLens by individuals with glasses is challenging at times, depending on the wearer’s corrective lens frame geometry"
(Van Gestel et al, 2024)

> "Additionally, visualization design can have an important influence on performance"
(Van Gestel et al, 2024)

> "At the end of the experiment which lasted 10 min (time used only to test the system, and not the time used to fulfill the survey), some students showed eyestrain, especially those students who usually used lenses. Also, students who used ORA-1 glasses show more visual tiredness than those who used VR-PRO. The students mentioned that they started to have problems with focusing after a short period of time while using ORA-1"
(Reyes et al, 2016)

> "In addition, improvements in AR glasses interaction can be added, by using speech recognition and voice navigation, instead of using the touch interface"
(Reyes et al, 2016)

