---
title: Prototyping I
date: "2021-10-22"
description: "A brief overview, documentation and reflection of the prototyping and testing on voice assistants done in the last semester. The most important take-away: This needs to be a group effort."
header: "/assets/images/thumbs/Screenshot_2021-10-24_at_11.11.50.png"
tags:
    - methodologies
    - review
---
# Prototyping I
Ausgehend von der [[Thematic Analysis]] vor dem zweiten Colloquium wollte ich im letzten Semester erste Entwicklungen mit den eigenen Ansätzen bezüglich Sprachassistenten umsetzen. Dazu galt es einerseits eine Entwicklungsumgebung (Tech Stack) aufzubauen, welche Rapid Prototyping erlaubt und andererseits zu definieren, wie diese ersten Prototypen genau zu funktionieren haben und wie sie testbar werden. Parallele Entwicklungen [[Vorbereitung und Zusammenfassung Gedanken für C3|bezüglich der Erkundung der sozialen/Relevanz]] haben den Prototypen dann noch einen zusätzlichen Dreh gegeben.

## Prototypes
Folge Prototypen konnten umgesetzt werden.

### Timers
*artyom.js*
Timer stellen ist gefühlt das meistgebrauchte Feature in Bezug auf Sprachassistenten. Ein guter Test um sich das jeweilige Framework einzuarbeiten…

### Proximity Sensor und Flip Switches with micro:bit
*Mycroft, Raspberry Pi und micro:bit*
Diese beiden Tests kam aus dem Gedanken heraus, dass Peripherie-Geräte der Interaktion mit Sprachassistenten im Bezug auf der Verhandlung von Privatsphäre zudienlich sein können.

Die Tests waren durchaus spannend, wenn auch sehr technisch. Ich konnte vor allem Proof of Concepts umsetzen diese aber nicht eingehend testen. Beim Proximity Sensor ging es darum, dass ich mit Hilfe eines Beacon Objektes dem Sprachassistenten mitteile, ob ich mich in der Nähe befinde oder nicht. Dieser reagiert dann dementsprechend darauf wenn ich mich nähere und ist ansonsten nicht aktiv.

Beim Flip Switch lässt sich mit einer kurzen Handbewegung, dem Umkehren eines Beacon Objektes, der Zustand des Sprachassistenten verändern. Der Zustand wird dann wiederum im Beacon Objekt wiedergegeben.

![Code](/assets/images/thumbs/IMG_0439.jpeg)

### ELIZA; on mycroft and artyom
*Mycroft, Raspberry Pi, artyom.js*
ELIZA war ein von Joseph Weizenbaum entworfenes Chatprogram, welches entlang der Linie einer klassischen Sprech-Therapiesitzung gestaltet wurde. Eigentlich wollte Weizenbaum vorführen, wie einfach der Mensch zu täuschen ist. Jedoch war sein Program sehr beliebt. ELIZA beruht auf wenigen Regeln, wie ein etwas vom Mensch geschriebenes zu interpretieren ist und reagiert darauf in der Regel mit Fragen. Ich habe ELIZA in zwei verschiedenen Sprachassistenz-Frameworks umgesetzt um damit die Dialogizität zu testen.

### Memory Holders
*artyom.js*
Ausgehend aus einem nicht verfolgtem Thema der thematischen Analyse, [[Knowledge Practices]], wollte ich einen Sprachassistenten testen, welcher sich Praxen rund um Wissen oder zumindest Notizen fokusiert. In diesem Test lässt sich in einem Dialog mit dem Sprachassistenten treten und er speichert forlaufend alles gesagte und spiegelt es wieder.

![Code](/assets/images/thumbs/Screenshot_2021-10-24_at_11.11.50.png)

## Reflexion
Das letzte Semester war überraschend kurz, was ich so nicht antizipiert hatte. Dementsprechend war auch die Planung den Umständen nicht entsprechend. Ich hätte gerne mehr Zeit fürs Testing aufwenden können.

Eines der wichtigsten Take-Aways ist wohl wie weit die technischen Möglichkeiten und auch Zugänglichkeit geschritten ist. Das ist vor allem für ein Prototyping innerhalb des Fokuses von Sprachassistenten sehr hilfreich und praktisch. Beim viel wichtigeren Teil des Testings habe ich festgestellt, dass ich umbedingt eine stabile Gruppe von Test-Personen brauche, innerhalb dessen ein Vergleich der einzelnen Tests möglich ist. Ansonsten gehe ich Gefahr in die *I-Methodology* zu fallen; Der Entwicklung und Testing aus meiner eigenen Sicht, zu meinen eigenen Bedürfnissen. Der Aufbaue einer solchen Test-Gruppe ist allerdings mit sehr viel Resourcen und Zeit verbunden.

Ein sehr spannender Aspekt, welcher durch das Prototyping dazu gekommen ist, ist das [Konversation Design](https://neohelden.com/de/blog/conversational-interfaces/conversational-design-prinzipien/). Es geht also darum, nicht einer einfachen Befehl-Befolgung Struktur zu folgen, sondern jene Personen, welche mit den Sprachassistenten sprechen auch auf der Ebene des Konversation abzuholen. Dies ist ein Bereich welcher im Moment noch sehr schwer abzudecken ist. Es ist aber auch jener Bereich in welchem ich die Aushandlung von Privatsphäre platzieren würde. 

## Tech Stack
- Mycroft [https://mycroft.ai/](https://mycroft.ai/)
- AIY Voicekit [https://aiyprojects.withgoogle.com/voice/](https://aiyprojects.withgoogle.com/voice/)
- Artyom.js [https://sdkcarlos.github.io/sites/artyom.html](https://sdkcarlos.github.io/sites/artyom.html)
- Rasperry Pi 4 [https://www.raspberrypi.com/products/raspberry-pi-4-model-b/](https://www.raspberrypi.com/products/raspberry-pi-4-model-b/)
- BBC micro:bit [https://microbit.org/](https://microbit.org/) - Kleines Mikroprozessor-Entwicklungsboard welches mit verschiedenen Sensoren, zB 

## Repositories
Mein erarbeiteter Code ist in folgenden Repositories zu finden.
- [https://github.com/thgie/tele-bits](https://github.com/thgie/tele-bits)
- [https://github.com/thgie/eliza-skill](https://github.com/thgie/eliza-skill)
- [https://github.com/thgie/The-Relevance-of-Speaking-with-Things](https://github.com/thgie/The-Relevance-of-Speaking-with-Things)