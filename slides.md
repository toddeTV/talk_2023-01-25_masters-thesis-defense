---
theme: ./theme
layout: default
themeConfig:
  primary: '#3b82f6'
  showTotalPageCount: false
  showPageProcessBar: true
title: Talk 2023-01-25 - master's thesis defense
author:
  name: Thorsten Seyschab
  website: todde.tv
titleTemplate: '%s'
background: false
# class: bg-gray-500
download: false
exportFilename: talk_2023-01-25_masters-thesis-defense
highlighter: shiki
lineNumbers: false
monaco: false
remoteAssets: true
selectable: false
record: true
info: |
  # Talk 2023-01-25 - master's thesis defense
  
  This project contains the slides for my the talk on 2023-01-20 at the university
  [Technische Universität Dresden](https://tu-dresden.de/) about [FMADB](https://fmadb.org/),
  which was my master's thesis defense.  
  The slides are partially based on my talk
  [Talk 2022-10-28 - Musiktheorie Symposium](https://github.com/toddeTV/talk_2022-10-28_musiktheorie-symposium).
  
  The presented language is `German`, the repository and documentation language of FMADB is `English`.
colorSchema: light
routerMode: history
aspectRatio: 16/9
canvasWidth: 1024
favicon: /assets/fmadb_logo/v8/logo-light/logo-light_icon_h-64px.png
plantUmlServer: https://www.plantuml.com/plantuml
fonts:
  sans: Roboto
  serif: Roboto Slab
  mono: Fira Code
drawings:
  enabled: true
  persist: true
  presenterOnly: false
  syncAll: false
---

<AppIntroLogoFullscreen />

<!--
* Begrüßung zu meiner Verteidigung, welche ein 30 min Vortrag mit anschließenden 30 min Fragen ist.
* Fragen bitte notieren und am Ende stellen.
* Gäste, die nicht vom Fach sind, sind heute hier -> daher 
* Ich stelle hier eine Übersicht meiner Arbeit und der Ergebnisse dieser vor. Tiefergehende Informationen gerne bei
  Bedarf am Ende erfragen. Zeit aber einfach zu knapp, die rund 120 Seiten meiner Arbeit in 30 Minuten vorzustellen.
-->

---
layout: two-cols
---

<h1>Über mich</h1>

<div class="flex flex-col justify-center items-center mt-14">
  <img class="w-50 rounded-full"
      src="/assets/persons/Thorsten-Seyschab.jpg"
  />
  <h2 class="mt-4">Thorsten Seyschab</h2>
</div>

::right::

<VClicks class="space-y-2 text-xl h-full mt-22">

* <mdi-desktop-classic class="baseColor mr-2" /> Informatiker aus Deutschland<br>
  <span class="text-sm ml-10">Spezialisiert in Web Technologien & Datenbanken</span>
* <mdi-console class="baseColor mr-2" /> Full Stack Web Developer
* <mdi-school-outline class="baseColor mr-2" /> Technische Universität Dresden
* <mdi-email class="baseColor mr-2" /> [business@todde.tv](business@todde.tv)
* <mdi-web class="baseColor mr-2" /> [https://todde.tv/](https://todde.tv/)
  * <mdi-github class="baseColor mr-2" /> [toddeTV](https://github.com/toddeTV)
  * <mdi-gitlab class="baseColor mr-2" /> [toddeTV](https://gitlab.com/toddeTV)

</VClicks>

---
layout: two-cols
---

<h1><span class="line-through mr-6">Über mich</span>FMADB Team</h1>

<div class="flex flex-col justify-center items-center mt-14">
  <img class="w-50 rounded-full"
       src="/assets/persons/Thorsten-Seyschab.jpg"
  />
  <h2 class="mt-4">Thorsten Seyschab</h2>
</div>

<div class="absolute w-full flex flex-row justify-center left-0 px-40 pt-10">
  <div>
    <img class="h-15 p-2"
         src="/assets/attribution_logos/TU-Dresden.svg"
    />
  </div>
  <div>
    <img class="h-15 p-2 mx-10"
         src="/assets/attribution_logos/HfmDD.png"
    />
  </div>
  <div>
    <img class="h-15 p-2"
         src="/assets/attribution_logos/epfl.svg"
    />
  </div>
</div>

::right::

<h1 class="opacity-0">.</h1>

<div class="flex flex-col justify-center items-center mt-14">
  <img class="w-50 rounded-full"
      src="/assets/persons/Susanne-Hardt.jpg"
  />
  <h2 class="mt-4">Susanne Hardt</h2>
</div>

<!--
* Hfm vertreten durch Susanne
* TU-Dresden vertreten durch mich
* Epfl in der Schweiz als Expertenfeedback
* und und und
* Doch um zu verstehen, was FMADB ist und warum es einzigartig ist, müssen wir erst das übergeordnete Vorhaben verstehen.
-->

---

# Motivation

<VClicks class="space-y-2 text-xl">

* <mdi-crosshairs class="baseColor mr-2" /> Ziel der Dissertation von Susanne:<br>
  <span class="text-sm ml-10">Korpusstudie über 50 Filme.</span><br>
  <span class="text-sm ml-10">Erkenntnisse aus Filmmusik gewinnen.</span><br>
  <span class="text-sm ml-10">Dafür viele unterschiedliche Parameter betrachten.</span><br>
  <span class="text-sm ml-10">Zusammenhänge und Muster ermitteln, Modelle finden.</span>
* <mdi-book-open class="baseColor mr-2 mt-4" /> Beispiel:<br>
  <span class="text-sm ml-10">Beeinflusst Musik die Wahrnehmung des Zuschauers in Hinsicht auf (Un-)Vorhersehbarkeit des Ausgangs der Szene?</span><br>
  <span class="text-sm ml-10">Und wenn ja, welche Gestaltungsparameter in der Komposition sind dafür verantwortlich?</span>

</VClicks>

<div v-click class="text-2xl text-center mt-8 baseColor">
  <mdi-arrow-right class="mr-2 pt-1" />
  <span>Geht das nicht ohne einen Informatiker?</span>
  <mdi-arrow-left class="ml-2 pt-1" />
</div>

<!--
* "Modell" ist falsch, eigentlich "Filmmusikalische Topologien"
* Ohne Informatiker: Gibt es schon vergleichbares, an dem man sich orientieren kann?
-->

---

<div class="flex flex-row">
  <h1>Verwandte Arbeiten</h1>
  <div class="pt-3 pl-8 text-xl baseColor">Wissenschaftliche Arbeiten</div>
</div>

<VClicks class="space-y-0.5 text-xl">

* Betrachtung einzelner Filmcharaktere in kontextlosen und abstrakten Bewegbilder:
  * <span class="text-gray-400 text-sm">Annabel Cohen, Sandra K. Marshall [<AppLiteratureHyperlink>MC88</AppLiteratureHyperlink>]</span>
  * <span class="text-gray-400 text-sm">Bethold Hoeckner [<AppLiteratureHyperlink>Hoe11</AppLiteratureHyperlink>]</span>
* Einzelfilmanalysen:
  * <span class="text-gray-400 text-sm">Annabel Cohen zu dem Film "The red Violin" [<AppLiteratureHyperlink>Coh</AppLiteratureHyperlink>]</span>
* Filmübergreifende eingeschänkte Analysen:
  * <span class="text-gray-400 text-sm">Nathan Fink zu sechs Filmen von Alfred Hitchcock [<AppLiteratureHyperlink>Fin06</AppLiteratureHyperlink>]</span>
  * <span class="text-gray-400 text-sm">Pascal Rudolph zu 12 Filmen [<AppLiteratureHyperlink>Rud22</AppLiteratureHyperlink>]</span>
  * <span class="text-gray-400 text-sm">Philip Kümpel zu verschiedenen zufällig ausgewählten Filmen [<AppLiteratureHyperlink>Küm19</AppLiteratureHyperlink>]</span>
* Filmübergreifende vollständige Analysen:
  * <span class="text-red-500">?</span>

</VClicks>

<!--
* Keiner der Arbeiten deckt die Filme vollständig mit allen Parametern ab, z.B.:
  * Philip Kümpel konzentriert sich auf die Instrumentation
  * Pascal Rudolph nur zu ausgewählten Musikeinsätzen & nur 12 Filme  
    In deinem Buch "Präexistente Musik im Film" von 2022
  * Annabel Cohen, Sandra K. Marshall und Bethold Hoeckner lassen Filmdramaturgie komplett weg
* Warum also gibt es solch eine große, vollumfängliche Korpusstudie noch nicht? -> Überlegen wir uns einmal das Herangehen
-->

---

# Das Problem

Grobe Pipeline.

---

# Das Problem

Metadaten Film

---

# Das Problem

Parameter definieren

---

# Das Problem

Analyse

---

# Das Problem

Auswertung

---

# Das Problem

Erkenntnisse

---

# Warum gibt es solch große Korpusstudien noch nicht?

---

# Die Lösung: FMADB

Metadaten Film

---

# Die Lösung: FMADB

Parameter definieren

---

# Die Lösung: FMADB

Analyse

---

# Die Lösung: FMADB

Auswertung

---

# Die Lösung: FMADB

Erkenntnisse

---

# Ecosystem

---

Live Demo Anwendung & Dokumentation

---

# Backend Modell

---

# Besondere Hürden

---

# Entwicklung des Timeline-Ansatzes

---

# Abweichungen zur Arbeit

---

# Mehr in meiner schriftlichen Arbeit

---

# Literatur

---

Schlussfolie
