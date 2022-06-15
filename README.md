# Formula Student - Path Planning Algorithm

## Abstract (EN)
Formula Student is a worldwide engineering competition held in different locations across the globe.
The goal of every participating team is to develop a race car from scratch to compete against other teams.
The race cars are either powered by a combustion engine or an electric motor which have different subcategories in the competition.
The Zurich UAS Racing team from the Zurich University of Applied Sciences built an electric-powered race car with driverless capabilities.
Sensors detect the cones on the track, which mark the track's limits, and the car's position.
A path planning algorithm needs to manoeuvre the inside of the track.
This thesis solves this problem with two different algorithms.
The first algorithm, the so-called ''Exploration Algorithm'', calculates the middle line of the track.
The Exploration Algorithm works on different tracks like the ''Acceleration'' track (a straight line) and Track Drive tracks that are unknown to the team until race day.
Further improvements can be made on the ''Skidpad'' track.
A static implementation, where the coordinates of the track are saved manually, can be used to solve the issues on that particular track.
The output of the Exploration Algorithm will be delivered to the second algorithm, the so-called ''Optimization Algorithm'', which optimizes the middle line with the information of the car's attributes to an optimal racing line.
The Optimization Algorithm works very well with the Minimum Curvature objective, but it does not perform the best compared to the Minimum Time objective.
A switch to the Minimum Time objective can further improve the estimated lap times after all required parameters can be provided.
Optimizing the track in parts during the exploration phase can further compensate for the longer computation times needed for the objective.

## Zusammenfassung (DE)
Formula Student ist ein weltweiter Ingenieur Wettbewerb, welcher an verschiedenen Orten auf der ganzen Welt ausgetragen wird.
Das Ziel jedes Teams ist es, ein Rennauto von neu auf zu entwickeln und mit diesem am Renntag gegen andere Teams anzutreten.
Dabei werden die Wettkämpfe in unterschiedliche Kategorien unterteilt, einerseits nach Antriebsart, Verbrennungs- und Elektromotor, und anderseits nach Rennen mit und ohne Fahrer.
Das Zurich UAS Racing Team der Zürcher Hochschule für angewandte Wissenschaften hat ein elektrisch angetriebenes Rennauto entwickelt.
Für die automatisierte Fahrfunktion ohne Fahrer bedarf es neben der Erkennung der Pylonen der Streckenbegrenzung und der Lokalisierung des Fahrzeugs auf der Strecke, die Plannung des zu fahrenden Pfades.
Dieser Pfad ist dabei so konzipiert, dass das Fahrzeug so sicher und schnell wie möglich durch die Strecke manövriert werden kann.
Diese wissenschaftliche Arbeit stellt zwei Algorithmen vor, welche dieses Problem lösen.
Der erste Algorithmus, der sogenannte Erkundungsalgorithmus, berechnet die Mittellinie der Strecke.
Dieser kann für die sogenannte ''Acceleration'' Strecke und für verschiedene unbekannte Strecken angewendet werden.
Eine Erweiterung des Erkundungsalgorithmus für die ''Skidpad'' Strecke müsste noch realisiert werden.
Dieses Problem kann mit einer statischen Implementation, welches die vorausgespeicherten Koordinaten der Mittellinie nutzt, gelöst werden.
Das Resultat des Erkundungsalgorithmus wird am zweiten Algorithmus, dem Optimierungsalgorithmus übergeben.
Der zweite Algorithmus optimiert die Mittellinie zu einer Ideallinie.
Dabei werden je nach Optimierungskriterium verschiedene Fahrzeugparameter berücksichtigt.
Der Optimierungsalgorithmus liefert dabei bereits gute Resultate, wenn als Kriterium die minimale Krümmung des Pfades zugrunde gelegt wird.
Eine weitere Verbesserung der Rennzeit könnte zudem erreicht werden, wenn diese Zeit als weiteres Optimierungskriterium angesetzt wird, wofür allerdings die Fahrzeugparameter genau bekannt sein müssen.
Ein Wechsel zur minimaler Zeitzielsetzung könnte die geschätzten Rundenzeiten weiter verbessern, sobald alle notwendigen Parametern bereitgestellt werden können.
Um die Berechnungszeiten zu reduzieren, könnte die Optimierung des Pfades für einzelne Teilstrecken bereits während der Erkundungsphase erfolgen.

<img src="https://github.com/Beomar97/path-planning-docs/blob/master/img/Result_Rand_final.png" alt="Exploration Algorithm on the ''Rand'' track." height="300px"/> <img src="https://github.com/Beomar97/path-planning-docs/blob/master/img/Results_Optimization_Rand_Laps_2.png" alt="Optimization Algorithm on the ''Rand'' track." height="300px"/>
