# PhD Research

I worked with Prof. Victoria Interrante, my PhD advisor, on a variety of interesting and challenging subjects during my time at the University of Minnesota. My research interests focused on Non-Photo realistic Rendering (NPR) in Virtual Reality (VR) and Augmented Reality (AR), Video-See-Through (VST) Head-Mounted Displays (HMDs), Multi-Person Collaboration in VR, Visual Perception, Distance Underestimation, Spatial Disorientation, Cybersickness, and Human-Computer Interaction (HCI). All the official papers and publications can be found on the [publications page](https://www.kvaziri.com/publications/), but here you will find some more details about my research.

### Distance Underestimation Research with NPR VST System

From 2014 to 2017, my main research focus was to further understand distance underestimation problem in virtual environments and resulted in two publications.

First paper, published by the Association of Computer Machinery (ACM) Symposium on Applied Perception (SAP) in 2017, was an interesting multi-disciplinary project with many hands-on experiences with 3D modeling and design, 3D-printing, coding software, designing hardware, visual perception, cognition, and running human-subject user studies. This paper showed that using basic NPR filters can maintain spatial integrity in architectural environments. However, since the user study was performed indoors inside the University’s library hallways, peer reviewers were concerned about spatial clues of the environment, like perspective or doors, which gave us the opportunity to work on the second paper in an outdoor open field environment.

The second paper was published by IEEEVR in 2021, and showed that even in reduced-cue environments, NPR can maintain spatial integrity. Even more interestingly, we found that removing all the context around the target did not significantly reduce distance accuracy probably because of the angular declination of the target itself.

Here, you will find some additional details that was not covered extensively in the papers to the maximum length criteria of most conferences and journals.

For the first project, we created a portable custom VST system based on an nVisor ST50. This special HMD is dual-purpose: VR with its removable blinder and AR through its Optical-See-Through (OST) by removing that piece. This fact allowed us to create a custom 3D-printed camera mount and calibrate our camera views to near perfect registrations with the real-world which is not easily done with other VR-only HMDs currently on the market like Oculus Rift and HTC Vibe. Also at this point, Microsoft HoloLens has a very narrow field-of-view (FOV) which is not perfect for distance perception studies. By using nVisor ST50, we were able to simply 3D-print half of the camera mount and superimpose one camera image on the see-through LCD and observe the difference between these images and correct the magnification and misalignments.

<img src="assets/nvis_st50.jpg" height="100"> <img src="assets/vst_system_camera_mount.jpg" height="100"> <img src="assets/vst_camera_mount_model_3a.png" height="100"> <img src="assets/vst_camera_mount_half_print.jpg" height="100"> <img src="assets/vst_angle_adjustment_pic1.jpg" height="100"> <img src="assets/vst_bracket_adjustments.jpg" height="100">

Our custom camera mount also has rails on top and bottom in order for the cameras to move and shift sideways, so we can individually adjust them to every participants’ interpupillary eye distance (IPD) to eliminate parallax in horizontal and vertical axes. Our system has parallax in depth axis, but it can be shown mathematically that for distance above 10 feet, it is negligible.

<img src="assets/vst_camera_bracket.jpg" height="100"> <img src="assets/vst_ipd_adjustments.jpg" height="100"> <img src="assets/vst_system_in_use.jpg" height="100">

### Custom Backpack PC

My years of experience in building gaming computer for family and friends finally was paid off when we decided to make our VST system more portable. I got to design and build a backpack computer case from scratch. Back of this case is designed in such fashion that it can be bolt into a standard A.L.I.C.E. (All-purpose Lightweight Individual Carrying Equipment) backpack frame with wing-nuts. We used an NVidia GTX-1080 card which is more than enough to render into two HMD screens with high frame rates, an Asus Maximus VIII Mini-ITX mainboard with built-in Wi-Fi, Intel 750 U.2 nVMe SSD, and Intel i7 6700K CPU. This case weighed about 11.5 lb. and about 15 lb. with ALICE frame.

<img src="assets/vst_backpack_sketches.jpg" height="100"> <img src="assets/vst_backpack_mounting.jpg" height="100"> <img src="assets/vst_backpack_02.jpg" height="100"> <img src="assets/vst_backpack_01.jpg" height="100"> <img src="assets/vst_backpack_00.jpg" height="100">

### User Study Procedure

Participants in our study viewed three different environments in three different hallways: Real-World through the HMDs OST display, unprocessed VST view with our camera mount, and NPR processed VST view filtered with Sobel edges. Participants were given 2 warmup distances at 4.5 and 6.5 meters in each environment, and then each trial had 4 more readings at 4, 5, 6, and 7 meters which their order of appearance was randomized. The order of views were also shuffled so no two participant had the same order and each view could appear in different hallways.

<img src="assets/vst_hallways.jpg" height="100"> <img src="assets/vst_userstudy_01.jpg" height="100"> <img src="assets/vst_userstudy_02.jpg" height="100"> <img src="assets/vst_userstudy_03.jpg" height="100">

For measuring the distance, we first found the starting position on the floor by using an aluminum bracket and a pen to mark the center between two shoe fronts on a piece of tape. Then we removed this bracket and used a tape measure to place the target at the appropriate distance according to the scheduled trial.

<img src="assets/vst_userstudy_04.jpg" height="100"> <img src="assets/vst_userstudy_05.jpg" height="100"> <img src="assets/vst_userstudy_07.jpg" height="100"> <img src="assets/vst_userstudy_08.jpg" height="100"> <img src="assets/vst_userstudy_06.jpg" height="100">

After the participants finished their walk, we put a second aluminum bracket at their feet and used our first bracket again to align the laser tape measure back against our starting position. This procedure allowed us to quickly measure and record the walked distance. For more details about this study and the results, please check out the [2017 ACM SAP paper](https://www.kvaziri.com/publications/).

### Outdoor Distance Underestimation Research with NPR VST System

<img src="assets/teaser_hires.jpg" height="150">

For second project, we conducted egocentric distance estimation in an outdoor open-field space devoid of spatial clues. This time we used HP Omen backpack computer, and modified the nVisor ST50 to power up by the backpack. Initial field tests revealed that the slow shutter web cams cannot perform in lit outdoor environment and showed a completely white image despite the exposure and gain settings, so we made custom neutral density filters of 5% and 20% with available window tint sheets and nuts and washers from the local hardware stores to reduce the light.

<img src="assets/nuts_washers.jpg" height="150"> <img src="assets/nd_filters.jpg" height="150"> <img src="assets/LAB_color_space.png" height="150">

We also added a new scene using background subtraction to remove everything but the target, in addition to the video-see-through and Sobel filter. Background subtraction was done by converting the camera frames into LAB color space, ignoring the L-channel, and using the other two channel with a threshold to mask the orange color. However, our target was a plastic cone and prone to specular reflections, so our cameras low dynamic range captured the orange color with white hues and made cavities in the target. To overcome this, we wrapped our target in a felt like fabric that had no specular reflections, and the result was perfect.

<img src="assets/cones2.jpg" height="300">

This work was published in the [IEEEVR 2021 Conference](https://www.kvaziri.com/publications/).
