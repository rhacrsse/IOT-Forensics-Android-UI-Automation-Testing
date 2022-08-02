# WALKTHROUGH
This guide describes a step by step procedure in order to add a new device to do Testing phase
The first approach will be using directly the source code, changing something depending on the needs of the app to test.
It must be collected some information in order to understand how to configure the test.
A list of steps could be the following:
1. (only if this a new project) Download Android Studio
2. Create a VDA compatible with Google Store and x64 processor, otherwise we cannot download the app needed from the app store.
3. Launch the VDA qemu device, configure Google App Store and download the app needed in the front page
4. Create a new project empty
5. Inspect the new application to test through the tool *uiautomatorviewer*
6. Collect the main actions the must be replicated, and possible resourceid and pixels positions 
7. Create the class in order to perform the test and modify the default instrumented class such that we can perform the test.
8. Our goal is to create a test able to run for days without stopping in order to collect a sufficient amount of data through the router Wi-Fi sniffer device located in the AntLab laboratory.
