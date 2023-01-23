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
clicks: 5
---

# Das Problem

<div class="relative">

<AppAnalysisPipeline :animation="5" />

<div class="absolute bg-white w-35 h-full top-0 left-30" v-click-hide></div>
<div class="absolute bg-white w-30 h-full top-0 left-65" v-click-hide></div>
<div class="absolute bg-white w-37 h-full top-0 left-95" v-click-hide></div>
<div class="absolute bg-white w-39 h-full top-0 left-132" v-click-hide></div>

</div>

<!--
* Am Anfang stehen viele Filme ...
* ... am Ende wollen wir Erkenntnisse aus den Filmmusiken dieser haben
* Erkenntnisse vergleichbar mit anderen, nicht nur für sich selbst.
-->

---

# Das Problem

<AppAnalysisPipeline />

<AppArrowUp :nbr="1" />

<div class="px-3 flex flex-row">

<div class="w-45 mr-10 flex-shrink-0">
  <img src="/assets/movie-covers/tmdb-120.jpg" />
  <div class="text-right text-xs">
    &copy; themoviedb.org
  </div>
</div>

<VClicks class="text-lg">

* Unterschiedliche Namen (Sprachen & Länder)
  * [ger] Der Herr der Ringe - Die Gefährten
  * [eng] The Lord of the Rings: The Fellowship of the Ring
* Unterschiedliche Längen zwischen und innerhalb Länder
  * Kinofassung: 171 Minuten
  * Extended Edition: 218 Minuten
* Medium (Konvertierung & Kompression)
  * DVD, Netflix, Amazon Prime, ...

</VClicks>

</div>

---

# Das Problem

<AppAnalysisPipeline />

<AppArrowUp :nbr="2" />

<VClicks class="px-3 text-lg">

* viele <mdi-exclamation-thick class="text-red-500" />
  * BPM, Time Signature, Dynamic, Scale, Effect, Cluster, Function, ...
* unterschiedliche Herangehensweisen für gleiche Parameter
  * Hansjörg Pauli definiert 3 Funktionen von Filmmusik
  * Norbert Jürgen Schneider definiert 20 Funktionen von Filmmusik
* unterschiedliche Bezeichnungen für gleiche Parameter
  * Diegetische Musik == Inzidenzmusik == Source-Musik
* Parameter sind verschieden und facettenreich
  * z.B. BPM nicht nur reine Zahlen (Accelerando, Unbekannt, ...)

</VClicks>

<!--
* viele Parameter, welche nehme ich, welche bringen mir etwas?
* BPM:
  * Accelerando = schneller werden
  * Ritardando = langsamer werden
-->

---
clicks: 5
---

# Das Problem

<AppAnalysisPipeline />

<AppArrowUp :nbr="3" />

<div class="px-3 text-lg">

<table>
  <thead class="!font-bold">
    <tr>
      <td v-click="1" class="w-1/2 border-r-1">
        Computergestützt<br>
        <ul class="font-normal">
          <li v-click="2">Audiospuren</li>
          <li v-click="2" class="-mt-2">Musiknoten</li>
        </ul>
      </td>
      <td v-click="1" class="align-top">
        Händisch
      </td>
    </tr>
  </thead>
  <tbody>
    <tr v-click="3">
      <td class="border-r-1">
        Audiospur direkt technisch schwer, da Musik, Effekten und Sprache gemischt
      </td>
      <td>
      </td>
    </tr>
    <tr v-click="4">
      <td class="border-r-1">
        Rechtliches Problem bei direkter Verwendung
      </td>
      <td>
      </td>
    </tr>
    <tr v-click="5">
      <td colspan="2" class="text-center">
        Notenmaterial selten vorhanden
      </td>
    </tr>
  </tbody>
</table>

</div>

<!--
* separat veröffentlichte Soundtracks weichen von Filmen ab
* Doch wie visualisieren während der Analysen und der Eingaben der Daten?
-->

---
clicks: 4
---

# Das Problem

<AppAnalysisPipeline />

<AppArrowUp :nbr="4" />

<table class="-mt-4 -mb-5">
  <thead class="!font-bold">
    <tr>
      <td v-click="1" class="w-1/2 border-r-1">
        Tabellarisch
      </td>
      <td v-click="4" class="align-top">
        Andere Darstellungsarten?
      </td>
    </tr>
  </thead>
  <tbody>
    <tr v-click="1" class="!border-b-0">
      <td class="border-r-1">
        1. Eine Tabelle mit überlappenden Zeitintervallen
      </td>
      <td>
      </td>
    </tr>
    <tr v-click="1" class="!border-b-0">
      <td class="border-r-1">
        2. Eine Tabelle mit nicht überlappenden Zeitintervallen<br>
        <img src="/assets/parameter-example-tables/2_one-table-with-overlap_small.png"
             class="mt-1 w-90 animImg1" v-click="2" />
      </td>
      <td>
      </td>
    </tr>
    <tr v-click="1" class="!border-b-0">
      <td class="border-r-1">
        3. Mehrere Tabellen, eine pro Parameter<br>
        <img src="/assets/parameter-example-tables/3_multiple-tables-per-parameter_small.png"
             class="mt-1 animImg1" v-click="2" />
      </td>
      <td>
      </td>
    </tr>
  </tbody>
</table>

<img src="/assets/parameter-example-tables/2_one-table-with-overlap.png"
     v-click="3"
     class="animImg2 absolute bottom-40 left-20 z-10" />
<img src="/assets/parameter-example-tables/3_multiple-tables-per-parameter.png"
     v-click="3"
     class="animImg2 absolute bottom-10 left-21 z-10" />
<!-- <div v-click="3"
     class="absolute top-0 left-0 w-full h-full bg-white/75 z-1"></div> -->
<div v-click="3"
     class="absolute top-75 left-0 w-127 h-25 bg-white z-1"></div>
<div v-click="3"
     class="absolute top-109 left-0 w-127 h-18 bg-white z-1"></div>
<div v-click="3"
     class="absolute top-99 left-30 w-127 h-18 bg-white z-1"></div>

<!--
* Connectoren Bezeichnungen:
  * bei Bpm `Accelerando` & `Ritardando`
  * bei Dynamic `Crescendo` & `Decrescendo`
-->

---

# Das Problem

<AppAnalysisPipeline />

<AppArrowUp :nbr="5" />

<VClicks class="px-3 text-lg space-y-2">

* Schön wären Diagramme
* Tabellen oder Diagramme miteinander vergleichen

</VClicks>

---

# Das Problem

<AppAnalysisPipeline />

<AppArrowUp :nbr="6" />

<VClicks class="space-y-2 text-xl px-3">

* anderen zeigen und sich freuen 😊

</VClicks>

---

# Warum gibt es solch große Korpusstudien noch nicht?

<VClicks class="space-y-10 mt-15 text-xl">

* <mdi-image-size-select-small class="baseColor mr-2" /> Umfang<br>
  <span class="text-sm ml-10">Dateneingabe und Auswertung vereinfachen</span>
* <mdi-select-compare class="baseColor mr-2" /> Vergleichbarkeit<br>
  <span class="text-sm ml-10">einheitliche Struktur bereitstellen</span>
  
</VClicks>

<div v-click class="text-2xl text-center mt-11 text-gray-400">
  <mdi-arrow-right class="mr-2 pt-1" />
  <span class="line-through">Geht das nicht ohne einen Informatiker?</span>
  <mdi-arrow-left class="ml-2 pt-1" />
</div>

<div v-after class="text-2xl text-center mt-1 baseColor">
  <mdi-arrow-right class="mr-2 pt-1" />
  <span>Wir brauchen die Informatik als Lösung!</span>
  <mdi-arrow-left class="ml-2 pt-1" />
</div>

<!--
* nur vereinzelte filmübergreifende Studien, da sehr komplex und umfangreich
* Möglichkeit der Vereinheitlichung der Analysen filmübergreifend, da Film sehr individuell
  * Pascal Rudolph "Präexistente Musik im Film" 2022 [?] sagt schon in seiner Einleitung, dass er ueberall anders
    vorgehen musste
* von anderen kann man nicht nutzen, daher immer wieder von vorne
* Wie meine Recherche zeigte, gibt es momentan nichts hierfür //TODO grob als eigene Folie?
* Das heisst, wir muessen da ran.
-->

---

# Die Lösung: FMADB

<AppAnalysisPipeline />

<AppArrowUp :nbr="1" />

<div class="px-3 flex flex-row relative">

<div class="w-45 mr-10 flex-shrink-0">
  <img src="/assets/movie-covers/tmdb-120.jpg" />
  <div class="text-right text-xs">
    &copy; themoviedb.org
  </div>
</div>

<div class="text-lg text-gray-400 pt-9">

* Unterschiedliche Namen (Sprachen & Länder)
  * [ger] Der Herr der Ringe - Die Gefährten
  * [eng] The Lord of the Rings: The Fellowship of the Ring
* Unterschiedliche Längen zwischen und innerhalb Länder
  * Kinofassung: 171 Minuten
  * Extended Edition: 218 Minuten
* Medium (Konvertierung & Kompression)
  * DVD, Netflix, Amazon Prime, ...

</div>

<div class="w-full flex flex-row text-lg absolute left-56.5" v-click>
  <mdi-check class="text-green-500 mr-2" />
  Filme mit Metainformationen automatisch von
  <img src="/assets/TMDB_Asset3.svg" class="h-2.5 mx-2 mt-2.5" />
  crawlen
</div>

<div class="w-full text-lg absolute left-63.5 top-18 bg-white h-18" v-click>
<mdi-check class="text-green-500" /> global nur Englische Titel durch crawlen nutzen
</div>

<div class="w-full text-lg absolute left-63.5 top-42.5 bg-white h-18" v-click>
<mdi-check class="text-green-500" /> individuell vermerkbare Filmlänge durch Nutzer
</div>

<div class="w-full text-lg absolute left-63.5 top-67 bg-white" v-click>
<mdi-check class="text-green-500" /> individuell vermerkbar durch Nutzer
</div>

</div>

---

# Die Lösung: FMADB

<AppAnalysisPipeline />

<AppArrowUp :nbr="2" />

<div class="px-3 text-lg relative">

<div class="text-gray-400">

* viele <mdi-exclamation-thick class="text-red-500" />
  * BPM, Time Signature, Dynamic, Scale, Effect, Cluster, Function, ...
* unterschiedliche Herangehensweisen für gleiche Parameter
  * Hansjörg Pauli definiert 3 Funktionen von Filmmusik
  * Norbert Jürgen Schneider definiert 20 Funktionen von Filmmusik
* unterschiedliche Bezeichnungen für gleiche Parameter
  * Diegetische Musik == Inzidenzmusik == Source-Musik
* Parameter sind verschieden und facettenreich
  * z.B. BPM nicht nur reine Zahlen (Accelerando, Unbekannt, ...)

</div>

<div class="w-full absolute top-9 left-8 bg-white" v-click>
<mdi-check class="text-green-500" /> Fleißarbeit, aktuell nur grundlegende musiktheoretische Parameter
</div>

<div class="absolute top-3 right-4 border py-1 px-2 z-1" v-after>
Kategorien:
<ul>
  <li>Musiktheoretische Parameter</li>
  <li>Dramaturgische Parameter</li>
  <li>Bildgestalterische Parameter</li>
  <li>Drehbuchbezogene Parameter</li>
  <li>Wahrnehmungs-Parameter</li>
  <li>Sonstige Parameter</li>
</ul>
</div>

<div class="w-full absolute top-25 left-8 bg-white h-18" v-click>
<mdi-check class="text-green-500" /> festlegen und User ggf Freiraum ermöglichen
</div>

<div class="w-full absolute top-50 left-8 bg-white" v-click>
<mdi-check class="text-green-500" /> festlegen und User ggf Terminologieänderungen ermöglichen
</div>

<div class="w-full absolute top-66 left-8 bg-white" v-click>
<mdi-check class="text-green-500" /> Sonderfälle durch individuelle Lösungen abdecken
</div>

</div>

<!--
* Analyseparameter unterteilt in:
  * Musiktheoretischer Parameter
  * Dramaturgische Parameter
  * Bildgestalterische Parameter
  * Drehbuchbezogene Parameter
  * Wahrnehmungs-Parameter
  * Sonstiger Parameter
-->

---

# Die Lösung: FMADB

<AppAnalysisPipeline />

<AppArrowUp :nbr="3" />

<div class="px-3 text-lg relative">

<table class="text-gray-400">
  <thead class="!font-bold">
    <tr>
      <td class="w-1/2 border-r-1">
        Computergestützt<br>
        <ul class="font-normal">
          <li>Audiospuren</li>
          <li class="-mt-2">Musiknoten</li>
        </ul>
      </td>
      <td class="align-top">
        Händisch
      </td>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="border-r-1">
        Audiospur direkt technisch schwer, da Musik, Effekten und Sprache gemischt
      </td>
      <td>
      </td>
    </tr>
    <tr>
      <td class="border-r-1">
        Rechtliches Problem bei direkter Verwendung
      </td>
      <td>
      </td>
    </tr>
    <tr>
      <td colspan="2" class="text-center">
        Notenmaterial selten vorhanden
      </td>
    </tr>
  </tbody>
</table>

<div class="absolute flex flex-row left-111 top-1 z-10" v-click>
  <div class="border border-green-500 rounded-lg w-30 h-10 mr-2">
  </div>
  <mdi-check class="text-green-500 text-xl mt-1.5" />
</div>

<div class="bg-white absolute h-55 w-113 top-4.5 left-0" v-after></div>

</div>

<!--
* Rechtliche Probleme!
-->

---

# Die Lösung: FMADB

<AppAnalysisPipeline />

<AppArrowUp :nbr="4" />

<table class="-mt-4 -mb-5">
  <thead class="!font-bold">
    <tr>
      <td class="w-1/2 border-r-1 text-gray-400">
        Tabellarisch
      </td>
      <td class="align-top relative">
        <div class="text-gray-400" v-click-hide>
          Andere Darstellungsarten?
        </div>
        <div class="absolute left-2 top-3" v-after>
          Zeitleiste
        </div>
        <div class="absolute left-25 top-3 font-normal" v-click>
          mit Zeitleistenelementtypen:
        </div>
      </td>
    </tr>
  </thead>
  <tbody class="text-gray-400">
    <tr class="!border-b-0">
      <td class="border-r-1">
        1. Eine Tabelle mit überlappenden Zeitintervallen
      </td>
      <td>
      </td>
    </tr>
    <tr class="!border-b-0">
      <td class="border-r-1">
        2. Eine Tabelle mit nicht überlappenden Zeitintervallen<br>
        <img src="/assets/parameter-example-tables/2_one-table-with-overlap_small.png"
             class="mt-1 w-90 animImg1 opacity-80" />
      </td>
      <td>
      </td>
    </tr>
    <tr class="!border-b-0">
      <td class="border-r-1">
        3. Mehrere Tabellen, eine pro Parameter<br>
        <img src="/assets/parameter-example-tables/3_multiple-tables-per-parameter_small.png"
             class="mt-1 animImg1 opacity-80" />
      </td>
      <td>
      </td>
    </tr>
  </tbody>
</table>

<div class="absolute top-59 left-130">
  <div class="mb-3">1. Ein Wert, sequentiell (z.B. BPM, dynamic, root)</div>
  <div class="mb-3">2. Mehrere Werte, sequentiell (als 3 darstellen)</div>
  <div class="mb-3">3. Ein Wert, parallel (z.B. Orchestration)</div>
  <div class="mb-3">4. Mehrere Werte, parallel (als 3 darstellen)</div>
</div>

<!-- <div class="flex flex-row">
  <mdi-check class="text-green-500" />
  <span class="font-bold mx-1.5">Timeline</span>
  als Visualisierung mit Eingabehilfe
</div> -->

<div class="absolute top-90 left-135">
  <img src="/assets/miniTimeline.svg" class="w-95" />
</div>

<!--
* Wort `Auswertung` hier etwas irreführend, da nun zweierlei gemeint ist:
  * leichte Eingabe mit Visualisierung
  * Evaluation als Erkenntnissgewinn nach Dateneingabe
* Das wird in FMADB `Timeline` genannt
* Connectoren Bezeichnungen:
  * bei Bpm `Accelerando` & `Ritardando`
  * bei Dynamic `Crescendo` & `Decrescendo`
-->

---

# Das Problem

<AppAnalysisPipeline />

<AppArrowUp :nbr="5" />

<div class="px-3 text-lg space-y-2 text-gray-400">

* Schön wären Diagramme
* Tabellen oder Diagramme miteinander vergleichen

</div>

<div class="w-full flex flex-row justify-between mt-2" v-click>
  <img src="/assets/miniTimeline.svg" class="flex-shrink-0 h-40" />
  <img src="/assets/evaluation-examples/bpm.svg" class="flex-shrink-0 h-38" />
  <img src="/assets/evaluation-examples/dynamic.svg" class="flex-shrink-0 h-38" />
</div>

<ul class="absolute top-108 left-17 text-lg space-y-2" v-click>
  <li>
    <div class="flex flex-row">
      <div>
        Evaluationstypen
      </div>
      <div class="flex flex-col ml-6">
        <div>1. Auswertung einzelner Zeitleisten einzelner Filme</div>
        <div>2. Auswertung mehrerer Zeitleisten des gleichen Films</div>
        <div>3. Auswertung mehrerer Filme repräsentiert durch je eine Zeitleiste pro Film</div>
        <div>4. Allgemeine Auswertung der enthaltenen Daten in FMADB</div>
      </div>
    </div>
  </li>
</ul>

---

# Die Lösung: FMADB

<AppAnalysisPipeline />

<AppArrowUp :nbr="6" />

<div class="space-y-2 text-xl px-3 text-gray-400">

* anderen zeigen und sich freuen 😊

</div>

<div class="space-y-2 text-xl pl-10 pt-3" v-click>
  <mdi-check class="text-green-500" /> anderen umfangreicheres zeigen und sich noch mehr freuen 🤩
</div>

---

# Ecosystem

<div class="absolute top-12 right-19">
  <img src="/assets/EcosystemCommunication.svg" class="h-37" />
</div>

<div class="w-full h-0 relative mt-38" v-click>
  <div class="absolute top-0 left-0 w-full h-0.5 bg-gray-300 z-1"></div>
  <div class="absolute top-0 left-1/2 w-0 h-0 text-xl baseColor flex flex-row justify-center">
    <div class="-mt-3.5 z-10">
      <div class="bg-white px-3">
        Polyrepo
      </div>
    </div>
  </div>
</div>

<div class="w-full h-4"></div>

<div class="flex flex-row justify-between">
  <div class="py-1 px-4 w-69 flex-shrink-0" v-click>
    <div>
      <mdi-github class="mr-2" />
      <a href="https://github.com/toddeTV/FMADB_frontend" target="_blank">toddeTV/FMADB_frontend</a>
    </div>
    <div class="pl-7 mt-3">
      <div class="mb-3.5">Frontend mit:</div>
      <div class="flex flex-col space-y-3">
        <div>
          <LogosTypescriptIcon class="mr-2" /> TypeScript
        </div>
        <div>
          <LogosVue class="mr-2" /> Vue 3
        </div>
        <div>
          <LogosVueuse class="mr-2" /> VueUse
        </div>
        <div>
          <LogosApollostack class="mr-2" /> Apollo
        </div>
        <div>
          <VscodeIconsFileTypeLightQuasar class="mr-2" /> Quasar
        </div>
      </div>
    </div>
  </div>
  <div class="py-1 px-4 w-69 flex-shrink-0" v-click>
    <div>
      <mdi-github class="mr-2" />
      <a href="https://github.com/toddeTV/FMADB_backend" target="_blank">toddeTV/FMADB_backend</a>
    </div>
    <div class="pl-7 mt-3">
      <div class="mb-3.5">Backend mit:</div>
      <div class="flex flex-col space-y-3">
        <div>
          <LogosTypescriptIcon class="mr-2" /> TypeScript
        </div>
        <div>
          <LogosNestjs class="mr-2" /> NestJS
        </div>
        <div>
          <LogosPostgresql class="mr-2" /> PostgreSQL
        </div>
        <div>
          <LogosPrisma class="mr-2" /> Prisma
        </div>
        <div>
          <VscodeIconsFileTypeGraphql class="mr-2" /> GraphQL
        </div>
        <div>
          <VscodeIconsFileTypeRest class="mr-2" /> REST
        </div>
      </div>
    </div>
  </div>
  <div class="py-1 px-4 w-82 flex-shrink-0" v-click>
    <div>
      <mdi-github class="mr-2" />
      <a href="https://github.com/toddeTV/FMADB_documentation" target="_blank">toddeTV/FMADB_documentation</a>
    </div>
    <div class="pl-7 mt-3">
      <div class="mb-3.5">Dokumentation mit:</div>
      <div class="flex flex-col space-y-3">
        <div>
          <LogosTypescriptIcon class="mr-2" /> TypeScript
        </div>
        <div>
          <LogosVitejs class="mr-2" /> vitepress
        </div>
        <div>
          <LogosVue class="mr-2" /> Vue 3
        </div>
      </div>
    </div>
  </div>
</div>

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
