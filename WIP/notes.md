# STATO AVANZAMENTO LAVORI

L’obbiettivo è di creare un sistema che possa interagire automaticamente con diversi dispositivi IoT, usando sia Alexa sia controllando automaticamente le app di controllo di tali dispositivi.
A tal proposito ti chiederei di dare un’occhiata alle metodologie esistenti su Android per poter controllare un’applicazione (tipo monkey / monkeyrunner).
Obbiettivo iniziale: dato un dispositivo IoT (es. una lampadina controllabile a distanza) e la relativa App, scrivere del codice che controlli automaticamente la lampadina tramite App (installata su smartphone o meglio su un emulatore android).

# INCONTRO FEBRUARY 18TH, 2022

## PRESENTI: Fabio

## PUNTI SALIENTI:
1. Raccogliere informazioni su Stato dell’Arte
2. Capire come poter usare un sistema android (e.g. emulazione, device fisico, su virtualbox)
3. capire possibili metodologie per creare un sistema che interagisce in automatico con l’app di un dispositivo intelligente.

## NOTE:
Credenziali per il controllo della lampadina tramite applicazione Tapo: *CHECK CREDENTIALS*

## DOMANDE

## PUNTO 1
- [x] Collezionare i vari  paper.
- [x] Dividere i paper in cluster.
- [x] Chiedere a Fabio come proseguire.

## OBIETTIVO
Stato dell’Arte sui sistemi per automatizzare il testing di un’applicazione android. Questo ci serve per automatizzare il processo di interazione Utente + APP dispositivo IOT con il dispositivo stesso. Facendo ciò successivamente sarà possibile fare lo spoofing dell’interazione tra APP e IOT device e collezionare grossi Dataset di traffico da poter analizzare per indagini in ambito IOT Forensics.

## PAROLE CHIAVE - LINKS

### IOT FORENSICS
**A Survey on the Internet of Things (IoT) Forensics: Challenges, Approaches, and Open Issues**
\
[https://ieeexplore.ieee.org/document/8950109](https://ieeexplore.ieee.org/document/8950109)

**Forensic Analysis of digital evidence extracted from Amazon Echo**
\
[https://ieeexplore.ieee.org/document/9398391](https://ieeexplore.ieee.org/document/9398391)


**Towards Labeling On-Demand IoT Traffic**
\
[https://doi.org/10.1145/3474718.3474727](https://doi.org/10.1145/3474718.3474727)


**SIMADL: Simulated Activities of Daily Living Dataset**
\
Analysis of the Activities of Daily Living (ADLs), in a smart home environment
\
[https://doi.org/10.3390/data3020011](https://doi.org/10.3390/data3020011)

**Simulation of Smart Home Activity Datasets**
\
[https://doi.org/10.3390/s150614162](https://doi.org/10.3390/s150614162)


**User activity recognition for energy saving in smart homes**
\
[https://doi.org/10.1016/j.pmcj.2014.08.006](https://doi.org/10.1016/j.pmcj.2014.08.006)


**Multi-user activity recognition: Challenges and opportunities**
\
[https://doi.org/10.1016/j.inffus.2020.06.004](https://doi.org/10.1016/j.inffus.2020.06.004)


**Your Smart Home Can't Keep a Secret: Towards Automated Fingerprinting of IoT Traffic**
\
[https://doi.org/10.1145/3320269.3384732](https://doi.org/10.1145/3320269.3384732)

### FRAMEWORK RESEARCH CURRENT STATE OF THE ART
**On the Energy Footprint of Mobile Testing Frameworks**
\
[https://doi.org/10.1109/TSE.2019.2946163](https://doi.org/10.1109/TSE.2019.2946163)
\
Energy consumption of Testing Automation tools
\
It uses 8 popular frameworks for Android Apps automation GUI testing
* Android View Client
* Appium
* Calabash
* Espresso
* Monkeyrunner
* Python Ui Automator
* Robotium
* UIAutomator

**Understanding the Test Automation Culture of App Developers**
\
[https://ieeexplore.ieee.org/document/7102609](https://ieeexplore.ieee.org/document/7102609)
\
Understanding Test automation culture of app developers (android apps and windows apps) GUI/unit testing
* JUnit
* MonkeyRunner
* Robotium
* Robolectric

**Android Ripper**
\
Automated technique that tests Android apps via their Graphical User Interface (GUI).
\
[https://ieeexplore.ieee.org/abstract/document/6494930](https://ieeexplore.ieee.org/abstract/document/6494930)
\
[https://github.com/reverse-unina/AndroidRipper](https://github.com/reverse-unina/AndroidRipper)
\
[https://ieeexplore.ieee.org/document/6405345](https://ieeexplore.ieee.org/document/6405345)
\
[https://ieeexplore.ieee.org/abstract/document/6786194](https://ieeexplore.ieee.org/abstract/document/6786194)

**Continuous, Evolutionary and Large-Scale: A New Perspective for Automated Mobile App Testing**
\
Automation framework state of the art
\
[https://doi.org/10.1109/ICSME.2017.27](https://doi.org/10.1109/ICSME.2017.27)

*keywords: "TEST AUTOMATION" OPEN SOURCE ANDROID APPS*

**A general framework for comparing automatic testing techniques of Android mobile apps**
\
[https://doi.org/10.1016/j.jss.2016.12.017](https://doi.org/10.1016/j.jss.2016.12.017)

**The iMPAcT Tool for Android Testing**
\
[https://doi.org/10.1145/3300963](https://doi.org/10.1145/3300963)
\
This paper presents an approach and tool (iMPAcT) to automate the testing of mobile applications. It is an iterative process that combines reverse engineering and testing. It automatically explores the mobile application while trying to identify recurring behavior (pattern matching) to test. The whole process is based on a catalog of patterns that defines which type of behavior should be searched (UI Patterns) and the test strategies that can be applied in order to ensure the behavior is correctly implemented (Test Patterns).

**Automated Testing of Android Apps: A Systematic Literature Review**
\
[https://doi.org/10.1109/TR.2018.2865733](https://doi.org/10.1109/TR.2018.2865733)
\
Publicly available tools:
* AndroidRipper
* EMMA
* Monkey
* RERAN
* Robotium
* Robolectric
* Sikuli

**Mobicomonkey: context testing of Android apps**
\
[https://doi.org/10.1145/3197231.3197234](Https://doi.org/10.1145/3197231.3197234)
\
[https://github.com/LordAmit/mobile-monkey](https://github.com/LordAmit/mobile-monkey)
\
based on monkey, monkeyrunner and UI Automator

*ANDROID APPLICATIONS TESTING PLATFORM*

**Capture-Replay Testing for Android Applications**
\
[https://doi.org/10.1109/IS3C.2014.293](https://doi.org/10.1109/IS3C.2014.293)

**Automating GUI testing for Android applications**
\
It uses Monkey
\
[https://doi.org/10.1145/1982595.1982612](https://doi.org/10.1145/1982595.1982612)

**An analysis of automated tests for mobile Android applications**
\
[https://doi.org/10.1109/CLEI.2016.7833334](https://doi.org/10.1109/CLEI.2016.7833334)
* Android. Test (UNIT TESTING)
* Fest (UNIT TESTING)
* EasyMock (UNIT TESTING)
* Hamcrest (UNIT TESTING)
* JUnit (UNIT TESTING)
* Robolectric (UNIT TESTING)
* Robotium (GUI TESTING)
* Espresso (GUI TESTING)

**CrashScope: A Practical Tool for Automated Testing of Android Applications**
\
[https://doi.org/10.1109/ICSE-C.2017.16](https://doi.org/10.1109/ICSE-C.2017.16)
\
When a crash is detected, CRASHSCOPE generates an augmented crash report containing screen shots, detailed crash reproduction steps, the captured exception stack trace, and a fully replay able script that automatically reproduces the crash on a target device(s).

*keywords: ALLINTITLE: FRAMEWORK FOR AUTOMATED MOBILE TESTING*

*keywords: FRAMEWORK FOR AUTOMATED MOBILE TESTING*

**Automated Mobile Testing as a Service (AM-TaaS)**
\
[https://doi.orrg/10.1109/SERVICES.2015.20](https://doi.orrg/10.1109/SERVICES.2015.20)
* MonkeyRunner

*keywords: "MOBILE APPLICATIONS" AUTOMATED TESTING TOOLS*

**Automated Testing of Mobile Applications using Scripting Technique: A Study on Appium**
\
[https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.1049.9945&rep=rep1&type=pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.1049.9945&rep=rep1&type=pdf)
* Appium

**Novel Framework for Automation Testing of Mobile Applications using Appium**
\
[https://www.mecs-press.org/ijmecs/ijmecs-v9-n2/IJMECS-V9-N2-4.pdf](https://www.mecs-press.org/ijmecs/ijmecs-v9-n2/IJMECS-V9-N2-4.pdf)
* Appium

*keywords: MONKEYRUNNER*

**Practical GUI Testing of Android Applications Via Model Abstraction and Refinement**
\
[https://doi.org/10.1109/ICSE.2019.00042](https://doi.org/10.1109/ICSE.2019.00042)
* APE

**Stoat Prototype**
\
[https://github.com/tingsu/Stoat](https://github.com/tingsu/Stoat)

**Record and replay for Android: are we there yet in industrial cases?**
\
[https://doi.org/10.1145/3106237.3117769](https://doi.org/10.1145/3106237.3117769)
* appetizer
* Bot-bot
* Culebra
* Espresso
* MobiPlay
* monkey runner
* Mosaic
* Ranorex
* RERAN
* Robotium
* VALERA
* HiroMarco
* RepetiTouch

**Paladin: Automated Generation of Reproducible Test Cases for Android Apps**
\
[https://doi.org/10.1145/3301293.3302363](https://doi.org/10.1145/3301293.3302363)

**Espresso vs. EyeAutomate: An Experiment for the Comparison of Two Generations of Android GUI Testing**
\
[https://doi.org/10.1145/3319008.3319022](https://doi.org/10.1145/3319008.3319022)

**Practical Android Test Recording with Espresso Test Recorder**
\
[https://doi.org/10.1109/ICSE-SEIP.2019.00029](https://doi.org/10.1109/ICSE-SEIP.2019.00029)

**Sara: self-replay augmented record and replay for Android in industrial cases**
\
[https://doi.org/10.1145/3293882.3330557](https://doi.org/10.1145/3293882.3330557)

**SmartDroid: an automatic system for revealing UI-based trigger conditions in android applications**
\
[https://doi.org/10.1145/2381934.2381950](https://doi.org/10.1145/2381934.2381950)

*keyword: ESPRESSO*

**MT4A: a no-programming test automation framework for Android applications**
\
[https://doi.org/10.1145/2994291.2994300](https://doi.org/10.1145/2994291.2994300)
* Appium
* Calabash
* Robotium
* Selendroid
* Espresso
* UI Automator
* Ranorex
* Research Frameworks

**FrUITeR: a framework for evaluating UI test reuse**
\
[https://doi.org/10.1145/3368089.3409708](https://doi.org/10.1145/3368089.3409708)
\
reusing existing UI tests from an app to automatically generate new tests for other apps.

**Scripted GUI Testing of Android Apps: A Study on Diffusion, Evolution and Fragility**
\
[https://doi.org/10.1145/3127005.3127008](https://doi.org/10.1145/3127005.3127008)
* Espresso
* UI Automator
* Selendroid
* Robotium
* Robolectric
* Appium

**Sapienz: multi-objective automated testing for Android applications**
\
[https://doi.org/10.1145/2931037.2931054](https://doi.org/10.1145/2931037.2931054)

**Barista: A Technique for Recording, Encoding, and Running Platform Independent Android Tests**
\
[https://doi.org/10.1109/ICST.2017.21](https://doi.org/10.1109/ICST.2017.21)

**AppFlow: using machine learning to synthesize robust, reusable UI tests**
\
[https://doi.org/10.1145/3236024.3236055](https://doi.org/10.1145/3236024.3236055)

**FragDroid: Automated User Interface Interaction with Activity and Fragment Analysis in Android Applications**
\
[https://doi.org/10.1109/DSN.2018.00049](https://doi.org/10.1109/DSN.2018.00049)

*keywords: AUTOMATED TEST INPUT GENERATION*

*keywords: ANDROID && "AUTOMATED TEST INPUT GENERATION"*

**Automated Test Input Generation for Android: Are We There Yet? (E)**
\
[https://doi.org/10.1109/ASE.2015.89](https://doi.org/10.1109/ASE.2015.89) (monkey)
\
[https://doi.org/10.1145/2950290.2983958](https://doi.org/10.1145/2950290.2983958) (monkey)

**Automated test input generation for android: towards getting there in an industrial case**
\
[https://doi.org/10.1109/ICSE-SEIP.2017.32](https://doi.org/10.1109/ICSE-SEIP.2017.32)

**DroidBot: a lightweight UI-Guided test input generator for android**
\
[https://doi.org/10.1109/ICSE-C.2017.8](https://doi.org/10.1109/ICSE-C.2017.8)

**DroidMate: a robust and extensible test generator for Android**
\
[https://doi.org/10.1145/2897073.2897716](https://doi.org/10.1145/2897073.2897716)

**DroidMate-2: a platform for Android test generation**
\
[https://doi.org/10.1145/3238147.3240479](https://doi.org/10.1145/3238147.3240479)

**A reinforcement learning based approach to automated testing of Android applications**
\
[https://doi.org/10.1145/3278186.3278191](https://doi.org/10.1145/3278186.3278191)

**An empirical study of Android test generation tools in industrial cases**
\
[https://doi.org/10.1145/3238147.3240465](https://doi.org/10.1145/3238147.3240465)

**Seven reasons why: an in-depth study of the limitations of random test input generation for Android**
\
[https://doi.org/10.1145/3324884.3416567](https://doi.org/10.1145/3324884.3416567)

*keywords: "AUTOMATIC TEST" && "USER INTERFACE ELEMENTS" && "INTERACTION"*

*keywords: ALLINTITLE: AUTOMATIC USER INTERACTION GENERATION*

**Segen: generation of test cases for selenium and selendroid**
\
[https://doi.org/10.1145/3011141.3011154](https://doi.org/10.1145/3011141.3011154)

**RERAN: timing- and touch-sensitive record and replay for Android**
\
[https://dl.acm.org/doi/10.5555/2486788.2486799](https://dl.acm.org/doi/10.5555/2486788.2486799)

**Research on Mobile Application Automation Testing Technology Based on Appium**
\
[https://doi.org/10.1109/ICVRIS.2019.00068](https://doi.org/10.1109/ICVRIS.2019.00068)

*keywords: AUTOMATE GUI TESTING ANDROID*

**Humanoid: a deep learning-based approach to automated black-box Android app testing**
\
[https://doi.org/10.1109/ASE.2019.00104](https://doi.org/10.1109/ASE.2019.00104)

*keywords: abstract:android && abstract:gui && abstract:testing && abstract:mobile*

## DIVIDI I PAPER IN CLUSTER
- scelta phisical device vs virtualbox con su iso android x86 ??
- scelta tool di GUI Automation tra quelli selezionati foss e sviluppati dai ricercatori ??
- usare un tool scrivendo il codice oppure usare un tool di record and replay
- machine learning technique per riprodurre UI Tests
- molti paper trattano (monkey, ui automator, monkeyrunner), appium, espresso


# INCONTRO MARCH 17TH, 2022

## PRESENTI: Fabio

## PUNTI SALIENTI:
Dopo che hai guardato una serie di tool per generare automaticamente delle interazioni con le app android ti direi di mettere in pratica uno dei metodi che hai trovato e vedere quanto possa funzionare.
Se tra virtualizzato e device fisico non c'è differenza ti direi che non cambia molto per le prime fasi puoi provare come ti viene meglio. 
Il traffico che andiamo a generare lo catturiamo con dei tool simili a wireshark e poi lo analizziamo con un tool che ne estragga delle caratteristiche per un approccio orientato al Machine Learning, ma questo sarà un passo futuro.
Ti direi di effettuare qualche prova e poi ci riaggiorniamo in chiamata o in persona anche con il prof, così se ci sono decisioni da prendere le facciamo insieme. 
Riguardo la 40ina di paper non credo sia necessario che tu li legga tutti, sono decisamente tanti.
Ti direi di scremarli guardando abstract/conclusioni e rimuovendo quelli che ti sembrano poco sensati.

## OBIETTIVO

## AUTOMATED UI TEST TOOLS
Dato che svilupperemo per Android partiamo dal suo IDE, Android Studio, e vediamo cosa offre lato AUTOMATED UI TESTING

## HOW TO TEST APPS ANDROID STUDIO / CLI USER GUIDE: [https://developer.android.com/studio/test](https://developer.android.com/studio/test) ##
Description of the various tools that help you create, configure, and run your tests from Android Studio or the command line.

## TEST IN ANDROID STUDIO 
basic testing, constraint => you need the source code of the app to be tested.

## TEST FROM THE COMMAND LINE
mode fine-grained control testing, but same constraint of previous point.

## ADVANCING TEST SETUP ###
to override default settings, configure Gradle options, or refactor your code so that tests are separated in their own module.

## OTHER TESTING TOOLS ###

### Espresso Test Recorder: [https://developer.android.com/studio/test/other-testing-tools/espresso-test-recorder](https://developer.android.com/studio/test/other-testing-tools/espresso-test-recorder)
The Espresso Test Recorder tool lets you create UI tests for your app without writing any test code.
\
By recording a test scenario, you can record your interactions with a device and add assertions to verify UI elements in particular snapshots of your app.
\
Espresso Test Recorder then takes the saved recording and automatically generates a corresponding UI test that you can run to test your app.
\
Espresso Test Recorder writes tests based on the [Espresso Testing framework](https://developer.android.com/training/testing/espresso), an API in AndroidX Test.
\
The Espresso API encourages you to create concise and reliable UI tests based on user actions.
\
By stating expectations, interactions, and assertions without directly accessing the underlying app’s activities and views, this structure prevents test flakiness and optimizes test run speed.
\
constraint => you need the source code to build of the app to be testedi

### App Crawler: [https://developer.android.com/studio/test/other-testing-tools/app-crawler](https://developer.android.com/studio/test/other-testing-tools/app-crawler)
To automatically test your app without the need to write or maintain any code.
\
The crawler runs alongside your app, automatically issuing actions (tap, swipe, etc.) to explore the state-space of your app.
\
The crawl terminates automatically when there are no more unique actions to perform, the app crashes, or a timeout you designate is reached.
\
constraint => you need the source code to build of the app to be tested
\
**ESPRESSO TEST RECORDER NEEDS USER TO INTERACT WITH THE BUILT APP IN ORDER TO GENERATE THE TEST CODE.**
\
**APP CRAWLER INSPECTS AUTOMAGICALLY THE BUILT APP AND DISCOVERS VALID ACTIONS TO BE EXECUTED.**

### Monkey Testing: [https://developer.android.com/studio/test/other-testing-tools/monkey](https://developer.android.com/studio/test/other-testing-tools/monkey)
The Monkey is a program that runs on your emulator or device and generates pseudo-random streams of user events such as clicks, touches, or gestures, as well as a number of system-level events. You can use the Monkey to stress-test applications that you are developing, in a random yet repeatable manner.
\
You can launch the Monkey using a command line on your development machine or from a script. Because the Monkey runs in the emulator/device environment, you must launch it from a shell in that environment. You can do this by prefacing adb shell to each command, or by entering the shell and entering Monkey commands directly.
\
With no options specified, the Monkey will launch in a quiet (non-verbose) mode, and will send events to any (and all) packages installed on your target. Here is a more typical command line, which will launch your application and send 500 pseudo-random events to it.
\
Working on seed values it seems to create a deterministic pseudo-random events:
\
e.g. connect device to Wi-Fi (it is the first time, pair it through android studio, i guess that would be the chance to pair it through adb, but this must be investigated more in detail)
\
`adb start-server`
\
`adb shell monkey -s 1 1` -> Apre Orologio su timer
\
`adb shell monkey -s 2 1` -> Apre Office
\
`adb shell monkey -s 3 1` -> Apre MobilePASS+
\
`adb shell monkey -s 4 1` -> Apre Spazio AR
\
`adb shell monkey -s 5 1` -> Apre Gmail
\
`adb kill-server`
\
With monkey command, you can increase the probability of certain events with percent value. Use Monkey-runner for a deterministic behaviour
\
[https://stackoverflow.com/questions/31431200/example-for-using-monkey-command-with-almost-all-options-in-android](https://stackoverflow.com/questions/31431200/example-for-using-monkey-command-with-almost-all-options-in-android)

### MonkeyRunner **(deprecated)**: [https://developer.android.com/studio/test/monkeyrunner](https://developer.android.com/studio/test/monkeyrunner)
Used to perform Monkey testing with python scripts.
\
The monkey tool runs in an adb shell directly on the device or emulator and generates pseudo-random streams of user and system events.
\
In comparison, the monkeyrunner tool controls devices and emulators from a workstation by sending specific commands and events from an API.
\
The monkeyrunner tool provides these unique features for Android testing:
* Multiple device control
* Functional Testing
* Regression Testing
* Extensible automation
The monkeyrunner tool uses Jython, an implementation of Python that uses the Java programming language.
\
Jython allows the monkeyrunner API to interact easily with the Android framework.
\
With Jython you can use Python syntax to access the constants, classes, and methods of the API.
\
[https://stackoverflow.com/questions/15579328/how-to-run-monkeyrunner-on-an-already-installed-apk](https://stackoverflow.com/questions/15579328/how-to-run-monkeyrunner-on-an-already-installed-apk)
\
[https://stackoverflow.com/questions/12698814/get-launchable-activity-name-of-package-from-adb](https://stackoverflow.com/questions/12698814/get-launchable-activity-name-of-package-from-adb)
\
Monkeyrunner is being replaced by UI AUTOMATOR Tool.
\
e.g.
\
`create monkeyrunner.py`
\
`monkeyrunner monkeyrunner.py`

### UI AUTOMATOR: [https://developer.android.com/training/testing/other-components/ui-automator](https://developer.android.com/training/testing/other-components/ui-automator)
UI Automator is a UI testing framework suitable for cross-app functional UI testing across system and installed apps.
The UI Automator APIs let you interact with visible elements on a device, regardless of which Activity is in focus, so it allows you to perform operations such as opening the Settings menu or the app launcher in a test device.
Your test can look up a UI component by using convenient descriptors such as the text displayed in that component or its content description.
UI Automator and Espresso have some feature overlap but Espresso has more synchronization mechanisms so it's preferred for common UI tests.

### Espresso: [https://developer.android.com/training/testing/espresso](https://developer.android.com/training/testing/espresso)

**ANDROID STUDIO AUTOMATED TESTING SAMPLES ESPRESSO / UI AUTOMATOR**
\
[https://github.com/android/testing-samples](https://github.com/android/testing-samples)

__(BOOKMARK)__
\
**AUTOMATE UI TESTS: [https://developer.android.com/training/testing/instrumented-tests/ui-tests](https://developer.android.com/training/testing/instrumented-tests/ui-tests)**
\
__(BOOKMARK)__

### COMPOSE: [https://developer.android.com/jetpack/compose/testing](https://developer.android.com/jetpack/compose/testing)

### APPIUM: [https://appium.io/](https://appium.io/)

### CALABASH: [https://github.com/calabash/calabash-android](https://github.com/calabash/calabash-android)
To use monkey use the bash tool adb shell monkey/adb devices.

To use the other devices create a java/kotlin test snippet in android studio and execute it in the device connected through usb cable/Wi-Fi pairing. 

## VIRTUAL / PHYSICAL

Creiamo VM con Android come OS INSTALLATION ANDROID 9.0 X86\_64: [https://i12bretro.github.io/tutorials/0258.html](https://i12bretro.github.io/tutorials/0258.html)

### ANDROID EMULATOR/DEVICE
[https://developer.android.com/studio/run/emulator](https://developer.android.com/studio/run/emulator) 
[https://developer.android.com/studio/run/device](https://developer.android.com/studio/run/device)

__USIAMO PHYSICAL DEVICE COLLEGATO AD ANDROID STUDIO__

[https://stackoverflow.com/questions/7022527/how-to-click-a-view-of-android-program-through-monkeyrunner](https://stackoverflow.com/questions/7022527/how-to-click-a-view-of-android-program-through-monkeyrunner) 

## Ridurre numero di paper

# INCONTRO APRIL 12TH, 2022

## PRESENTI: Fabio, Alessandro

## PUNTI SALIENTI:
1. 1 test con + app gestire o + test da orchestratore ognuno per 1 app o disp gestito
2. Orchestrare i test con scheduling temporale e esecuzione sequenziale per test deterministico per riprodurre comportamento umano o test random.
3. Provare a usare e creare un emulatore android anche di android studio o macchina virtuale
4. Mappare tutte le possibili interazioni che si possono avere con l'oggetto vanno mappate (e.g. x la lampadina Smart Bulb di Tapo, on/off, cambio colore e cambio luminosità.
5. Scrivere un log file con aioni automatiche che il test sta facendo x avere una GROUD TRUTH in sfruttare in seconda analisi x la parte di classificazione (e.g. TIMESTAMP APP TIPO\_ATTIVITA'
