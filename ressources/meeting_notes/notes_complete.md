# Meeting Notes 06.06.2022

## Attendance ✅ ❌:

| Name   | abbr     | attendance |
| ------ | -------- | ---------- |
| Marco  | forstma1 | ✅          |
| Dan    | hochsdan | ✅          |
| Luis   | miranlui | ❌          |
| Monika | reif     | ✅          |
| Stefan | brrt     | ❌          |

## Notes

**General / Todos:**

- Finished Chapters 4 Results and Chapter 5 Discussion and Conclusion
- Finished Abstract/Zusammenfassung and Preface
- Several improvements on references, table of contents and more
- Discussed further improvements possible for thesis before hand-in
- Describe the structure of the code base in the appendix and reference it in the thesis
  - Mention that access is only available for team members of ZUR
  - Add the link to the repository.
- Look that image sizes are unified.
- Track Plotter figure is missing a reference ->. Generally, all images have references.
- Descriptions at the start of the chapters need to be improved.
  - Don't start with "This chapter..."
- Maybe move the GGV table to the appendix and reference it.
- In Results, describe the Skidpad image more -> generally describe images in the results chapter more in detail.
- Overview images in the results chapter can be moved to the appendix if too many pictures are in it.
- If helpful, important text can be bold, or subheadings can be created.
- German Zusammenfassung needs improvement.

# Meeting Notes 30.05.2022

## Attendance ✅ ❌:

| Name   | abbr     | attendance |
| ------ | -------- | ---------- |
| Marco  | forstma1 | ✅          |
| Dan    | hochsdan | ✅          |
| Luis   | miranlui | ❌          |
| Monika | reif     | ✅          |
| Stefan | brrt     | ❌          |

## Notes

**General / Todos:**

- Talking about tips and feedback for thesis and what to write about next
- Finished Chapter 3, now on to Chapter 4 Results
- Would be great to have a draft of chapter 4 Results and possibly Chapter 5 Discussion on Friday or Saturday

# Meeting Notes 19.05.2022

## Attendance ✅ ❌:

| Name   | abbr     | attendance |
| ------ | -------- | ---------- |
| Marco  | forstma1 | ✅          |
| Dan    | hochsdan | ✅          |
| Luis   | miranlui | ✅          |
| Monika | reif     | ✅          |
| Stefan | brrt     | ❌          |

## Notes

**What we have done:**

- Only small changes in Code, added some parameters to the Optimization Algorithm
- Created additional figures for Approach and Methods Chapter (Architecture, Optimization Package, V-Model, ...)
- Written sections about Scrum and V-Model, started with Optimization Algorithm and Architecture

**What we want to accomplish by next week:**

- Mostly finish Approach / Methods Chapter
- Test algorithms with Simulation Tool (with Luis tomorrow)

**Problems:**

- None

**General / Todos:**

- Will try to test the Path Planner Package with the Simulation Tool tomorrow
- Adjust V-Model figure, so it looks more like a V
- Figures on how the different objectives (algorithms) in Optimization work
- Project and Weekly Plan can be added to the appendix
- Concept of Operations (V-Model) given by Team (ZUR) and Formula Student Rulebook
- Add Verification and Integration Sections into Approach / Methods Chapter
- In Results Chapter
  - Difference between Optimization objectives (time-wise and more)

  - Describe Test Setup
- What has already been tested? What still needs to be verified? To think about next...

# Meeting Notes 13.05.2022

## Attendance ✅ ❌:

| Name   | abbr     | attendance |
| ------ | -------- | ---------- |
| Marco  | forstma1 | ✅          |
| Dan    | hochsdan | ✅          |
| Luis   | miranlui | ✅          |
| Monika | reif     | ✅          |
| Stefan | brrt     | ❌          |

## Notes

**What we have done:**

- Started describing exploration algo in chapter 3
- Added scrum description
- Added chapter Hardware Abstraction à to explain how we developed the algos
- Applied corrections
- Added Section 'Work Overview' in Chapter 1 + updated Objective description
- Moved Optimization Algorithm to separate ROS Service => Path Planner can now still calculate the path via Exploration algorithm while the optimized path is being calculated
- Add additional test tracks (+ skidpad track) to cone publisher

**What we want to accomplish by next week:**

- Finish Algo exploration description
- Create further illustrations for explanation

**Problems:**

- None

**General / Todos:**

- Implement Path Planning Package into Simulation Tool with Luis

- Proposal Structure for Chapter 3 Approach / Methods

  - Anfangs High Level Overview Mischung technisch und organisatorisch, Kapitel ersichtlich was kommt, Flussdiagram (um dieses haben wir dann die Prozessmethoden)

  - Vorgehensmethode => Kanban und Scrum, maybe V-Model?

  - Setup technisch, lokale Linux VM, ROS Installation, VS Code als IDE, GitHub Repos, GitHub Actions CI/CD (maybe?), Deployment Architektur

  - Overview Architektur ROS und Code, Grundüberlegung => Path Planning Package in ROS, Prototyp Architektur zeigen, Explo und Opt Algos, erhaltet Input und sendet Input

    - Messages (interfaces und fszhaw msgs) (System aussen)
    - Path Planner Node
      - Exploration Algorithm

    - Optimization Service Node
      - Optimization Algorithm

  - Verifikation und Validierungen (Code Reviews, Fehlerfälle: Cones gehen verloren, Cones andere Seite entdeckt, allg Fehlerannahmen)
    - Testing mit Maps, Cone Publisher und Planned Trajectory Subscriber (mocks), utils wie track plotter, trackconfig

- Setup eher im Projektanhang: Weekly meetings, Review every other week, Mitarbeit mit anderen BA Teams in Driverless und gesamt Verein (Working Saturday, Hilfe im Workshop, Ausstellung Conecto ZHAW)
- In Resultate Kapitel, Vergleich erste Algorithmen und Versuche
  - erste Überlegungen und Tests, alter path planner zhaw, dann densify und interpolate, rrt max hamburg, komplexer algo à la ultimate und dann jetzige implementation
  - Zuerst was hat eth mit mpcc, dann global racetrajectory von tumftm

# Meeting Notes 05.05.2022

## Attendance ✅ ❌:

| Name   | abbr     | attendance |
| ------ | -------- | ---------- |
| Marco  | forstma1 | ✅          |
| Dan    | hochsdan | ✅          |
| Luis   | miranlui | ✅          |
| Monika | reif     | ✅          |
| Stefan | brrt     | ❌          |

## Notes

**What** **we have done:**

- Extended Cone Publisher with Sim Tool compatibility, receives all track cones from tool and publishes these
- A lot of Code Refactoring, added Docstrings, Typings and many more improvements
- "Cache" for Exploration algorithm, takes only e.g. last 50 cones for distance measurements
- Working on "Switch" implementation, when to switch algorithms
- Optimization Algorithm with input from Exploration works now
- Added Path Smoothening for midpoints in Exploration Algorithm (Cubic Spline Interpolation)
- Extended Chapter 1 State of the Art Section with more examples
- Finished Algorithms Section in Chapter 2 (references and images)
- Started with Results

**What we want to accomplish by next week:**

- Write on Results
- Read other persons writings
- Refinement of Algorithms
- Compatibility with Simulation Tool
- Do "Work Overview" section in Chapter 1

**Problems:**

- None

**General / Todos:**

- Maybe use the Starting Position to know when to switch the algorithms, know when a lap is finished (Possible for Trackdrive)

- Getting Sim Tool working with Algorithms => Trying together probably better

  - Ask Gui how hard a local installation might be (Performance reasons on server)

- For testing, note down configs, make screenshots and more

- Feedback on Thesis (Detailed in PDF):

  - Sachlicher formulieren

  - Objektiver schreiben, mehr Bezug zur Arbeit und weniger zu Person

  - Nie Bild direkt unter Überschrift

  - Bild referenzieren im Text

# Meeting Notes 29.04.2022

## Attendance ✅ ❌:

| Name   | abbr     | attendance |
| ------ | -------- | ---------- |
| Marco  | forstma1 | ✅          |
| Dan    | hochsdan | ✅          |
| Luis   | miranlui | ✅          |
| Monika | reif     | ✅          |
| Stefan | brrt     | ❌          |

## Notes

**What** **we have done:**

- Chapter 2 Section Algorithms finished (and added pictures)
- Done with "Exploration" algorithm implementation, a lot of refactoring and making it more clearer to understand
- Created figures for "Exploration" algorithm (Pseudocode and Flow-diagram)
- Finished PlannedTrajectory Publisher for the autopilot
- Tested "Exploration" algorithm with another, longer track => looks good!

**What we want to accomplish by next week:**

- Do "Work Overview" section in Chapter 1
- Combine Exploration with Optimization -> does it work together?
- Generally more Thesis writing this week
- Path smoothening
- Start writing about realization

**Problems:**

- None

**General / Todos:**

- Think about how to test the algorithms after they are finished

  ->maybe use manual points and calculate delta? whats the difference with real midpoints

# Meeting Notes 21.04.2022

## Attendance ✅ ❌:

| Name   | abbr     | attendance |
| ------ | -------- | ---------- |
| Marco  | forstma1 | ✅          |
| Dan    | hochsdan | ✅          |
| Luis   | miranlui | ✅          |
| Monika | reif     | ✅          |
| Stefan | brrt     | ❌          |

## Notes

**What** **we have done:**

- Testing/experimenting with Triangulation for the Exploration algorithm (see 'marcos-testing-reloaded'-branch)
- Started with the 'Output'-Publisher
- Finished section 'ZUR Autonomous System' in Chapter 2 Background
- Extended algorithm section in Chapter 2

**What we want to accomplish by next week:**

- Finish Implementation of the Exploration algorithm, or at least get a working prototype
- Add sections 'Work Overview' and add 'TUMFTM and U of Edinburgh' implementations to section 'FS Implementations' in Chapter 1 Introduction
- Improve BA thesis with feedback from Monika

**Problems:**

- None

**Todos:**

- After algorithm is finished, try to apply it to other tracks

  => Can use tracks from the Simulation Tool

- Consider the angle in front of the car if it could be a problem 

- BA Thesis Feedback

  - Introduction looks quite good
    - Add some more implementations from other schools (e.g. Edinburgh and Munich)
  - Background also pretty good
    - Explain/Show different tracks (e.g. Skid Pad, etc.) at the beginning of Chapter 2 Background
    - Maybe explain basic setup of ROS project (e.g. ETHZ skeleton?)
    - Pictures or figures for these algorithms
  - Methods
    - Later more into detail with triangulation and more

# Meeting Notes 12.04.2022

## Attendance ✅ ❌:

| Name   | abbr     | attendance |
| ------ | -------- | ---------- |
| Marco  | forstma1 | ✅          |
| Dan    | hochsdan | ✅          |
| Luis   | miranlui | ✅          |
| Monika | reif     | ✅          |
| Stefan | brrt     | ❌          |

## Notes

**What** **we have done:**

- Optimized the triangulation algorithm with thresholds
- Integrate global trajectory into ROS project

- Created input transformer for global trajectory
- First test implementation for exploration with Delaunay
- Worked on Chapter 2 (FS Events and a bit about FSZHAW autonomous system)

**What we want to accomplish by next week:**

- Work on chapter 2
- Optimize Triangulation

**Problems:**

- Finding a way to get the middle point with curve detection

**Todos:**

- What happens when cones are missing? Will the algorithm still work?

- Maybe add virtual cones => As we know the width of the track

  After interpolation of the track, create additional points in between the "real" midpoints

- Send draft to Monika whenever we have something => Probably first version after easter weekend

- Wait with description of algorithms after they are prettty much finished and robust

- what happens if we see cones from the other side

- After track is known, even before the car is there => connect track to beginning (see screenshots)

# Meeting Notes 07.04.2022

## Attendance ✅ ❌:

| Name   | abbr     | attendance |
| ------ | -------- | ---------- |
| Marco  | forstma1 | ✅          |
| Dan    | hochsdan | ✅          |
| Luis   | miranlui | ✅          |
| Monika | reif     | ✅          |
| Stefan | brrt     | ❌          |

## Notes

**What** **we have done:**

- Chapter 2 Algorithms (wrote about RRT and Triangulation)
- Chapter 2 Formula Student (from Monika’s Input)
- Optimized the triangulation algorithm with less cones
- Created an “Input Transformer” in ROS (prepares cones and reference line for global racetrajectory)

**What we want to accomplish by next week:**

- Integrate global trajectory into ROS project
- Work on chapter 2

**Problems:**

- Finding a way to get the middle point with less cones on one side (not perfect yet à Demo)

# Meeting Notes 31.03.2022

## Attendance ✅ ❌:

| Name   | abbr     | attendance |
| ------ | -------- | ---------- |
| Marco  | forstma1 | ✅          |
| Dan    | hochsdan | ✅          |
| Luis   | miranlui | ✅          |
| Monika | reif     | ✅          |
| Stefan | brrt     | ❌          |

## Notes

**What we have done:**

- Gobal trajectory optimization input testing, how it works, settings, etc.:
  https://github.com/TUMFTM/global_racetrajectory_optimization
- Started with chapter 2
- Revision of chapter 1
- Tried to get middle point of cones with different color (demo)

**What we want to accomplish by next week:**

- Calculate distance from middle point to border
- Integrate global trajectory into ROS project
- Work on chapter 2
- Optimize triangulation with less cones

**Problems:**

- If there are not a lot of cones in curve, it will “break” the algorithm

**Todos:**

- Change chapter title from "Theoretical Principles" to "Background"

- Better to move some information about Formula Student from chapter 1 to chapter 2

  => Explain different tracks and challenges as well

- Create a figure about the methods

  Problem => two different sides 1. Exploration (Triangulation, RRT) 2. Optimization

  Figure should give a overview of whole project, show how everything works

  => Put it at the beginning of the methods chapter

- Also create overview / figures for the algorithms => how they work

- Think about how to compare different algorithms

  => How to test and verify the algorithms? Look at precision and timing?

- Notes for Marco:

  - Update diagram with output + inner working of algorithm
  - Implement: Input transformation for algorithm (+ maybe also needed for output)
  - Maybe able to start optimizing in parts? Don't need to wait for whole track

# Meeting Notes 24.03.2022

## Attendance ✅ ❌:

| Name   | abbr     | attendance |
| ------ | -------- | ---------- |
| Marco  | forstma1 | ✅          |
| Dan    | hochsdan | ✅          |
| Luis   | miranlui | ✅          |
| Monika | reif     | ✅          |
| Stefan | brrt     | ❌          |

## Notes





# Meeting Notes 17.03.2022

## Attendance ✅ ❌:

| Name   | abbr     | attendance |
| ------ | -------- | ---------- |
| Marco  | forstma1 | ✅          |
| Dan    | hochsdan | ✅          |
| Luis   | miranlui | ✅          |
| Monika | reif     | ✅          |
| Stefan | brrt     | ❌          |

## Notes

**What we have done:**

- Chapter 1 "finished", will be extended if more sources are found
- Research of algorithms and literature
- Found test tracks and created a plotter for those tracks
- First test implementation in ROS (simple cone publisher and planner subscriber)
- First Input / Output Model «drawn»

**What we want to accomplish by next week:**

- Implement and test algorithms implementieren (RRT / MPCC)
- Start with chapter 2

**Problems:**

- Difficult to find ideal algorithms (how to approach)
- Combining different algorithms (some teams have used Triangulation with RRT => how to approach?)

# Meeting Notes 10.03.2022

## Attendance ✅ ❌:

| Name   | abbr     | attendance |
| ------ | -------- | ---------- |
| Marco  | forstma1 | ✅          |
| Dan    | hochsdan | ✅          |
| Luis   | miranlui | ✅          |
| Monika | reif     | ✅          |
| Stefan | brrt     | ❌          |

## Notes

- Question: What should we include in the thesis?
  - In chapter 1 Initial Situation write about what other schools have used, e.g. ETH used algorithms a and b, Edinburgh used algorithms c and d, and FSZHAW last year used bla bla
  - In chapter 2 theory write about the algorithms used by the schools briefly and the algorithms we use
  - In chapter 3 methods talk about the algorithms we are using and how we implemented them

- Algorithms
  - Pick which already have been used in other teams
  - Think about miscalculated cones (error rate?)

- Have an illustration ready for next monday about inputs/outputs

# Meeting Notes 03.03.2022

## Attendance ✅ ❌:

| Name   | abbr     | attendance |
| ------ | -------- | ---------- |
| Marco  | forstma1 | ✅          |
| Dan    | hochsdan | ✅          |
| Luis   | miranlui | ✅          |
| Monika | reif     | ❌          |
| Stefan | brrt     | ❌          |

## Notes

- Both Marco and Dan have completed the official ROS 2 tutorials

- Both have done some research into existing path planning algorithms and other works

  - Basic graph search algorithms
    - Dijkstra
    - A*

  - Rapidly-exploring Random Trees (RRT)
  - Model Predictive Path Integral (MPPI)

- Some interesting papers have been uploaded to the FSZHAW SharePoint

  https://zhaw.sharepoint.com/sites/FSZHAW2020-2021

- Next big step is to define the interfaces for both the inputs and outputs

  - Output will very likely be the next coordinate for the car to go to (probably the easiest and most preferable solution)
    - Still some restrictions apply
      - Distance of the car to the next point (e.g. 2m in front of the car) <- most likely be a config parameter

  - Input will probably be a list of the coordinates of the detected cones and the current position of the car (will be most tricky part)

- Need to think about what to implement and how to organize the nodes internally in ROS

- Resource Mgmt also important, computation needs to be quick of the path

- If we already want to implement something in ROS -> Draw a middle line of the path

## TODOs

- Think about the Input and Output
- Think about the architecture and how we want to organize the nodes internally
- First implementation in ROS possible -> draw a middle line

# Meeting Notes 24.02.2022

## Attendance ✅ ❌:

| Name   | abbr     | attendance |
| ------ | -------- | ---------- |
| Marco  | forstma1 | ✅          |
| Dan    | hochsdan | ✅          |
| Luis   | miranlui | ✅          |
| Monika | reif     | ❌          |
| Stefan | brrt     | ❌          |

## Notes

- Merging both meetings into one would be good

- Deadlines

  - Car assembly deadline doesn't matter for us

  - 08.07.2022 is deadline for the video of the car driving itself

    => everything should be done at least 1 week before

  - Implementation should be done at around semester end, so we have enough time for testing

- Simulation Tool Ba will probably be based on [fs-driverless.github.io](http://fs-driverless.github.io)

- Input

  - Need to figure out what input we need
  - Other teams can adapt on our needs
  - Should have it in 1-2 weeks

- Luis will discuss with Monika about the MS channel

  => easiest would be to invite her to the existing channel in FSZHAW

- Input/Output interfaces will be very important

  - e.g. output could be a list of points (for the car to drive to)

## TODOs

- Figure out what we need as Input (in 1-2 weeks)
- Invite Monika to the Teams Channel (Luis)
- Think about Input/Output
- Send invitations for newly merged meeting

# Meeting Notes 22.02.2022

## Attendance ✅ ❌:

| Name   | abbr     | attendance |
| ------ | -------- | ---------- |
| Marco  | forstma1 | ✅          |
| Dan    | hochsdan | ✅          |
| Luis   | miranlui | ❌          |
| Monika | reif     | ✅          |
| Stefan | brrt     | ✅          |

## Notes

- Struktur BA
  - Einleitung
    - Was wollen wir machen?
    - Was gibt es bereits? Was ist der Stand der Technik?
    - Wie ist die Ausgangslage?
    - Infos zum Vorgänger (Was hat das letzte Team gemacht?)
    - Infos zu Formula Student
    - Was machen ETHZ oder andere in der Industrie
  - Theoretishe Grundlagen
    - Während dem einlesen => gleich gelerntes in die Dokumentation notieren
    - Grobbeschrieb ROS 2
  - Vorgehen
    - Wie sind wir hier vorgegangen?
    - Beschreibung der verschiedenen Methoden für Path Planning
    - Auch Gesamtmethodik
    - V-Modell => Schritte in V-Modell eventuell eigene Methodik
    - Iterativ, Scrum
    - DevOps, CI/CD
  - Resultate
    - Was wurde gemacht, wie schauts aus
  - Diskussion
    - Was klappte, was nicht
  - Können uns an vorhandene BAs von Formula Student orientieren
- Sonstiges
  - Falls Drittsoftware auf GPU zugreifen möchte, muss der Safe Mode im Jetson deaktiviert werden
  - Struktur für zukünftige Meetings zum beschleunigen
    - Was wurde gemacht => Was als nächstes geplant => Wo gibt es Schwierigkeiten
  - Ist eine Gruppe in MS Teams für die Kommunikation nötig?
- Offene Fragen
  - Genaue Deadlines noch offen
    - Wann muss Algorithmus/Implementation stehen? Auch wichtig bezüglich Testphase
    - Vorabversion ab wann? Finale Version ab wann?
  - Wie sieht der Input aus für unseren Algorithmus? (Aus Perception, evtl Liste mit x/y Positionen der detektierten Objekten als Float Werten) => Pub/Sub
    - Was für Testdaten brauchen wir?
    - Als Requirement für Perception Team, das wir Testdaten haben
  - Einzelne Meetings mit Luis und Reif oder gemeinsam (Auch möglich das sie sich 10/15min später einwählen)
    - Möglicher Termin finden

## TODOs

- Termin finden für Weekly Meeting mit Luis (miranlui), Reif (reif) und Stefan (brrt)
- Gruppe in MS Teams erstellen mit alle Stakeholders (Marco, Dan, Luis, Reif, Stefan)
- Offene Fragen mit Luis beantworten
- ROS 2 Umgebung einrichten + Tutorials durchmachen
- Bereits schauen ob ROS 2 bereits Bibliotheken zum Thema hat
- Einlesen ins Thema Path Planning und schauen wie andere dies gemacht haben (Vorgänger, AMZ, etc.)