# PhD Research

I worked with Prof. Victoria Interrante, my PhD advisor, on a variety of interesting and challenging subjects during my time at the University of Minnesota. My research interests focused on Non-Photo realistic Rendering (NPR) in Virtual Reality (VR) and Augmented Reality (AR), Video-See-Through (VST) Head-Mounted Displays (HMDs), Multi-Person Collaboration in VR, Visual Perception, Distance Underestimation, Spatial Disorientation, Cybersickness, and Human-Computer Interaction (HCI). All the official papers and publications can be found on the [publications page](https://www.kvaziri.com/publications/), but here you will find some more details about my research.

### Distance Underestimation Research with NPR VST System

From 2014 to 2017, my main research focus was to further understand distance underestimation problem in virtual environments and resulted in two publications.

First paper, published by the Association of Computer Machinery (ACM) Symposium on Applied Perception (SAP) in 2017, was an interesting multi-disciplinary project with many hands-on experiences with 3D modeling and design, 3D-printing, coding software, designing hardware, visual perception, cognition, and running human-subject user studies. This paper showed that using basic NPR filters can maintain spatial integrity in architectural environments. However, since the user study was performed indoors inside the University’s library hallways, peer reviewers were concerned about spatial clues of the environment, like perspective or doors, which gave us the opportunity to work on the second paper in an outdoor open field environment. 

The second paper was published by IEEEVR in 2021, and showed that even in reduced-cue environments, NPR can maintain spatial integrity. Even more interestingly, we found that removing all the context around the target did not significantly reduce distance accuracy probably because of the angular declination of the target itself.

Here, you will find some additional details that was not covered extensively in the papers to the maximum length criteria of most conferences and journals.

For the first project, we created a portable custom VST system based on an nVisor ST50. This special HMD is dual-purpose: VR with its removable blinder and AR through its Optical-See-Through (OST) by removing that piece. This fact allowed us to create a custom 3D-printed camera mount and calibrate our camera views to near perfect registrations with the real-world which is not easily done with other VR-only HMDs currently on the market like Oculus Rift and HTC Vibe. Also at this point, Microsoft HoloLens has a very narrow field-of-view (FOV) which is not perfect for distance perception studies. By using nVisor ST50, we were able to simply 3D-print half of the camera mount and superimpose one camera image on the see-through LCD and observe the difference between these images and correct the magnification and misalignments.

<img src="assets/nvis_st50.jpg" height="100"> <img src="assets/nvis_blinder.jpg" height="100"> <img src="assets/mount_model.jpg" height="100"> <img src="assets/mount_half.jpg" height="100"> <img src="assets/vst_side.jpg" height="100"> <img src="assets/vst_front.jpg" height="100">

Our custom camera mount also has rails on top and bottom in order for the cameras to move and shift sideways, so we can individually adjust them to every participants’ interpupillary eye distance (IPD) to eliminate parallax in horizontal and vertical axes. Our system has parallax in depth axis, but it can be shown mathematically that for distance above 10 feet, it is negligible.

<img src="assets/ipd_test.jpg" height="100"> <img src="assets/vst_calibration_1.jpg" height="100"> <img src="assets/vst_calibration_2.jpg" height="100">

My years of experience in building gaming computer for family and friends finally was paid off when we decided to make our VST system more portable. I got to design and build a backpack computer case from scratch. Back of this case is designed in such fashion that it can be bolt into a standard A.L.I.C.E. (All-purpose Lightweight Individual Carrying Equipment) backpack frame with wing-nuts. We used an NVidia GTX-1080 card which is more than enough to render into two HMD screens with high frame rates, an Asus Maximus VIII Mini-ITX mainboard with built-in Wi-Fi, Intel 750 U.2 nVMe SSD, and Intel i7 6700K CPU. This case weighed about 11.5 lb. and about 15 lb. with ALICE frame.

<img src="assets/backpack_1.jpg" height="100"> <img src="assets/backpack_2.jpg" height="100"> <img src="assets/backpack_3.jpg" height="100"> <img src="assets/backpack_4.jpg" height="100"> <img src="assets/backpack_5.jpg" height="100">

Participants in our study viewed three different environments in three different hallways: Real-World through the HMDs OST display, unprocessed VST view with our camera mount, and NPR processed VST view filtered with Sobel edges. Participants were given 2 warmup distances at 4.5 and 6.5 meters in each environment, and then each trial had 4 more readings at 4, 5, 6, and 7 meters which their order of appearance was randomized. The order of views were also shuffled so no two participant had the same order and each view could appear in different hallways.

<img src="assets/environment_1.jpg" height="100"> <img src="assets/environment_2.jpg" height="100"> <img src="assets/environment_3.jpg" height="100"> <img src="assets/environment_4.jpg" height="100">

For measuring the distance, we first found the starting position on the floor
