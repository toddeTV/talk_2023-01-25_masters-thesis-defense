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
  <svg class="w-100" viewBox="0 0 571 255" fill="none" xmlns="http://www.w3.org/2000/svg">
    <path d="M511.061 42.0607C511.646 41.4749 511.646 40.5251 511.061 39.9393L501.515 30.3934C500.929 29.8076 499.979 29.8076 499.393 30.3934C498.808 30.9792 498.808 31.9289 499.393 32.5147L507.879 41L499.393 49.4853C498.808 50.0711 498.808 51.0208 499.393 51.6066C499.979 52.1924 500.929 52.1924 501.515 51.6066L511.061 42.0607ZM112 42.5L510 42.5V39.5L112 39.5V42.5Z" fill="#999999"/>
    <path d="M526.848 36.3636V38.1392H519.781V36.3636H526.848ZM521.841 33.0966H523.936V46.0938C523.936 46.6856 524.022 47.1295 524.194 47.4254C524.371 47.7154 524.596 47.9107 524.868 48.0114C525.146 48.1061 525.439 48.1534 525.747 48.1534C525.978 48.1534 526.167 48.1416 526.315 48.1179C526.463 48.0883 526.582 48.0646 526.67 48.0469L527.097 49.929C526.955 49.9822 526.756 50.0355 526.502 50.0888C526.247 50.148 525.925 50.1776 525.534 50.1776C524.942 50.1776 524.362 50.0503 523.794 49.7958C523.232 49.5413 522.764 49.1536 522.391 48.6328C522.024 48.112 521.841 47.455 521.841 46.6619V33.0966ZM530 50V36.3636H532.095V50H530ZM531.065 34.0909C530.657 34.0909 530.304 33.9518 530.009 33.6737C529.719 33.3955 529.574 33.0611 529.574 32.6705C529.574 32.2798 529.719 31.9454 530.009 31.6673C530.304 31.3891 530.657 31.25 531.065 31.25C531.473 31.25 531.823 31.3891 532.113 31.6673C532.408 31.9454 532.556 32.2798 532.556 32.6705C532.556 33.0611 532.408 33.3955 532.113 33.6737C531.823 33.9518 531.473 34.0909 531.065 34.0909ZM535.932 50V36.3636H537.956V38.4943H538.134C538.418 37.7663 538.877 37.2011 539.51 36.7987C540.143 36.3903 540.904 36.1861 541.792 36.1861C542.691 36.1861 543.44 36.3903 544.038 36.7987C544.641 37.2011 545.112 37.7663 545.449 38.4943H545.591C545.941 37.79 546.464 37.2307 547.163 36.8164C547.861 36.3962 548.699 36.1861 549.675 36.1861C550.894 36.1861 551.892 36.5678 552.667 37.3313C553.442 38.0889 553.83 39.2696 553.83 40.8736V50H551.735V40.8736C551.735 39.8674 551.46 39.1483 550.909 38.7163C550.359 38.2842 549.711 38.0682 548.965 38.0682C548.006 38.0682 547.263 38.3582 546.737 38.9382C546.21 39.5123 545.946 40.2403 545.946 41.1222V50H543.816V40.6605C543.816 39.8852 543.564 39.2608 543.061 38.7873C542.558 38.3079 541.91 38.0682 541.117 38.0682C540.572 38.0682 540.063 38.2132 539.59 38.5032C539.122 38.7932 538.744 39.1957 538.454 39.7106C538.169 40.2196 538.027 40.8085 538.027 41.4773V50H535.932ZM563.378 50.2841C562.064 50.2841 560.931 49.9941 559.978 49.4141C559.031 48.8281 558.3 48.0114 557.785 46.9638C557.276 45.9103 557.022 44.6851 557.022 43.2884C557.022 41.8916 557.276 40.6605 557.785 39.5952C558.3 38.5239 559.016 37.6894 559.934 37.0916C560.857 36.4879 561.934 36.1861 563.165 36.1861C563.875 36.1861 564.577 36.3045 565.269 36.5412C565.962 36.7779 566.592 37.1626 567.16 37.6953C567.728 38.2221 568.181 38.9205 568.518 39.7905C568.856 40.6605 569.024 41.7318 569.024 43.0043V43.892H558.513V42.081H566.894C566.894 41.3116 566.74 40.625 566.432 40.0213C566.13 39.4176 565.698 38.9412 565.136 38.592C564.58 38.2428 563.923 38.0682 563.165 38.0682C562.331 38.0682 561.608 38.2753 560.999 38.6896C560.395 39.098 559.931 39.6307 559.605 40.2876C559.28 40.9446 559.117 41.6489 559.117 42.4006V43.608C559.117 44.6378 559.294 45.5108 559.649 46.2269C560.01 46.9371 560.511 47.4787 561.15 47.8516C561.789 48.2185 562.532 48.402 563.378 48.402C563.929 48.402 564.426 48.325 564.87 48.1712C565.319 48.0114 565.707 47.7746 566.033 47.4609C566.358 47.1413 566.61 46.7448 566.787 46.2713L568.811 46.8395C568.598 47.526 568.24 48.1297 567.737 48.6506C567.234 49.1655 566.613 49.5679 565.873 49.858C565.133 50.142 564.301 50.2841 563.378 50.2841Z" fill="#999999"/>
    <path d="M86.1201 24.2486C84.7825 24.2486 83.6432 23.8846 82.7021 23.1566C81.7611 22.4227 81.042 21.3603 80.5448 19.9695C80.0477 18.5727 79.7991 16.8859 79.7991 14.9091C79.7991 12.9441 80.0477 11.2662 80.5448 9.87535C81.0479 8.47857 81.77 7.41323 82.711 6.67933C83.658 5.93951 84.7944 5.5696 86.1201 5.5696C87.4459 5.5696 88.5793 5.93951 89.5203 6.67933C90.4673 7.41323 91.1894 8.47857 91.6865 9.87535C92.1896 11.2662 92.4411 12.9441 92.4411 14.9091C92.4411 16.8859 92.1926 18.5727 91.6954 19.9695C91.1982 21.3603 90.4791 22.4227 89.5381 23.1566C88.597 23.8846 87.4577 24.2486 86.1201 24.2486ZM86.1201 22.2955C87.4459 22.2955 88.4757 21.6562 89.2096 20.3778C89.9435 19.0994 90.3105 17.2765 90.3105 14.9091C90.3105 13.3348 90.1418 11.9942 89.8044 10.8874C89.473 9.78066 88.9936 8.93726 88.3662 8.35724C87.7448 7.77723 86.9961 7.48722 86.1201 7.48722C84.8062 7.48722 83.7793 8.1353 83.0395 9.43146C82.2997 10.7217 81.9298 12.5476 81.9298 14.9091C81.9298 16.4834 82.0955 17.821 82.4269 18.9219C82.7584 20.0227 83.2348 20.8602 83.8563 21.4343C84.4836 22.0084 85.2383 22.2955 86.1201 22.2955ZM101.745 24.2486C100.408 24.2486 99.2682 23.8846 98.3271 23.1566C97.3861 22.4227 96.667 21.3603 96.1698 19.9695C95.6727 18.5727 95.4241 16.8859 95.4241 14.9091C95.4241 12.9441 95.6727 11.2662 96.1698 9.87535C96.6729 8.47857 97.395 7.41323 98.336 6.67933C99.283 5.93951 100.419 5.5696 101.745 5.5696C103.071 5.5696 104.204 5.93951 105.145 6.67933C106.092 7.41323 106.814 8.47857 107.312 9.87535C107.815 11.2662 108.066 12.9441 108.066 14.9091C108.066 16.8859 107.818 18.5727 107.32 19.9695C106.823 21.3603 106.104 22.4227 105.163 23.1566C104.222 23.8846 103.083 24.2486 101.745 24.2486ZM101.745 22.2955C103.071 22.2955 104.101 21.6562 104.835 20.3778C105.569 19.0994 105.935 17.2765 105.935 14.9091C105.935 13.3348 105.767 11.9942 105.429 10.8874C105.098 9.78066 104.619 8.93726 103.991 8.35724C103.37 7.77723 102.621 7.48722 101.745 7.48722C100.431 7.48722 99.4043 8.1353 98.6645 9.43146C97.9247 10.7217 97.5548 12.5476 97.5548 14.9091C97.5548 16.4834 97.7205 17.821 98.0519 18.9219C98.3834 20.0227 98.8598 20.8602 99.4813 21.4343C100.109 22.0084 100.863 22.2955 101.745 22.2955ZM113.002 21.674C112.564 21.674 112.188 21.5172 111.875 21.2035C111.561 20.8898 111.404 20.514 111.404 20.076C111.404 19.638 111.561 19.2622 111.875 18.9485C112.188 18.6348 112.564 18.478 113.002 18.478C113.44 18.478 113.816 18.6348 114.13 18.9485C114.443 19.2622 114.6 19.638 114.6 20.076C114.6 20.366 114.526 20.6323 114.378 20.875C114.236 21.1177 114.044 21.313 113.801 21.4609C113.564 21.603 113.298 21.674 113.002 21.674ZM113.002 12.4766C112.564 12.4766 112.188 12.3197 111.875 12.006C111.561 11.6924 111.404 11.3165 111.404 10.8786C111.404 10.4406 111.561 10.0647 111.875 9.75107C112.188 9.43738 112.564 9.28054 113.002 9.28054C113.44 9.28054 113.816 9.43738 114.13 9.75107C114.443 10.0647 114.6 10.4406 114.6 10.8786C114.6 11.1686 114.526 11.4349 114.378 11.6776C114.236 11.9202 114.044 12.1155 113.801 12.2635C113.564 12.4055 113.298 12.4766 113.002 12.4766ZM124.255 24.2486C122.917 24.2486 121.778 23.8846 120.837 23.1566C119.896 22.4227 119.177 21.3603 118.68 19.9695C118.182 18.5727 117.934 16.8859 117.934 14.9091C117.934 12.9441 118.182 11.2662 118.68 9.87535C119.183 8.47857 119.905 7.41323 120.846 6.67933C121.793 5.93951 122.929 5.5696 124.255 5.5696C125.581 5.5696 126.714 5.93951 127.655 6.67933C128.602 7.41323 129.324 8.47857 129.821 9.87535C130.324 11.2662 130.576 12.9441 130.576 14.9091C130.576 16.8859 130.327 18.5727 129.83 19.9695C129.333 21.3603 128.614 22.4227 127.673 23.1566C126.732 23.8846 125.592 24.2486 124.255 24.2486ZM124.255 22.2955C125.581 22.2955 126.61 21.6562 127.344 20.3778C128.078 19.0994 128.445 17.2765 128.445 14.9091C128.445 13.3348 128.277 11.9942 127.939 10.8874C127.608 9.78066 127.128 8.93726 126.501 8.35724C125.88 7.77723 125.131 7.48722 124.255 7.48722C122.941 7.48722 121.914 8.1353 121.174 9.43146C120.434 10.7217 120.065 12.5476 120.065 14.9091C120.065 16.4834 120.23 17.821 120.562 18.9219C120.893 20.0227 121.37 20.8602 121.991 21.4343C122.618 22.0084 123.373 22.2955 124.255 22.2955ZM139.88 24.2486C138.542 24.2486 137.403 23.8846 136.462 23.1566C135.521 22.4227 134.802 21.3603 134.305 19.9695C133.807 18.5727 133.559 16.8859 133.559 14.9091C133.559 12.9441 133.807 11.2662 134.305 9.87535C134.808 8.47857 135.53 7.41323 136.471 6.67933C137.418 5.93951 138.554 5.5696 139.88 5.5696C141.206 5.5696 142.339 5.93951 143.28 6.67933C144.227 7.41323 144.949 8.47857 145.446 9.87535C145.949 11.2662 146.201 12.9441 146.201 14.9091C146.201 16.8859 145.952 18.5727 145.455 19.9695C144.958 21.3603 144.239 22.4227 143.298 23.1566C142.357 23.8846 141.217 24.2486 139.88 24.2486ZM139.88 22.2955C141.206 22.2955 142.235 21.6562 142.969 20.3778C143.703 19.0994 144.07 17.2765 144.07 14.9091C144.07 13.3348 143.902 11.9942 143.564 10.8874C143.233 9.78066 142.753 8.93726 142.126 8.35724C141.505 7.77723 140.756 7.48722 139.88 7.48722C138.566 7.48722 137.539 8.1353 136.799 9.43146C136.059 10.7217 135.69 12.5476 135.69 14.9091C135.69 16.4834 135.855 17.821 136.187 18.9219C136.518 20.0227 136.995 20.8602 137.616 21.4343C138.243 22.0084 138.998 22.2955 139.88 22.2955Z" fill="#999999"/>
    <path d="M260.122 24.2486C258.784 24.2486 257.645 23.8846 256.704 23.1566C255.763 22.4227 255.044 21.3603 254.547 19.9695C254.05 18.5727 253.801 16.8859 253.801 14.9091C253.801 12.9441 254.05 11.2662 254.547 9.87535C255.05 8.47857 255.772 7.41323 256.713 6.67933C257.66 5.93951 258.796 5.5696 260.122 5.5696C261.448 5.5696 262.581 5.93951 263.522 6.67933C264.469 7.41323 265.191 8.47857 265.688 9.87535C266.192 11.2662 266.443 12.9441 266.443 14.9091C266.443 16.8859 266.195 18.5727 265.697 19.9695C265.2 21.3603 264.481 22.4227 263.54 23.1566C262.599 23.8846 261.46 24.2486 260.122 24.2486ZM260.122 22.2955C261.448 22.2955 262.478 21.6562 263.212 20.3778C263.945 19.0994 264.312 17.2765 264.312 14.9091C264.312 13.3348 264.144 11.9942 263.806 10.8874C263.475 9.78066 262.996 8.93726 262.368 8.35724C261.747 7.77723 260.998 7.48722 260.122 7.48722C258.808 7.48722 257.781 8.1353 257.041 9.43146C256.302 10.7217 255.932 12.5476 255.932 14.9091C255.932 16.4834 256.097 17.821 256.429 18.9219C256.76 20.0227 257.237 20.8602 257.858 21.4343C258.486 22.0084 259.24 22.2955 260.122 22.2955ZM276.209 5.81818V24H274.007V8.12642H273.9L269.462 11.0739V8.83665L274.007 5.81818H276.209ZM283 21.674C282.562 21.674 282.186 21.5172 281.873 21.2035C281.559 20.8898 281.402 20.514 281.402 20.076C281.402 19.638 281.559 19.2622 281.873 18.9485C282.186 18.6348 282.562 18.478 283 18.478C283.438 18.478 283.814 18.6348 284.128 18.9485C284.441 19.2622 284.598 19.638 284.598 20.076C284.598 20.366 284.524 20.6323 284.376 20.875C284.234 21.1177 284.042 21.313 283.799 21.4609C283.563 21.603 283.296 21.674 283 21.674ZM283 12.4766C282.562 12.4766 282.186 12.3197 281.873 12.006C281.559 11.6924 281.402 11.3165 281.402 10.8786C281.402 10.4406 281.559 10.0647 281.873 9.75107C282.186 9.43738 282.562 9.28054 283 9.28054C283.438 9.28054 283.814 9.43738 284.128 9.75107C284.441 10.0647 284.598 10.4406 284.598 10.8786C284.598 11.1686 284.524 11.4349 284.376 11.6776C284.234 11.9202 284.042 12.1155 283.799 12.2635C283.563 12.4055 283.296 12.4766 283 12.4766ZM294.253 24.2486C292.915 24.2486 291.776 23.8846 290.835 23.1566C289.894 22.4227 289.175 21.3603 288.678 19.9695C288.18 18.5727 287.932 16.8859 287.932 14.9091C287.932 12.9441 288.18 11.2662 288.678 9.87535C289.181 8.47857 289.903 7.41323 290.844 6.67933C291.791 5.93951 292.927 5.5696 294.253 5.5696C295.579 5.5696 296.712 5.93951 297.653 6.67933C298.6 7.41323 299.322 8.47857 299.819 9.87535C300.322 11.2662 300.574 12.9441 300.574 14.9091C300.574 16.8859 300.325 18.5727 299.828 19.9695C299.331 21.3603 298.612 22.4227 297.671 23.1566C296.73 23.8846 295.591 24.2486 294.253 24.2486ZM294.253 22.2955C295.579 22.2955 296.609 21.6562 297.342 20.3778C298.076 19.0994 298.443 17.2765 298.443 14.9091C298.443 13.3348 298.275 11.9942 297.937 10.8874C297.606 9.78066 297.126 8.93726 296.499 8.35724C295.878 7.77723 295.129 7.48722 294.253 7.48722C292.939 7.48722 291.912 8.1353 291.172 9.43146C290.432 10.7217 290.063 12.5476 290.063 14.9091C290.063 16.4834 290.228 17.821 290.56 18.9219C290.891 20.0227 291.368 20.8602 291.989 21.4343C292.616 22.0084 293.371 22.2955 294.253 22.2955ZM309.878 24.2486C308.54 24.2486 307.401 23.8846 306.46 23.1566C305.519 22.4227 304.8 21.3603 304.303 19.9695C303.805 18.5727 303.557 16.8859 303.557 14.9091C303.557 12.9441 303.805 11.2662 304.303 9.87535C304.806 8.47857 305.528 7.41323 306.469 6.67933C307.416 5.93951 308.552 5.5696 309.878 5.5696C311.204 5.5696 312.337 5.93951 313.278 6.67933C314.225 7.41323 314.947 8.47857 315.444 9.87535C315.947 11.2662 316.199 12.9441 316.199 14.9091C316.199 16.8859 315.95 18.5727 315.453 19.9695C314.956 21.3603 314.237 22.4227 313.296 23.1566C312.355 23.8846 311.216 24.2486 309.878 24.2486ZM309.878 22.2955C311.204 22.2955 312.234 21.6562 312.967 20.3778C313.701 19.0994 314.068 17.2765 314.068 14.9091C314.068 13.3348 313.9 11.9942 313.562 10.8874C313.231 9.78066 312.751 8.93726 312.124 8.35724C311.503 7.77723 310.754 7.48722 309.878 7.48722C308.564 7.48722 307.537 8.1353 306.797 9.43146C306.057 10.7217 305.688 12.5476 305.688 14.9091C305.688 16.4834 305.853 17.821 306.185 18.9219C306.516 20.0227 306.993 20.8602 307.614 21.4343C308.241 22.0084 308.996 22.2955 309.878 22.2955Z" fill="#999999"/>
    <path d="M415.974 24.2486C414.636 24.2486 413.497 23.8846 412.556 23.1566C411.615 22.4227 410.896 21.3603 410.398 19.9695C409.901 18.5727 409.653 16.8859 409.653 14.9091C409.653 12.9441 409.901 11.2662 410.398 9.87535C410.901 8.47857 411.623 7.41323 412.565 6.67933C413.512 5.93951 414.648 5.5696 415.974 5.5696C417.299 5.5696 418.433 5.93951 419.374 6.67933C420.321 7.41323 421.043 8.47857 421.54 9.87535C422.043 11.2662 422.295 12.9441 422.295 14.9091C422.295 16.8859 422.046 18.5727 421.549 19.9695C421.052 21.3603 420.333 22.4227 419.392 23.1566C418.451 23.8846 417.311 24.2486 415.974 24.2486ZM415.974 22.2955C417.299 22.2955 418.329 21.6562 419.063 20.3778C419.797 19.0994 420.164 17.2765 420.164 14.9091C420.164 13.3348 419.995 11.9942 419.658 10.8874C419.326 9.78066 418.847 8.93726 418.22 8.35724C417.598 7.77723 416.85 7.48722 415.974 7.48722C414.66 7.48722 413.633 8.1353 412.893 9.43146C412.153 10.7217 411.783 12.5476 411.783 14.9091C411.783 16.4834 411.949 17.821 412.28 18.9219C412.612 20.0227 413.088 20.8602 413.71 21.4343C414.337 22.0084 415.092 22.2955 415.974 22.2955ZM431.812 24.2486C430.64 24.2486 429.595 24.0473 428.678 23.6449C427.766 23.2424 427.041 22.6831 426.503 21.967C425.97 21.2449 425.68 20.4074 425.633 19.4545H427.87C427.917 20.0405 428.119 20.5465 428.474 20.9727C428.829 21.3929 429.293 21.7184 429.867 21.9492C430.442 22.18 431.078 22.2955 431.776 22.2955C432.557 22.2955 433.25 22.1593 433.854 21.8871C434.457 21.6148 434.931 21.236 435.274 20.7507C435.617 20.2654 435.789 19.7031 435.789 19.0639C435.789 18.3951 435.623 17.8062 435.292 17.2972C434.96 16.7823 434.475 16.3799 433.836 16.0898C433.197 15.7998 432.415 15.6548 431.492 15.6548H430.036V13.7017H431.492C432.214 13.7017 432.847 13.5715 433.392 13.3111C433.942 13.0507 434.371 12.6837 434.679 12.2102C434.993 11.7367 435.15 11.1804 435.15 10.5412C435.15 9.92566 435.014 9.39003 434.741 8.9343C434.469 8.47857 434.084 8.12346 433.587 7.86896C433.096 7.61446 432.516 7.48722 431.847 7.48722C431.22 7.48722 430.628 7.60263 430.072 7.83345C429.521 8.05836 429.071 8.38684 428.722 8.81889C428.373 9.24503 428.184 9.75994 428.154 10.3636H426.023C426.059 9.41075 426.346 8.57623 426.884 7.86008C427.423 7.13802 428.127 6.57576 428.997 6.1733C429.873 5.77083 430.835 5.5696 431.883 5.5696C433.007 5.5696 433.972 5.79747 434.777 6.2532C435.582 6.70301 436.2 7.29782 436.632 8.03764C437.064 8.77746 437.28 9.57647 437.28 10.4347C437.28 11.4586 437.011 12.3316 436.473 13.0536C435.94 13.7757 435.215 14.2758 434.297 14.554V14.696C435.446 14.8854 436.342 15.3737 436.987 16.1609C437.633 16.9421 437.955 17.9098 437.955 19.0639C437.955 20.0523 437.686 20.9401 437.147 21.7273C436.615 22.5085 435.887 23.1241 434.963 23.5739C434.04 24.0237 432.989 24.2486 431.812 24.2486ZM443.149 21.674C442.711 21.674 442.335 21.5172 442.021 21.2035C441.708 20.8898 441.551 20.514 441.551 20.076C441.551 19.638 441.708 19.2622 442.021 18.9485C442.335 18.6348 442.711 18.478 443.149 18.478C443.587 18.478 443.963 18.6348 444.276 18.9485C444.59 19.2622 444.747 19.638 444.747 20.076C444.747 20.366 444.673 20.6323 444.525 20.875C444.383 21.1177 444.19 21.313 443.948 21.4609C443.711 21.603 443.445 21.674 443.149 21.674ZM443.149 12.4766C442.711 12.4766 442.335 12.3197 442.021 12.006C441.708 11.6924 441.551 11.3165 441.551 10.8786C441.551 10.4406 441.708 10.0647 442.021 9.75107C442.335 9.43738 442.711 9.28054 443.149 9.28054C443.587 9.28054 443.963 9.43738 444.276 9.75107C444.59 10.0647 444.747 10.4406 444.747 10.8786C444.747 11.1686 444.673 11.4349 444.525 11.6776C444.383 11.9202 444.19 12.1155 443.948 12.2635C443.711 12.4055 443.445 12.4766 443.149 12.4766ZM454.401 24.2486C453.064 24.2486 451.924 23.8846 450.983 23.1566C450.042 22.4227 449.323 21.3603 448.826 19.9695C448.329 18.5727 448.08 16.8859 448.08 14.9091C448.08 12.9441 448.329 11.2662 448.826 9.87535C449.329 8.47857 450.051 7.41323 450.992 6.67933C451.939 5.93951 453.076 5.5696 454.401 5.5696C455.727 5.5696 456.861 5.93951 457.802 6.67933C458.749 7.41323 459.471 8.47857 459.968 9.87535C460.471 11.2662 460.722 12.9441 460.722 14.9091C460.722 16.8859 460.474 18.5727 459.977 19.9695C459.479 21.3603 458.76 22.4227 457.819 23.1566C456.878 23.8846 455.739 24.2486 454.401 24.2486ZM454.401 22.2955C455.727 22.2955 456.757 21.6562 457.491 20.3778C458.225 19.0994 458.592 17.2765 458.592 14.9091C458.592 13.3348 458.423 11.9942 458.086 10.8874C457.754 9.78066 457.275 8.93726 456.647 8.35724C456.026 7.77723 455.277 7.48722 454.401 7.48722C453.087 7.48722 452.061 8.1353 451.321 9.43146C450.581 10.7217 450.211 12.5476 450.211 14.9091C450.211 16.4834 450.377 17.821 450.708 18.9219C451.04 20.0227 451.516 20.8602 452.138 21.4343C452.765 22.0084 453.52 22.2955 454.401 22.2955ZM470.026 24.2486C468.689 24.2486 467.549 23.8846 466.608 23.1566C465.667 22.4227 464.948 21.3603 464.451 19.9695C463.954 18.5727 463.705 16.8859 463.705 14.9091C463.705 12.9441 463.954 11.2662 464.451 9.87535C464.954 8.47857 465.676 7.41323 466.617 6.67933C467.564 5.93951 468.701 5.5696 470.026 5.5696C471.352 5.5696 472.486 5.93951 473.427 6.67933C474.374 7.41323 475.096 8.47857 475.593 9.87535C476.096 11.2662 476.347 12.9441 476.347 14.9091C476.347 16.8859 476.099 18.5727 475.602 19.9695C475.104 21.3603 474.385 22.4227 473.444 23.1566C472.503 23.8846 471.364 24.2486 470.026 24.2486ZM470.026 22.2955C471.352 22.2955 472.382 21.6562 473.116 20.3778C473.85 19.0994 474.217 17.2765 474.217 14.9091C474.217 13.3348 474.048 11.9942 473.711 10.8874C473.379 9.78066 472.9 8.93726 472.272 8.35724C471.651 7.77723 470.902 7.48722 470.026 7.48722C468.712 7.48722 467.686 8.1353 466.946 9.43146C466.206 10.7217 465.836 12.5476 465.836 14.9091C465.836 16.4834 466.002 17.821 466.333 18.9219C466.665 20.0227 467.141 20.8602 467.763 21.4343C468.39 22.0084 469.145 22.2955 470.026 22.2955Z" fill="#999999"/>
    <line x1="283.5" y1="31" x2="283.5" y2="50" stroke="#999999" stroke-width="3"/>
    <line x1="443.5" y1="31" x2="443.5" y2="50" stroke="#999999" stroke-width="3"/>
    <line x1="113.5" y1="31" x2="113.5" y2="255" stroke="#999999" stroke-width="3"/>
    <rect x="113.5" y="56.5" width="126" height="40" fill="#A6DEAB" stroke="black"/>
    <rect x="113.5" y="122.5" width="126" height="40" fill="#A6C6DE" stroke="black"/>
    <rect x="285.5" y="122.5" width="69" height="40" fill="#A6C6DE" stroke="black"/>
    <rect x="113.5" y="188.5" width="84" height="40" fill="#DEA6CE" stroke="black"/>
    <rect x="198.5" y="188.5" width="41" height="40" fill="#DEA6CE" stroke="black"/>
    <rect x="285.5" y="188.5" width="56" height="40" fill="#DEA6CE" stroke="black"/>
    <rect x="341.5" y="188.5" width="126" height="40" fill="#DEA6CE" stroke="black"/>
    <rect x="285.5" y="56.5" width="56" height="40" fill="#A6DEAB" stroke="black"/>
    <rect x="342.5" y="56.5" width="125" height="40" fill="#A6DEAB" stroke="black"/>
    <path d="M163.339 67.8182V86H161.137V70.1264H161.03L156.591 73.0739V70.8366L161.137 67.8182H163.339ZM174.498 86.2486C173.16 86.2486 172.021 85.8846 171.08 85.1566C170.139 84.4227 169.42 83.3603 168.923 81.9695C168.426 80.5727 168.177 78.8859 168.177 76.9091C168.177 74.9441 168.426 73.2662 168.923 71.8754C169.426 70.4786 170.148 69.4132 171.089 68.6793C172.036 67.9395 173.172 67.5696 174.498 67.5696C175.824 67.5696 176.957 67.9395 177.898 68.6793C178.845 69.4132 179.567 70.4786 180.064 71.8754C180.568 73.2662 180.819 74.9441 180.819 76.9091C180.819 78.8859 180.57 80.5727 180.073 81.9695C179.576 83.3603 178.857 84.4227 177.916 85.1566C176.975 85.8846 175.836 86.2486 174.498 86.2486ZM174.498 84.2955C175.824 84.2955 176.854 83.6562 177.588 82.3778C178.321 81.0994 178.688 79.2765 178.688 76.9091C178.688 75.3348 178.52 73.9942 178.182 72.8874C177.851 71.7807 177.372 70.9373 176.744 70.3572C176.123 69.7772 175.374 69.4872 174.498 69.4872C173.184 69.4872 172.157 70.1353 171.417 71.4315C170.678 72.7217 170.308 74.5476 170.308 76.9091C170.308 78.4834 170.473 79.821 170.805 80.9219C171.136 82.0227 171.613 82.8602 172.234 83.4343C172.862 84.0084 173.616 84.2955 174.498 84.2955ZM190.123 86.2486C188.785 86.2486 187.646 85.8846 186.705 85.1566C185.764 84.4227 185.045 83.3603 184.548 81.9695C184.051 80.5727 183.802 78.8859 183.802 76.9091C183.802 74.9441 184.051 73.2662 184.548 71.8754C185.051 70.4786 185.773 69.4132 186.714 68.6793C187.661 67.9395 188.797 67.5696 190.123 67.5696C191.449 67.5696 192.582 67.9395 193.523 68.6793C194.47 69.4132 195.192 70.4786 195.689 71.8754C196.193 73.2662 196.444 74.9441 196.444 76.9091C196.444 78.8859 196.195 80.5727 195.698 81.9695C195.201 83.3603 194.482 84.4227 193.541 85.1566C192.6 85.8846 191.461 86.2486 190.123 86.2486ZM190.123 84.2955C191.449 84.2955 192.479 83.6562 193.213 82.3778C193.946 81.0994 194.313 79.2765 194.313 76.9091C194.313 75.3348 194.145 73.9942 193.807 72.8874C193.476 71.7807 192.997 70.9373 192.369 70.3572C191.748 69.7772 190.999 69.4872 190.123 69.4872C188.809 69.4872 187.782 70.1353 187.042 71.4315C186.303 72.7217 185.933 74.5476 185.933 76.9091C185.933 78.4834 186.098 79.821 186.43 80.9219C186.761 82.0227 187.238 82.8602 187.859 83.4343C188.487 84.0084 189.241 84.2955 190.123 84.2955Z" fill="black"/>
    <path d="M305.646 86.2486C304.605 86.2486 303.667 86.0414 302.832 85.6271C301.998 85.2128 301.329 84.6446 300.826 83.9226C300.323 83.2005 300.047 82.3778 300 81.4545H302.131C302.214 82.2772 302.587 82.9579 303.249 83.4964C303.918 84.0291 304.717 84.2955 305.646 84.2955C306.392 84.2955 307.055 84.1209 307.635 83.7717C308.221 83.4225 308.68 82.9431 309.011 82.3335C309.348 81.7179 309.517 81.0225 309.517 80.2472C309.517 79.4541 309.343 78.7468 308.993 78.1254C308.65 77.498 308.177 77.0038 307.573 76.6428C306.969 76.2817 306.28 76.0982 305.504 76.0923C304.948 76.0864 304.377 76.1722 303.791 76.3498C303.205 76.5214 302.723 76.7434 302.344 77.0156L300.284 76.767L301.385 67.8182H310.831V69.7713H303.232L302.592 75.1335H302.699C303.072 74.8376 303.539 74.592 304.102 74.3967C304.664 74.2013 305.25 74.1037 305.86 74.1037C306.972 74.1037 307.964 74.37 308.834 74.9027C309.71 75.4295 310.396 76.1515 310.893 77.0689C311.396 77.9863 311.648 79.0339 311.648 80.2116C311.648 81.3717 311.387 82.4074 310.867 83.3189C310.352 84.2244 309.641 84.9406 308.736 85.4673C307.83 85.9882 306.801 86.2486 305.646 86.2486ZM321.105 86.2486C319.767 86.2486 318.628 85.8846 317.687 85.1566C316.746 84.4227 316.027 83.3603 315.53 81.9695C315.033 80.5727 314.784 78.8859 314.784 76.9091C314.784 74.9441 315.033 73.2662 315.53 71.8754C316.033 70.4786 316.755 69.4132 317.696 68.6793C318.643 67.9395 319.779 67.5696 321.105 67.5696C322.431 67.5696 323.564 67.9395 324.505 68.6793C325.452 69.4132 326.174 70.4786 326.671 71.8754C327.174 73.2662 327.426 74.9441 327.426 76.9091C327.426 78.8859 327.177 80.5727 326.68 81.9695C326.183 83.3603 325.464 84.4227 324.523 85.1566C323.582 85.8846 322.443 86.2486 321.105 86.2486ZM321.105 84.2955C322.431 84.2955 323.461 83.6562 324.194 82.3778C324.928 81.0994 325.295 79.2765 325.295 76.9091C325.295 75.3348 325.127 73.9942 324.789 72.8874C324.458 71.7807 323.978 70.9373 323.351 70.3572C322.73 69.7772 321.981 69.4872 321.105 69.4872C319.791 69.4872 318.764 70.1353 318.024 71.4315C317.285 72.7217 316.915 74.5476 316.915 76.9091C316.915 78.4834 317.08 79.821 317.412 80.9219C317.743 82.0227 318.22 82.8602 318.841 83.4343C319.468 84.0084 320.223 84.2955 321.105 84.2955Z" fill="black"/>
    <path d="M392.692 86L400.824 69.9134V69.7713H391.449V67.8182H403.097V69.8778L395 86H392.692ZM411.946 86.2486C410.608 86.2486 409.469 85.8846 408.528 85.1566C407.587 84.4227 406.868 83.3603 406.371 81.9695C405.873 80.5727 405.625 78.8859 405.625 76.9091C405.625 74.9441 405.873 73.2662 406.371 71.8754C406.874 70.4786 407.596 69.4132 408.537 68.6793C409.484 67.9395 410.62 67.5696 411.946 67.5696C413.272 67.5696 414.405 67.9395 415.346 68.6793C416.293 69.4132 417.015 70.4786 417.512 71.8754C418.015 73.2662 418.267 74.9441 418.267 76.9091C418.267 78.8859 418.018 80.5727 417.521 81.9695C417.024 83.3603 416.305 84.4227 415.364 85.1566C414.423 85.8846 413.283 86.2486 411.946 86.2486ZM411.946 84.2955C413.272 84.2955 414.301 83.6562 415.035 82.3778C415.769 81.0994 416.136 79.2765 416.136 76.9091C416.136 75.3348 415.967 73.9942 415.63 72.8874C415.299 71.7807 414.819 70.9373 414.192 70.3572C413.57 69.7772 412.822 69.4872 411.946 69.4872C410.632 69.4872 409.605 70.1353 408.865 71.4315C408.125 72.7217 407.755 74.5476 407.755 76.9091C407.755 78.4834 407.921 79.821 408.253 80.9219C408.584 82.0227 409.061 82.8602 409.682 83.4343C410.309 84.0084 411.064 84.2955 411.946 84.2955Z" fill="black"/>
    <path d="M49.7115 86V67.8182H51.8066V74.5298H51.9842C52.1381 74.2931 52.3511 73.9912 52.6234 73.6243C52.9016 73.2514 53.2981 72.92 53.813 72.63C54.3339 72.334 55.0382 72.1861 55.926 72.1861C57.0742 72.1861 58.0862 72.4731 58.9622 73.0472C59.8381 73.6213 60.5217 74.4351 61.013 75.4886C61.5042 76.5421 61.7498 77.785 61.7498 79.2173C61.7498 80.6615 61.5042 81.9132 61.013 82.9727C60.5217 84.0262 59.8411 84.8429 58.9711 85.4229C58.101 85.997 57.0978 86.2841 55.9615 86.2841C55.0855 86.2841 54.3842 86.1391 53.8574 85.8491C53.3307 85.5531 52.9252 85.2187 52.6412 84.8459C52.3571 84.4671 52.1381 84.1534 51.9842 83.9048H51.7356V86H49.7115ZM51.7711 79.1818C51.7711 80.2116 51.9221 81.1201 52.2239 81.9073C52.5257 82.6886 52.9667 83.3011 53.5467 83.745C54.1267 84.183 54.8369 84.402 55.6774 84.402C56.5533 84.402 57.2843 84.1712 57.8702 83.7095C58.4621 83.242 58.906 82.6146 59.2019 81.8274C59.5037 81.0343 59.6547 80.1525 59.6547 79.1818C59.6547 78.223 59.5067 77.3589 59.2108 76.5895C58.9208 75.8142 58.4798 75.2016 57.888 74.7518C57.302 74.296 56.5652 74.0682 55.6774 74.0682C54.8251 74.0682 54.109 74.2842 53.5289 74.7163C52.9489 75.1424 52.5109 75.7402 52.215 76.5096C51.9191 77.2731 51.7711 78.1638 51.7711 79.1818ZM64.9547 91.1136V72.3636H66.9789V74.5298H67.2275C67.3813 74.2931 67.5944 73.9912 67.8667 73.6243C68.1448 73.2514 68.5414 72.92 69.0563 72.63C69.5771 72.334 70.2814 72.1861 71.1692 72.1861C72.3174 72.1861 73.3295 72.4731 74.2054 73.0472C75.0814 73.6213 75.765 74.4351 76.2562 75.4886C76.7475 76.5421 76.9931 77.785 76.9931 79.2173C76.9931 80.6615 76.7475 81.9132 76.2562 82.9727C75.765 84.0262 75.0843 84.8429 74.2143 85.4229C73.3443 85.997 72.3411 86.2841 71.2047 86.2841C70.3288 86.2841 69.6274 86.1391 69.1007 85.8491C68.5739 85.5531 68.1685 85.2187 67.8844 84.8459C67.6003 84.4671 67.3813 84.1534 67.2275 83.9048H67.0499V91.1136H64.9547ZM67.0144 79.1818C67.0144 80.2116 67.1653 81.1201 67.4672 81.9073C67.769 82.6886 68.2099 83.3011 68.79 83.745C69.37 84.183 70.0802 84.402 70.9206 84.402C71.7966 84.402 72.5275 84.1712 73.1135 83.7095C73.7053 83.242 74.1492 82.6146 74.4451 81.8274C74.747 81.0343 74.8979 80.1525 74.8979 79.1818C74.8979 78.223 74.7499 77.3589 74.454 76.5895C74.164 75.8142 73.7231 75.2016 73.1312 74.7518C72.5453 74.296 71.8084 74.0682 70.9206 74.0682C70.0684 74.0682 69.3522 74.2842 68.7722 74.7163C68.1922 75.1424 67.7542 75.7402 67.4583 76.5096C67.1623 77.2731 67.0144 78.1638 67.0144 79.1818ZM80.1891 86V72.3636H82.2132V74.4943H82.3908C82.6749 73.7663 83.1336 73.2011 83.7669 72.7987C84.4002 72.3903 85.1607 72.1861 86.0485 72.1861C86.9481 72.1861 87.6968 72.3903 88.2946 72.7987C88.8983 73.2011 89.3688 73.7663 89.7061 74.4943H89.8482C90.1974 73.79 90.7212 73.2307 91.4196 72.8164C92.118 72.3962 92.9554 72.1861 93.932 72.1861C95.1512 72.1861 96.1485 72.5678 96.9238 73.3313C97.6992 74.0889 98.0868 75.2696 98.0868 76.8736V86H95.9917V76.8736C95.9917 75.8674 95.7164 75.1483 95.166 74.7163C94.6156 74.2842 93.9675 74.0682 93.2218 74.0682C92.263 74.0682 91.5202 74.3582 90.9934 74.9382C90.4667 75.5123 90.2033 76.2403 90.2033 77.1222V86H88.0726V76.6605C88.0726 75.8852 87.8211 75.2608 87.318 74.7873C86.8149 74.3079 86.1668 74.0682 85.3738 74.0682C84.8292 74.0682 84.3203 74.2132 83.8468 74.5032C83.3792 74.7932 83.0004 75.1957 82.7104 75.7106C82.4263 76.2196 82.2843 76.8085 82.2843 77.4773V86H80.1891Z" fill="black"/>
    <path d="M7.28649 152.284C6.15012 152.284 5.14693 151.997 4.2769 151.423C3.40687 150.843 2.72624 150.026 2.235 148.973C1.74376 147.913 1.49814 146.661 1.49814 145.217C1.49814 143.785 1.74376 142.542 2.235 141.489C2.72624 140.435 3.40983 139.621 4.28578 139.047C5.16172 138.473 6.1738 138.186 7.322 138.186C8.20978 138.186 8.91113 138.334 9.42605 138.63C9.94688 138.92 10.3434 139.251 10.6157 139.624C10.8939 139.991 11.1099 140.293 11.2638 140.53H11.4413V133.818H13.5365V152H11.5123V149.905H11.2638C11.1099 150.153 10.8909 150.467 10.6068 150.846C10.3227 151.219 9.91729 151.553 9.39054 151.849C8.86378 152.139 8.16244 152.284 7.28649 152.284ZM7.57058 150.402C8.41101 150.402 9.12124 150.183 9.70126 149.745C10.2813 149.301 10.7222 148.689 11.0241 147.907C11.3259 147.12 11.4768 146.212 11.4768 145.182C11.4768 144.164 11.3289 143.273 11.0329 142.51C10.737 141.74 10.299 141.142 9.71902 140.716C9.139 140.284 8.42285 140.068 7.57058 140.068C6.68279 140.068 5.94297 140.296 5.35112 140.752C4.76518 141.202 4.32425 141.814 4.02832 142.589C3.73831 143.359 3.59331 144.223 3.59331 145.182C3.59331 146.152 3.74127 147.034 4.0372 147.827C4.33905 148.615 4.78294 149.242 5.36887 149.71C5.96073 150.171 6.69463 150.402 7.57058 150.402ZM19.0141 157.114C18.659 157.114 18.3424 157.084 18.0642 157.025C17.786 156.972 17.5937 156.918 17.4871 156.865L18.0198 155.018C18.5288 155.149 18.9786 155.196 19.3692 155.161C19.7599 155.125 20.1061 154.95 20.4079 154.637C20.7157 154.329 20.9968 153.829 21.2513 153.136L21.642 152.071L16.5993 138.364H18.8721L22.6363 149.23H22.7783L26.5425 138.364H28.8153L23.0269 153.989C22.7665 154.693 22.4439 155.276 22.0592 155.738C21.6745 156.205 21.2277 156.551 20.7187 156.776C20.2156 157.001 19.6474 157.114 19.0141 157.114ZM33.6759 143.797V152H31.5807V138.364H33.6048V140.494H33.7824C34.102 139.802 34.5873 139.246 35.2384 138.825C35.8894 138.399 36.7298 138.186 37.7597 138.186C38.683 138.186 39.4909 138.375 40.1833 138.754C40.8758 139.127 41.4144 139.695 41.7991 140.459C42.1838 141.216 42.3762 142.175 42.3762 143.335V152H40.281V143.477C40.281 142.406 40.0028 141.571 39.4465 140.974C38.8901 140.37 38.1266 140.068 37.156 140.068C36.4872 140.068 35.8894 140.213 35.3627 140.503C34.8418 140.793 34.4305 141.216 34.1286 141.773C33.8268 142.329 33.6759 143.004 33.6759 143.797ZM50.2175 152.32C49.3534 152.32 48.5692 152.157 47.8649 151.831C47.1606 151.5 46.6013 151.023 46.187 150.402C45.7727 149.775 45.5655 149.017 45.5655 148.129C45.5655 147.348 45.7194 146.715 46.0272 146.229C46.3349 145.738 46.7463 145.353 47.2612 145.075C47.7761 144.797 48.3443 144.59 48.9657 144.454C49.5931 144.312 50.2234 144.199 50.8567 144.116C51.6853 144.01 52.3571 143.93 52.872 143.877C53.3928 143.818 53.7716 143.72 54.0083 143.584C54.251 143.448 54.3723 143.211 54.3723 142.874V142.803C54.3723 141.927 54.1326 141.246 53.6532 140.761C53.1797 140.275 52.4606 140.033 51.4959 140.033C50.4957 140.033 49.7115 140.252 49.1433 140.69C48.5751 141.128 48.1756 141.595 47.9448 142.092L45.9561 141.382C46.3113 140.554 46.7847 139.908 47.3766 139.447C47.9744 138.979 48.6254 138.654 49.3297 138.47C50.04 138.281 50.7383 138.186 51.4249 138.186C51.8629 138.186 52.3659 138.239 52.9341 138.346C53.5082 138.446 54.0616 138.657 54.5943 138.976C55.1329 139.296 55.5797 139.778 55.9348 140.423C56.29 141.068 56.4675 141.933 56.4675 143.016V152H54.3723V150.153H54.2658C54.1238 150.449 53.887 150.766 53.5556 151.103C53.2241 151.441 52.7832 151.728 52.2328 151.964C51.6824 152.201 51.0106 152.32 50.2175 152.32ZM50.5371 150.438C51.3657 150.438 52.0641 150.275 52.6323 149.949C53.2064 149.624 53.6384 149.203 53.9284 148.689C54.2244 148.174 54.3723 147.632 54.3723 147.064V145.146C54.2836 145.253 54.0882 145.35 53.7864 145.439C53.4905 145.522 53.1472 145.596 52.7566 145.661C52.3719 145.72 51.996 145.774 51.6291 145.821C51.2681 145.862 50.9751 145.898 50.7502 145.928C50.2057 145.999 49.6967 146.114 49.2232 146.274C48.7556 146.428 48.3768 146.661 48.0868 146.975C47.8027 147.283 47.6607 147.703 47.6607 148.236C47.6607 148.964 47.93 149.514 48.4686 149.887C49.0131 150.254 49.7026 150.438 50.5371 150.438ZM60.2916 152V138.364H62.3158V140.494H62.4933C62.7774 139.766 63.2361 139.201 63.8694 138.799C64.5027 138.39 65.2632 138.186 66.151 138.186C67.0506 138.186 67.7993 138.39 68.3971 138.799C69.0008 139.201 69.4713 139.766 69.8087 140.494H69.9507C70.2999 139.79 70.8237 139.231 71.5221 138.816C72.2205 138.396 73.058 138.186 74.0345 138.186C75.2538 138.186 76.251 138.568 77.0264 139.331C77.8017 140.089 78.1894 141.27 78.1894 142.874V152H76.0942V142.874C76.0942 141.867 75.819 141.148 75.2686 140.716C74.7181 140.284 74.07 140.068 73.3243 140.068C72.3655 140.068 71.6227 140.358 71.096 140.938C70.5692 141.512 70.3058 142.24 70.3058 143.122V152H68.1752V142.661C68.1752 141.885 67.9236 141.261 67.4205 140.787C66.9175 140.308 66.2694 140.068 65.4763 140.068C64.9318 140.068 64.4228 140.213 63.9493 140.503C63.4817 140.793 63.103 141.196 62.8129 141.711C62.5289 142.22 62.3868 142.808 62.3868 143.477V152H60.2916ZM82.0202 152V138.364H84.1153V152H82.0202ZM83.0855 136.091C82.6771 136.091 82.325 135.952 82.029 135.674C81.739 135.395 81.594 135.061 81.594 134.67C81.594 134.28 81.739 133.945 82.029 133.667C82.325 133.389 82.6771 133.25 83.0855 133.25C83.4939 133.25 83.8431 133.389 84.1331 133.667C84.429 133.945 84.577 134.28 84.577 134.67C84.577 135.061 84.429 135.395 84.1331 135.674C83.8431 135.952 83.4939 136.091 83.0855 136.091ZM93.4925 152.284C92.2141 152.284 91.1133 151.982 90.19 151.379C89.2667 150.775 88.5565 149.943 88.0593 148.884C87.5621 147.824 87.3136 146.614 87.3136 145.253C87.3136 143.868 87.5681 142.646 88.0771 141.586C88.592 140.521 89.3081 139.689 90.2255 139.092C91.1488 138.488 92.226 138.186 93.457 138.186C94.4158 138.186 95.2799 138.364 96.0494 138.719C96.8188 139.074 97.4491 139.571 97.9403 140.21C98.4316 140.849 98.7364 141.595 98.8548 142.447H96.7596C96.5998 141.826 96.2447 141.276 95.6942 140.796C95.1497 140.311 94.4158 140.068 93.4925 140.068C92.6758 140.068 91.9596 140.281 91.3441 140.707C90.7345 141.128 90.258 141.722 89.9148 142.492C89.5774 143.255 89.4087 144.152 89.4087 145.182C89.4087 146.235 89.5745 147.153 89.9059 147.934C90.2433 148.715 90.7167 149.322 91.3263 149.754C91.9419 150.186 92.6639 150.402 93.4925 150.402C94.0371 150.402 94.5312 150.307 94.9751 150.118C95.419 149.929 95.7949 149.656 96.1026 149.301C96.4104 148.946 96.6294 148.52 96.7596 148.023H98.8548C98.7364 148.828 98.4434 149.553 97.9759 150.198C97.5142 150.837 96.9016 151.346 96.1381 151.725C95.3806 152.098 94.4987 152.284 93.4925 152.284Z" fill="black"/>
    <path d="M155.061 133.818V152H152.966V133.818H155.061ZM164.438 152.284C163.207 152.284 162.127 151.991 161.198 151.405C160.275 150.819 159.553 150 159.032 148.946C158.517 147.893 158.259 146.661 158.259 145.253C158.259 143.832 158.517 142.592 159.032 141.533C159.553 140.474 160.275 139.651 161.198 139.065C162.127 138.479 163.207 138.186 164.438 138.186C165.669 138.186 166.747 138.479 167.67 139.065C168.599 139.651 169.321 140.474 169.836 141.533C170.357 142.592 170.617 143.832 170.617 145.253C170.617 146.661 170.357 147.893 169.836 148.946C169.321 150 168.599 150.819 167.67 151.405C166.747 151.991 165.669 152.284 164.438 152.284ZM164.438 150.402C165.373 150.402 166.143 150.162 166.747 149.683C167.35 149.203 167.797 148.573 168.087 147.792C168.377 147.011 168.522 146.164 168.522 145.253C168.522 144.341 168.377 143.492 168.087 142.705C167.797 141.918 167.35 141.281 166.747 140.796C166.143 140.311 165.373 140.068 164.438 140.068C163.503 140.068 162.734 140.311 162.13 140.796C161.526 141.281 161.08 141.918 160.79 142.705C160.5 143.492 160.355 144.341 160.355 145.253C160.355 146.164 160.5 147.011 160.79 147.792C161.08 148.573 161.526 149.203 162.13 149.683C162.734 150.162 163.503 150.402 164.438 150.402ZM182.409 146.425V138.364H184.504V152H182.409V149.692H182.267C181.948 150.384 181.451 150.973 180.776 151.458C180.101 151.938 179.249 152.178 178.219 152.178C177.367 152.178 176.609 151.991 175.946 151.618C175.283 151.239 174.763 150.671 174.384 149.914C174.005 149.15 173.816 148.188 173.816 147.028V138.364H175.911V146.886C175.911 147.881 176.189 148.674 176.745 149.266C177.308 149.857 178.024 150.153 178.894 150.153C179.415 150.153 179.944 150.02 180.483 149.754C181.027 149.488 181.483 149.079 181.85 148.529C182.223 147.978 182.409 147.277 182.409 146.425ZM193.491 152.284C192.355 152.284 191.352 151.997 190.481 151.423C189.611 150.843 188.931 150.026 188.44 148.973C187.948 147.913 187.703 146.661 187.703 145.217C187.703 143.785 187.948 142.542 188.44 141.489C188.931 140.435 189.614 139.621 190.49 139.047C191.366 138.473 192.378 138.186 193.527 138.186C194.414 138.186 195.116 138.334 195.631 138.63C196.151 138.92 196.548 139.251 196.82 139.624C197.098 139.991 197.314 140.293 197.468 140.53H197.646V133.818H199.741V152H197.717V149.905H197.468C197.314 150.153 197.095 150.467 196.811 150.846C196.527 151.219 196.122 151.553 195.595 151.849C195.068 152.139 194.367 152.284 193.491 152.284ZM193.775 150.402C194.616 150.402 195.326 150.183 195.906 149.745C196.486 149.301 196.927 148.689 197.229 147.907C197.53 147.12 197.681 146.212 197.681 145.182C197.681 144.164 197.533 143.273 197.238 142.51C196.942 141.74 196.504 141.142 195.924 140.716C195.344 140.284 194.627 140.068 193.775 140.068C192.887 140.068 192.148 140.296 191.556 140.752C190.97 141.202 190.529 141.814 190.233 142.589C189.943 143.359 189.798 144.223 189.798 145.182C189.798 146.152 189.946 147.034 190.242 147.827C190.544 148.615 190.988 149.242 191.573 149.71C192.165 150.171 192.899 150.402 193.775 150.402Z" fill="black"/>
    <path d="M301.559 157.114V149.905H301.381C301.227 150.153 301.008 150.467 300.724 150.846C300.44 151.219 300.034 151.553 299.508 151.849C298.981 152.139 298.28 152.284 297.404 152.284C296.267 152.284 295.264 151.997 294.394 151.423C293.524 150.843 292.843 150.026 292.352 148.973C291.861 147.913 291.615 146.661 291.615 145.217C291.615 143.785 291.861 142.542 292.352 141.489C292.843 140.435 293.527 139.621 294.403 139.047C295.279 138.473 296.291 138.186 297.439 138.186C298.327 138.186 299.028 138.334 299.543 138.63C300.064 138.92 300.461 139.251 300.733 139.624C301.011 139.991 301.227 140.293 301.381 140.53H301.63V138.364H303.654V157.114H301.559ZM297.688 150.402C298.528 150.402 299.238 150.183 299.818 149.745C300.398 149.301 300.839 148.689 301.141 147.907C301.443 147.12 301.594 146.212 301.594 145.182C301.594 144.164 301.446 143.273 301.15 142.51C300.854 141.74 300.416 141.142 299.836 140.716C299.256 140.284 298.54 140.068 297.688 140.068C296.8 140.068 296.06 140.296 295.468 140.752C294.882 141.202 294.441 141.814 294.146 142.589C293.855 143.359 293.71 144.223 293.71 145.182C293.71 146.152 293.858 147.034 294.154 147.827C294.456 148.615 294.9 149.242 295.486 149.71C296.078 150.171 296.812 150.402 297.688 150.402ZM316.083 146.425V138.364H318.178V152H316.083V149.692H315.941C315.621 150.384 315.124 150.973 314.449 151.458C313.774 151.938 312.922 152.178 311.892 152.178C311.04 152.178 310.282 151.991 309.62 151.618C308.957 151.239 308.436 150.671 308.057 149.914C307.678 149.15 307.489 148.188 307.489 147.028V138.364H309.584V146.886C309.584 147.881 309.862 148.674 310.419 149.266C310.981 149.857 311.697 150.153 312.567 150.153C313.088 150.153 313.618 150.02 314.156 149.754C314.701 149.488 315.156 149.079 315.523 148.529C315.896 147.978 316.083 147.277 316.083 146.425ZM322.015 152V138.364H324.11V152H322.015ZM323.081 136.091C322.672 136.091 322.32 135.952 322.024 135.674C321.734 135.395 321.589 135.061 321.589 134.67C321.589 134.28 321.734 133.945 322.024 133.667C322.32 133.389 322.672 133.25 323.081 133.25C323.489 133.25 323.838 133.389 324.128 133.667C324.424 133.945 324.572 134.28 324.572 134.67C324.572 135.061 324.424 135.395 324.128 135.674C323.838 135.952 323.489 136.091 323.081 136.091ZM333.665 152.284C332.351 152.284 331.218 151.994 330.265 151.414C329.318 150.828 328.587 150.011 328.072 148.964C327.563 147.91 327.309 146.685 327.309 145.288C327.309 143.892 327.563 142.661 328.072 141.595C328.587 140.524 329.303 139.689 330.221 139.092C331.144 138.488 332.221 138.186 333.452 138.186C334.162 138.186 334.864 138.304 335.556 138.541C336.249 138.778 336.879 139.163 337.447 139.695C338.015 140.222 338.468 140.92 338.805 141.79C339.143 142.661 339.312 143.732 339.312 145.004V145.892H328.8V144.081H337.181C337.181 143.312 337.027 142.625 336.719 142.021C336.417 141.418 335.985 140.941 335.423 140.592C334.867 140.243 334.21 140.068 333.452 140.068C332.618 140.068 331.896 140.275 331.286 140.69C330.682 141.098 330.218 141.631 329.892 142.288C329.567 142.945 329.404 143.649 329.404 144.401V145.608C329.404 146.638 329.581 147.511 329.937 148.227C330.298 148.937 330.798 149.479 331.437 149.852C332.076 150.219 332.819 150.402 333.665 150.402C334.216 150.402 334.713 150.325 335.157 150.171C335.607 150.011 335.994 149.775 336.32 149.461C336.645 149.141 336.897 148.745 337.074 148.271L339.098 148.839C338.885 149.526 338.527 150.13 338.024 150.651C337.521 151.165 336.9 151.568 336.16 151.858C335.42 152.142 334.589 152.284 333.665 152.284ZM348.429 138.364V140.139H341.362V138.364H348.429ZM343.422 135.097H345.517V148.094C345.517 148.686 345.603 149.129 345.775 149.425C345.952 149.715 346.177 149.911 346.449 150.011C346.727 150.106 347.02 150.153 347.328 150.153C347.559 150.153 347.748 150.142 347.896 150.118C348.044 150.088 348.163 150.065 348.252 150.047L348.678 151.929C348.536 151.982 348.337 152.036 348.083 152.089C347.828 152.148 347.506 152.178 347.115 152.178C346.523 152.178 345.943 152.05 345.375 151.796C344.813 151.541 344.345 151.154 343.972 150.633C343.605 150.112 343.422 149.455 343.422 148.662V135.097Z" fill="black"/>
    <rect x="354.5" y="122.5" width="34" height="40" fill="#A6C6DE" stroke="black"/>
    <rect x="388.5" y="122.5" width="79" height="40" fill="#A6C6DE" stroke="black"/>
    <path d="M374.981 143.229V145.182H367.026V143.229H374.981Z" fill="black"/>
    <path d="M54.1149 218V204.364H56.139V206.423H56.2811C56.5297 205.749 56.9795 205.201 57.6305 204.781C58.2815 204.361 59.0154 204.151 59.8322 204.151C59.9861 204.151 60.1784 204.154 60.4093 204.159C60.6401 204.165 60.8147 204.174 60.9331 204.186V206.317C60.862 206.299 60.6993 206.272 60.4448 206.237C60.1962 206.195 59.9328 206.175 59.6547 206.175C58.9918 206.175 58.3999 206.314 57.8791 206.592C57.3642 206.864 56.9558 207.243 56.6539 207.728C56.358 208.208 56.21 208.755 56.21 209.371V218H54.1149ZM68.5414 218.284C67.3103 218.284 66.2302 217.991 65.301 217.405C64.3777 216.819 63.6556 216 63.1348 214.946C62.6199 213.893 62.3624 212.661 62.3624 211.253C62.3624 209.832 62.6199 208.592 63.1348 207.533C63.6556 206.474 64.3777 205.651 65.301 205.065C66.2302 204.479 67.3103 204.186 68.5414 204.186C69.7724 204.186 70.8496 204.479 71.7729 205.065C72.7021 205.651 73.4242 206.474 73.9391 207.533C74.4599 208.592 74.7203 209.832 74.7203 211.253C74.7203 212.661 74.4599 213.893 73.9391 214.946C73.4242 216 72.7021 216.819 71.7729 217.405C70.8496 217.991 69.7724 218.284 68.5414 218.284ZM68.5414 216.402C69.4765 216.402 70.2459 216.162 70.8496 215.683C71.4533 215.203 71.9002 214.573 72.1902 213.792C72.4802 213.011 72.6252 212.164 72.6252 211.253C72.6252 210.341 72.4802 209.492 72.1902 208.705C71.9002 207.918 71.4533 207.281 70.8496 206.796C70.2459 206.311 69.4765 206.068 68.5414 206.068C67.6062 206.068 66.8368 206.311 66.2331 206.796C65.6294 207.281 65.1826 207.918 64.8926 208.705C64.6026 209.492 64.4576 210.341 64.4576 211.253C64.4576 212.164 64.6026 213.011 64.8926 213.792C65.1826 214.573 65.6294 215.203 66.2331 215.683C66.8368 216.162 67.6062 216.402 68.5414 216.402ZM83.4584 218.284C82.2273 218.284 81.1472 217.991 80.218 217.405C79.2947 216.819 78.5726 216 78.0518 214.946C77.5368 213.893 77.2794 212.661 77.2794 211.253C77.2794 209.832 77.5368 208.592 78.0518 207.533C78.5726 206.474 79.2947 205.651 80.218 205.065C81.1472 204.479 82.2273 204.186 83.4584 204.186C84.6894 204.186 85.7666 204.479 86.6899 205.065C87.6191 205.651 88.3412 206.474 88.8561 207.533C89.3769 208.592 89.6373 209.832 89.6373 211.253C89.6373 212.661 89.3769 213.893 88.8561 214.946C88.3412 216 87.6191 216.819 86.6899 217.405C85.7666 217.991 84.6894 218.284 83.4584 218.284ZM83.4584 216.402C84.3935 216.402 85.1629 216.162 85.7666 215.683C86.3703 215.203 86.8171 214.573 87.1072 213.792C87.3972 213.011 87.5422 212.164 87.5422 211.253C87.5422 210.341 87.3972 209.492 87.1072 208.705C86.8171 207.918 86.3703 207.281 85.7666 206.796C85.1629 206.311 84.3935 206.068 83.4584 206.068C82.5232 206.068 81.7538 206.311 81.1501 206.796C80.5464 207.281 80.0996 207.918 79.8096 208.705C79.5196 209.492 79.3746 210.341 79.3746 211.253C79.3746 212.164 79.5196 213.011 79.8096 213.792C80.0996 214.573 80.5464 215.203 81.1501 215.683C81.7538 216.162 82.5232 216.402 83.4584 216.402ZM98.766 204.364V206.139H91.6992V204.364H98.766ZM93.7589 201.097H95.854V214.094C95.854 214.686 95.9399 215.129 96.1115 215.425C96.2891 215.715 96.514 215.911 96.7862 216.011C97.0644 216.106 97.3574 216.153 97.6651 216.153C97.896 216.153 98.0853 216.142 98.2333 216.118C98.3813 216.088 98.4996 216.065 98.5884 216.047L99.0146 217.929C98.8725 217.982 98.6742 218.036 98.4197 218.089C98.1652 218.148 97.8427 218.178 97.4521 218.178C96.8602 218.178 96.2802 218.05 95.712 217.796C95.1497 217.541 94.6822 217.154 94.3093 216.633C93.9424 216.112 93.7589 215.455 93.7589 214.662V201.097Z" fill="black"/>
    <path d="M308 218H305.692L312.368 199.818H314.641L321.317 218H319.009L313.575 202.695H313.433L308 218ZM308.852 210.898H318.156V212.851H308.852V210.898Z" fill="black"/>
    <path d="M397.817 212.886V212.78C397.828 211.649 397.947 210.75 398.172 210.081C398.397 209.412 398.716 208.871 399.13 208.456C399.545 208.042 400.042 207.66 400.622 207.311C400.971 207.098 401.285 206.846 401.563 206.556C401.841 206.261 402.06 205.92 402.22 205.536C402.386 205.151 402.469 204.725 402.469 204.257C402.469 203.677 402.332 203.174 402.06 202.748C401.788 202.322 401.424 201.993 400.968 201.762C400.512 201.532 400.006 201.416 399.45 201.416C398.965 201.416 398.497 201.517 398.047 201.718C397.598 201.919 397.222 202.236 396.92 202.668C396.618 203.1 396.443 203.665 396.396 204.364H394.159C394.206 203.357 394.467 202.496 394.94 201.78C395.42 201.064 396.05 200.517 396.831 200.138C397.618 199.759 398.491 199.57 399.45 199.57C400.492 199.57 401.397 199.777 402.167 200.191C402.942 200.605 403.54 201.174 403.96 201.896C404.386 202.618 404.599 203.44 404.599 204.364C404.599 205.015 404.499 205.604 404.297 206.13C404.102 206.657 403.818 207.128 403.445 207.542C403.078 207.956 402.634 208.323 402.113 208.643C401.593 208.968 401.175 209.312 400.862 209.673C400.548 210.028 400.32 210.451 400.178 210.942C400.036 211.433 399.959 212.046 399.947 212.78V212.886H397.817ZM398.953 218.142C398.515 218.142 398.139 217.985 397.825 217.672C397.512 217.358 397.355 216.982 397.355 216.544C397.355 216.106 397.512 215.73 397.825 215.417C398.139 215.103 398.515 214.946 398.953 214.946C399.391 214.946 399.767 215.103 400.08 215.417C400.394 215.73 400.551 216.106 400.551 216.544C400.551 216.834 400.477 217.1 400.329 217.343C400.187 217.586 399.995 217.781 399.752 217.929C399.515 218.071 399.249 218.142 398.953 218.142Z" fill="black"/>
    <path d="M227.238 205.5H225.036C224.906 204.867 224.678 204.31 224.353 203.831C224.033 203.352 223.643 202.949 223.181 202.624C222.725 202.292 222.219 202.044 221.663 201.878C221.107 201.712 220.527 201.629 219.923 201.629C218.822 201.629 217.825 201.907 216.931 202.464C216.043 203.02 215.336 203.84 214.809 204.923C214.288 206.006 214.028 207.335 214.028 208.909C214.028 210.483 214.288 211.812 214.809 212.895C215.336 213.978 216.043 214.798 216.931 215.354C217.825 215.911 218.822 216.189 219.923 216.189C220.527 216.189 221.107 216.106 221.663 215.94C222.219 215.775 222.725 215.529 223.181 215.203C223.643 214.872 224.033 214.467 224.353 213.987C224.678 213.502 224.906 212.946 225.036 212.318H227.238C227.072 213.247 226.771 214.079 226.333 214.813C225.895 215.547 225.35 216.171 224.699 216.686C224.048 217.195 223.317 217.583 222.506 217.849C221.701 218.115 220.84 218.249 219.923 218.249C218.372 218.249 216.993 217.87 215.786 217.112C214.578 216.355 213.628 215.277 212.936 213.881C212.243 212.484 211.897 210.827 211.897 208.909C211.897 206.991 212.243 205.334 212.936 203.938C213.628 202.541 214.578 201.464 215.786 200.706C216.993 199.948 218.372 199.57 219.923 199.57C220.84 199.57 221.701 199.703 222.506 199.969C223.317 200.235 224.048 200.626 224.699 201.141C225.35 201.65 225.895 202.271 226.333 203.005C226.771 203.733 227.072 204.565 227.238 205.5Z" fill="black"/>
    <path d="M161.841 205.5C161.646 204.902 161.388 204.367 161.069 203.893C160.755 203.414 160.379 203.005 159.941 202.668C159.509 202.331 159.018 202.073 158.468 201.896C157.917 201.718 157.313 201.629 156.656 201.629C155.579 201.629 154.6 201.907 153.718 202.464C152.836 203.02 152.135 203.84 151.614 204.923C151.093 206.006 150.833 207.335 150.833 208.909C150.833 210.483 151.096 211.812 151.623 212.895C152.149 213.978 152.863 214.798 153.762 215.354C154.662 215.911 155.674 216.189 156.799 216.189C157.84 216.189 158.758 215.967 159.551 215.523C160.35 215.073 160.971 214.44 161.415 213.623C161.865 212.801 162.09 211.833 162.09 210.72L162.764 210.862H157.296V208.909H164.22V210.862C164.22 212.36 163.901 213.662 163.262 214.768C162.628 215.875 161.752 216.733 160.634 217.343C159.521 217.947 158.243 218.249 156.799 218.249C155.189 218.249 153.774 217.87 152.555 217.112C151.342 216.355 150.395 215.277 149.714 213.881C149.039 212.484 148.702 210.827 148.702 208.909C148.702 207.471 148.894 206.178 149.279 205.029C149.67 203.875 150.22 202.893 150.93 202.082C151.64 201.271 152.481 200.65 153.452 200.218C154.422 199.786 155.491 199.57 156.656 199.57C157.615 199.57 158.509 199.715 159.338 200.005C160.172 200.289 160.915 200.694 161.566 201.221C162.223 201.742 162.77 202.366 163.208 203.094C163.646 203.816 163.948 204.618 164.114 205.5H161.841Z" fill="black"/>
    <path d="M408.061 133.818V152H405.966V133.818H408.061ZM417.438 152.284C416.207 152.284 415.127 151.991 414.198 151.405C413.275 150.819 412.553 150 412.032 148.946C411.517 147.893 411.259 146.661 411.259 145.253C411.259 143.832 411.517 142.592 412.032 141.533C412.553 140.474 413.275 139.651 414.198 139.065C415.127 138.479 416.207 138.186 417.438 138.186C418.669 138.186 419.747 138.479 420.67 139.065C421.599 139.651 422.321 140.474 422.836 141.533C423.357 142.592 423.617 143.832 423.617 145.253C423.617 146.661 423.357 147.893 422.836 148.946C422.321 150 421.599 150.819 420.67 151.405C419.747 151.991 418.669 152.284 417.438 152.284ZM417.438 150.402C418.373 150.402 419.143 150.162 419.747 149.683C420.35 149.203 420.797 148.573 421.087 147.792C421.377 147.011 421.522 146.164 421.522 145.253C421.522 144.341 421.377 143.492 421.087 142.705C420.797 141.918 420.35 141.281 419.747 140.796C419.143 140.311 418.373 140.068 417.438 140.068C416.503 140.068 415.734 140.311 415.13 140.796C414.526 141.281 414.08 141.918 413.79 142.705C413.5 143.492 413.355 144.341 413.355 145.253C413.355 146.164 413.5 147.011 413.79 147.792C414.08 148.573 414.526 149.203 415.13 149.683C415.734 150.162 416.503 150.402 417.438 150.402ZM435.409 146.425V138.364H437.504V152H435.409V149.692H435.267C434.948 150.384 434.451 150.973 433.776 151.458C433.101 151.938 432.249 152.178 431.219 152.178C430.367 152.178 429.609 151.991 428.946 151.618C428.283 151.239 427.763 150.671 427.384 149.914C427.005 149.15 426.816 148.188 426.816 147.028V138.364H428.911V146.886C428.911 147.881 429.189 148.674 429.745 149.266C430.308 149.857 431.024 150.153 431.894 150.153C432.415 150.153 432.944 150.02 433.483 149.754C434.027 149.488 434.483 149.079 434.85 148.529C435.223 147.978 435.409 147.277 435.409 146.425ZM446.491 152.284C445.355 152.284 444.352 151.997 443.481 151.423C442.611 150.843 441.931 150.026 441.44 148.973C440.948 147.913 440.703 146.661 440.703 145.217C440.703 143.785 440.948 142.542 441.44 141.489C441.931 140.435 442.614 139.621 443.49 139.047C444.366 138.473 445.378 138.186 446.527 138.186C447.414 138.186 448.116 138.334 448.631 138.63C449.151 138.92 449.548 139.251 449.82 139.624C450.098 139.991 450.314 140.293 450.468 140.53H450.646V133.818H452.741V152H450.717V149.905H450.468C450.314 150.153 450.095 150.467 449.811 150.846C449.527 151.219 449.122 151.553 448.595 151.849C448.068 152.139 447.367 152.284 446.491 152.284ZM446.775 150.402C447.616 150.402 448.326 150.183 448.906 149.745C449.486 149.301 449.927 148.689 450.229 147.907C450.53 147.12 450.681 146.212 450.681 145.182C450.681 144.164 450.533 143.273 450.238 142.51C449.942 141.74 449.504 141.142 448.924 140.716C448.344 140.284 447.627 140.068 446.775 140.068C445.887 140.068 445.148 140.296 444.556 140.752C443.97 141.202 443.529 141.814 443.233 142.589C442.943 143.359 442.798 144.223 442.798 145.182C442.798 146.152 442.946 147.034 443.242 147.827C443.544 148.615 443.988 149.242 444.573 149.71C445.165 150.171 445.899 150.402 446.775 150.402Z" fill="black"/>
  </svg>
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

<VClicks class="px-3 text-lg space-y-2">

* Evaluationstypen
  * 1. Auswertung einzelner Zeitleisten einzelner Filme
  * 2. Auswertung mehrerer Zeitleisten des gleichen Films
  * 3. Auswertung mehrerer Filme repräsentiert durch je eine Zeitleiste pro Film
  * 4. Allgemeine Auswertung der enthaltenen Daten in FMADB

</VClicks>

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
  <svg class="h-37" viewBox="-1 -1 937 217" fill="none" xmlns="http://www.w3.org/2000/svg">
    <rect x="741" y="1" width="193" height="214" stroke="#5D8392" stroke-width="2"/>
    <path d="M781.286 107.909C781.286 109.827 780.94 111.484 780.248 112.881C779.555 114.277 778.605 115.355 777.398 116.112C776.19 116.87 774.811 117.249 773.261 117.249C771.71 117.249 770.331 116.87 769.124 116.112C767.916 115.355 766.966 114.277 766.274 112.881C765.581 111.484 765.235 109.827 765.235 107.909C765.235 105.991 765.581 104.334 766.274 102.938C766.966 101.541 767.916 100.464 769.124 99.706C770.331 98.9484 771.71 98.5696 773.261 98.5696C774.811 98.5696 776.19 98.9484 777.398 99.706C778.605 100.464 779.555 101.541 780.248 102.938C780.94 104.334 781.286 105.991 781.286 107.909ZM779.156 107.909C779.156 106.335 778.892 105.006 778.366 103.923C777.845 102.84 777.137 102.02 776.244 101.464C775.356 100.907 774.362 100.629 773.261 100.629C772.16 100.629 771.163 100.907 770.269 101.464C769.381 102.02 768.674 102.84 768.147 103.923C767.626 105.006 767.366 106.335 767.366 107.909C767.366 109.483 767.626 110.812 768.147 111.895C768.674 112.978 769.381 113.798 770.269 114.354C771.163 114.911 772.16 115.189 773.261 115.189C774.362 115.189 775.356 114.911 776.244 114.354C777.137 113.798 777.845 112.978 778.366 111.895C778.892 110.812 779.156 109.483 779.156 107.909ZM787.19 98.8182V117H784.988V98.8182H787.19ZM797.215 117H791.605V98.8182H797.464C799.228 98.8182 800.737 99.1822 801.992 99.9102C803.246 100.632 804.208 101.671 804.877 103.026C805.546 104.376 805.88 105.991 805.88 107.874C805.88 109.768 805.543 111.398 804.868 112.765C804.193 114.127 803.211 115.174 801.921 115.908C800.63 116.636 799.062 117 797.215 117ZM793.806 115.047H797.073C798.577 115.047 799.823 114.757 800.811 114.177C801.799 113.597 802.536 112.771 803.022 111.7C803.507 110.629 803.749 109.353 803.749 107.874C803.749 106.406 803.51 105.142 803.03 104.083C802.551 103.017 801.835 102.201 800.882 101.632C799.929 101.058 798.742 100.771 797.322 100.771H793.806V115.047ZM824.204 104.5H822.002C821.872 103.867 821.644 103.31 821.319 102.831C820.999 102.352 820.609 101.949 820.147 101.624C819.691 101.292 819.185 101.044 818.629 100.878C818.072 100.712 817.492 100.629 816.889 100.629C815.788 100.629 814.791 100.907 813.897 101.464C813.009 102.02 812.302 102.84 811.775 103.923C811.254 105.006 810.994 106.335 810.994 107.909C810.994 109.483 811.254 110.812 811.775 111.895C812.302 112.978 813.009 113.798 813.897 114.354C814.791 114.911 815.788 115.189 816.889 115.189C817.492 115.189 818.072 115.106 818.629 114.94C819.185 114.775 819.691 114.529 820.147 114.203C820.609 113.872 820.999 113.467 821.319 112.987C821.644 112.502 821.872 111.946 822.002 111.318H824.204C824.038 112.247 823.736 113.079 823.298 113.813C822.861 114.547 822.316 115.171 821.665 115.686C821.014 116.195 820.283 116.583 819.472 116.849C818.667 117.115 817.806 117.249 816.889 117.249C815.338 117.249 813.959 116.87 812.752 116.112C811.544 115.355 810.594 114.277 809.902 112.881C809.209 111.484 808.863 109.827 808.863 107.909C808.863 105.991 809.209 104.334 809.902 102.938C810.594 101.541 811.544 100.464 812.752 99.706C813.959 98.9484 815.338 98.5696 816.889 98.5696C817.806 98.5696 818.667 98.7028 819.472 98.9691C820.283 99.2354 821.014 99.6261 821.665 100.141C822.316 100.65 822.861 101.271 823.298 102.005C823.736 102.733 824.038 103.565 824.204 104.5ZM844.736 103.364C844.63 102.464 844.198 101.766 843.44 101.268C842.683 100.771 841.753 100.523 840.652 100.523C839.848 100.523 839.143 100.653 838.54 100.913C837.942 101.174 837.474 101.532 837.137 101.988C836.805 102.443 836.64 102.961 836.64 103.541C836.64 104.027 836.755 104.444 836.986 104.793C837.223 105.136 837.524 105.423 837.891 105.654C838.258 105.879 838.643 106.065 839.046 106.213C839.448 106.355 839.818 106.471 840.155 106.56L842.002 107.057C842.475 107.181 843.002 107.353 843.582 107.572C844.168 107.791 844.727 108.09 845.26 108.468C845.799 108.841 846.243 109.321 846.592 109.907C846.941 110.493 847.116 111.212 847.116 112.064C847.116 113.046 846.858 113.934 846.343 114.727C845.834 115.52 845.088 116.151 844.106 116.618C843.129 117.086 841.943 117.32 840.546 117.32C839.244 117.32 838.116 117.109 837.163 116.689C836.216 116.269 835.471 115.683 834.926 114.931C834.388 114.18 834.083 113.307 834.012 112.312H836.285C836.344 112.999 836.575 113.567 836.977 114.017C837.385 114.461 837.9 114.792 838.522 115.011C839.149 115.224 839.824 115.331 840.546 115.331C841.386 115.331 842.141 115.195 842.81 114.923C843.479 114.644 844.008 114.26 844.399 113.768C844.79 113.271 844.985 112.691 844.985 112.028C844.985 111.425 844.816 110.933 844.479 110.555C844.141 110.176 843.698 109.868 843.147 109.631C842.597 109.395 842.002 109.187 841.363 109.01L839.125 108.371C837.705 107.962 836.58 107.379 835.752 106.622C834.923 105.864 834.509 104.873 834.509 103.648C834.509 102.63 834.784 101.742 835.335 100.984C835.891 100.221 836.637 99.629 837.572 99.2088C838.513 98.7827 839.563 98.5696 840.723 98.5696C841.895 98.5696 842.937 98.7797 843.848 99.1999C844.76 99.6142 845.482 100.182 846.015 100.904C846.553 101.627 846.837 102.446 846.867 103.364H844.736ZM856.169 117.284C854.855 117.284 853.721 116.994 852.768 116.414C851.822 115.828 851.091 115.011 850.576 113.964C850.067 112.91 849.812 111.685 849.812 110.288C849.812 108.892 850.067 107.661 850.576 106.595C851.091 105.524 851.807 104.689 852.724 104.092C853.647 103.488 854.725 103.186 855.956 103.186C856.666 103.186 857.367 103.304 858.06 103.541C858.752 103.778 859.382 104.163 859.951 104.695C860.519 105.222 860.972 105.92 861.309 106.79C861.646 107.661 861.815 108.732 861.815 110.004V110.892H851.304V109.081H859.684C859.684 108.312 859.53 107.625 859.223 107.021C858.921 106.418 858.489 105.941 857.927 105.592C857.37 105.243 856.713 105.068 855.956 105.068C855.121 105.068 854.399 105.275 853.789 105.69C853.186 106.098 852.721 106.631 852.396 107.288C852.07 107.945 851.907 108.649 851.907 109.401V110.608C851.907 111.638 852.085 112.511 852.44 113.227C852.801 113.937 853.301 114.479 853.94 114.852C854.58 115.219 855.322 115.402 856.169 115.402C856.719 115.402 857.216 115.325 857.66 115.171C858.11 115.011 858.498 114.775 858.823 114.461C859.149 114.141 859.4 113.745 859.578 113.271L861.602 113.839C861.389 114.526 861.031 115.13 860.528 115.651C860.025 116.165 859.403 116.568 858.663 116.858C857.924 117.142 857.092 117.284 856.169 117.284ZM865.002 117V103.364H867.026V105.423H867.168C867.417 104.749 867.867 104.201 868.518 103.781C869.169 103.361 869.903 103.151 870.719 103.151C870.873 103.151 871.066 103.154 871.297 103.159C871.527 103.165 871.702 103.174 871.82 103.186V105.317C871.749 105.299 871.587 105.272 871.332 105.237C871.083 105.195 870.82 105.175 870.542 105.175C869.879 105.175 869.287 105.314 868.766 105.592C868.251 105.864 867.843 106.243 867.541 106.728C867.245 107.208 867.097 107.755 867.097 108.371V117H865.002ZM885.87 103.364L880.827 117H878.696L873.654 103.364H875.926L879.691 114.23H879.833L883.597 103.364H885.87ZM893.864 117.284C892.55 117.284 891.417 116.994 890.464 116.414C889.517 115.828 888.786 115.011 888.271 113.964C887.762 112.91 887.507 111.685 887.507 110.288C887.507 108.892 887.762 107.661 888.271 106.595C888.786 105.524 889.502 104.689 890.419 104.092C891.343 103.488 892.42 103.186 893.651 103.186C894.361 103.186 895.063 103.304 895.755 103.541C896.447 103.778 897.078 104.163 897.646 104.695C898.214 105.222 898.667 105.92 899.004 106.79C899.342 107.661 899.51 108.732 899.51 110.004V110.892H888.999V109.081H897.38C897.38 108.312 897.226 107.625 896.918 107.021C896.616 106.418 896.184 105.941 895.622 105.592C895.065 105.243 894.409 105.068 893.651 105.068C892.816 105.068 892.094 105.275 891.485 105.69C890.881 106.098 890.416 106.631 890.091 107.288C889.765 107.945 889.603 108.649 889.603 109.401V110.608C889.603 111.638 889.78 112.511 890.135 113.227C890.496 113.937 890.996 114.479 891.636 114.852C892.275 115.219 893.018 115.402 893.864 115.402C894.414 115.402 894.912 115.325 895.355 115.171C895.805 115.011 896.193 114.775 896.518 114.461C896.844 114.141 897.096 113.745 897.273 113.271L899.297 113.839C899.084 114.526 898.726 115.13 898.223 115.651C897.72 116.165 897.099 116.568 896.359 116.858C895.619 117.142 894.787 117.284 893.864 117.284ZM902.697 117V103.364H904.722V105.423H904.864C905.112 104.749 905.562 104.201 906.213 103.781C906.864 103.361 907.598 103.151 908.415 103.151C908.569 103.151 908.761 103.154 908.992 103.159C909.223 103.165 909.397 103.174 909.516 103.186V105.317C909.445 105.299 909.282 105.272 909.027 105.237C908.779 105.195 908.515 105.175 908.237 105.175C907.574 105.175 906.982 105.314 906.462 105.592C905.947 105.864 905.538 106.243 905.237 106.728C904.941 107.208 904.793 107.755 904.793 108.371V117H902.697Z" fill="#5D8392"/>
    <rect x="371" y="143" width="193" height="72" stroke="#5D8392" stroke-width="2"/>
    <path d="M418.676 189V170.818H425.033C426.299 170.818 427.344 171.037 428.167 171.475C428.989 171.907 429.602 172.49 430.004 173.224C430.407 173.952 430.608 174.76 430.608 175.648C430.608 176.429 430.469 177.074 430.191 177.583C429.919 178.092 429.558 178.495 429.108 178.79C428.664 179.086 428.182 179.305 427.661 179.447V179.625C428.217 179.661 428.776 179.856 429.339 180.211C429.901 180.566 430.371 181.075 430.75 181.738C431.129 182.401 431.318 183.212 431.318 184.17C431.318 185.082 431.111 185.902 430.697 186.63C430.283 187.358 429.629 187.935 428.735 188.361C427.841 188.787 426.678 189 425.246 189H418.676ZM420.878 187.047H425.246C426.684 187.047 427.705 186.769 428.309 186.212C428.918 185.65 429.223 184.969 429.223 184.17C429.223 183.555 429.066 182.987 428.753 182.466C428.439 181.939 427.992 181.519 427.412 181.205C426.832 180.886 426.146 180.726 425.352 180.726H420.878V187.047ZM420.878 178.808H424.962C425.625 178.808 426.222 178.678 426.755 178.418C427.294 178.157 427.72 177.79 428.034 177.317C428.353 176.843 428.513 176.287 428.513 175.648C428.513 174.849 428.235 174.171 427.678 173.615C427.122 173.052 426.24 172.771 425.033 172.771H420.878V178.808ZM438.665 189.32C437.801 189.32 437.016 189.157 436.312 188.831C435.608 188.5 435.049 188.023 434.634 187.402C434.22 186.775 434.013 186.017 434.013 185.129C434.013 184.348 434.167 183.715 434.474 183.229C434.782 182.738 435.194 182.353 435.708 182.075C436.223 181.797 436.792 181.59 437.413 181.454C438.04 181.312 438.671 181.199 439.304 181.116C440.133 181.01 440.804 180.93 441.319 180.877C441.84 180.818 442.219 180.72 442.456 180.584C442.698 180.448 442.82 180.211 442.82 179.874V179.803C442.82 178.927 442.58 178.246 442.1 177.761C441.627 177.275 440.908 177.033 439.943 177.033C438.943 177.033 438.159 177.252 437.591 177.69C437.022 178.128 436.623 178.595 436.392 179.092L434.403 178.382C434.759 177.554 435.232 176.908 435.824 176.447C436.422 175.979 437.073 175.654 437.777 175.47C438.487 175.281 439.186 175.186 439.872 175.186C440.31 175.186 440.813 175.239 441.381 175.346C441.955 175.446 442.509 175.657 443.042 175.976C443.58 176.296 444.027 176.778 444.382 177.423C444.737 178.068 444.915 178.933 444.915 180.016V189H442.82V187.153H442.713C442.571 187.449 442.334 187.766 442.003 188.103C441.671 188.441 441.23 188.728 440.68 188.964C440.13 189.201 439.458 189.32 438.665 189.32ZM438.984 187.438C439.813 187.438 440.511 187.275 441.08 186.949C441.654 186.624 442.086 186.203 442.376 185.689C442.672 185.174 442.82 184.632 442.82 184.064V182.146C442.731 182.253 442.536 182.35 442.234 182.439C441.938 182.522 441.594 182.596 441.204 182.661C440.819 182.72 440.443 182.774 440.076 182.821C439.715 182.862 439.422 182.898 439.197 182.928C438.653 182.999 438.144 183.114 437.67 183.274C437.203 183.428 436.824 183.661 436.534 183.975C436.25 184.283 436.108 184.703 436.108 185.236C436.108 185.964 436.377 186.514 436.916 186.887C437.46 187.254 438.15 187.438 438.984 187.438ZM454.279 189.284C453 189.284 451.899 188.982 450.976 188.379C450.053 187.775 449.343 186.943 448.845 185.884C448.348 184.824 448.1 183.614 448.1 182.253C448.1 180.868 448.354 179.646 448.863 178.586C449.378 177.521 450.094 176.689 451.012 176.092C451.935 175.488 453.012 175.186 454.243 175.186C455.202 175.186 456.066 175.364 456.835 175.719C457.605 176.074 458.235 176.571 458.726 177.21C459.218 177.849 459.523 178.595 459.641 179.447H457.546C457.386 178.826 457.031 178.276 456.48 177.796C455.936 177.311 455.202 177.068 454.279 177.068C453.462 177.068 452.746 177.281 452.13 177.707C451.521 178.128 451.044 178.722 450.701 179.492C450.364 180.255 450.195 181.152 450.195 182.182C450.195 183.235 450.361 184.153 450.692 184.934C451.029 185.715 451.503 186.322 452.112 186.754C452.728 187.186 453.45 187.402 454.279 187.402C454.823 187.402 455.317 187.307 455.761 187.118C456.205 186.929 456.581 186.656 456.889 186.301C457.197 185.946 457.416 185.52 457.546 185.023H459.641C459.523 185.828 459.23 186.553 458.762 187.198C458.3 187.837 457.688 188.346 456.924 188.725C456.167 189.098 455.285 189.284 454.279 189.284ZM464.657 184.028L464.621 181.436H465.047L471.013 175.364H473.606L467.249 181.791H467.072L464.657 184.028ZM462.704 189V170.818H464.799V189H462.704ZM471.369 189L466.042 182.253L467.533 180.797L474.032 189H471.369ZM481.458 189.284C480.144 189.284 479.011 188.994 478.058 188.414C477.111 187.828 476.38 187.011 475.865 185.964C475.356 184.91 475.102 183.685 475.102 182.288C475.102 180.892 475.356 179.661 475.865 178.595C476.38 177.524 477.096 176.689 478.014 176.092C478.937 175.488 480.014 175.186 481.245 175.186C481.955 175.186 482.657 175.304 483.349 175.541C484.042 175.778 484.672 176.163 485.24 176.695C485.808 177.222 486.261 177.92 486.598 178.79C486.936 179.661 487.104 180.732 487.104 182.004V182.892H476.593V181.081H484.974C484.974 180.312 484.82 179.625 484.512 179.021C484.21 178.418 483.778 177.941 483.216 177.592C482.66 177.243 482.003 177.068 481.245 177.068C480.411 177.068 479.689 177.275 479.079 177.69C478.475 178.098 478.011 178.631 477.685 179.288C477.36 179.945 477.197 180.649 477.197 181.401V182.608C477.197 183.638 477.374 184.511 477.729 185.227C478.091 185.937 478.591 186.479 479.23 186.852C479.869 187.219 480.612 187.402 481.458 187.402C482.009 187.402 482.506 187.325 482.95 187.171C483.399 187.011 483.787 186.775 484.113 186.461C484.438 186.141 484.69 185.745 484.867 185.271L486.891 185.839C486.678 186.526 486.32 187.13 485.817 187.651C485.314 188.165 484.693 188.568 483.953 188.858C483.213 189.142 482.381 189.284 481.458 189.284ZM492.387 180.797V189H490.292V175.364H492.316V177.494H492.493C492.813 176.802 493.298 176.246 493.949 175.825C494.6 175.399 495.441 175.186 496.471 175.186C497.394 175.186 498.202 175.375 498.894 175.754C499.587 176.127 500.125 176.695 500.51 177.459C500.895 178.216 501.087 179.175 501.087 180.335V189H498.992V180.477C498.992 179.406 498.714 178.571 498.157 177.974C497.601 177.37 496.838 177.068 495.867 177.068C495.198 177.068 494.6 177.213 494.074 177.503C493.553 177.793 493.141 178.216 492.84 178.773C492.538 179.329 492.387 180.004 492.387 180.797ZM510.065 189.284C508.928 189.284 507.925 188.997 507.055 188.423C506.185 187.843 505.505 187.026 505.013 185.973C504.522 184.913 504.276 183.661 504.276 182.217C504.276 180.785 504.522 179.542 505.013 178.489C505.505 177.435 506.188 176.621 507.064 176.047C507.94 175.473 508.952 175.186 510.1 175.186C510.988 175.186 511.689 175.334 512.204 175.63C512.725 175.92 513.122 176.251 513.394 176.624C513.672 176.991 513.888 177.293 514.042 177.53H514.22V170.818H516.315V189H514.291V186.905H514.042C513.888 187.153 513.669 187.467 513.385 187.846C513.101 188.219 512.696 188.553 512.169 188.849C511.642 189.139 510.941 189.284 510.065 189.284ZM510.349 187.402C511.189 187.402 511.9 187.183 512.48 186.745C513.06 186.301 513.501 185.689 513.802 184.907C514.104 184.12 514.255 183.212 514.255 182.182C514.255 181.164 514.107 180.273 513.811 179.51C513.515 178.74 513.077 178.142 512.497 177.716C511.917 177.284 511.201 177.068 510.349 177.068C509.461 177.068 508.721 177.296 508.129 177.752C507.544 178.202 507.103 178.814 506.807 179.589C506.517 180.359 506.372 181.223 506.372 182.182C506.372 183.152 506.52 184.034 506.816 184.827C507.117 185.615 507.561 186.242 508.147 186.71C508.739 187.171 509.473 187.402 510.349 187.402Z" fill="#5D8392"/>
    <rect x="1" y="91" width="193" height="124" stroke="#5D8392" stroke-width="2"/>
    <path d="M46.4058 162V143.818H57.3078V145.771H48.6075V151.915H56.491V153.868H48.6075V162H46.4058ZM60.6481 162V148.364H62.6722V150.423H62.8143C63.0629 149.749 63.5127 149.201 64.1637 148.781C64.8148 148.361 65.5487 148.151 66.3654 148.151C66.5193 148.151 66.7117 148.154 66.9425 148.159C67.1733 148.165 67.3479 148.174 67.4663 148.186V150.317C67.3952 150.299 67.2325 150.272 66.978 150.237C66.7294 150.195 66.466 150.175 66.1879 150.175C65.525 150.175 64.9331 150.314 64.4123 150.592C63.8974 150.864 63.489 151.243 63.1872 151.728C62.8912 152.208 62.7433 152.755 62.7433 153.371V162H60.6481ZM75.0746 162.284C73.8435 162.284 72.7634 161.991 71.8342 161.405C70.9109 160.819 70.1888 160 69.668 158.946C69.1531 157.893 68.8956 156.661 68.8956 155.253C68.8956 153.832 69.1531 152.592 69.668 151.533C70.1888 150.474 70.9109 149.651 71.8342 149.065C72.7634 148.479 73.8435 148.186 75.0746 148.186C76.3056 148.186 77.3828 148.479 78.3061 149.065C79.2353 149.651 79.9574 150.474 80.4723 151.533C80.9931 152.592 81.2536 153.832 81.2536 155.253C81.2536 156.661 80.9931 157.893 80.4723 158.946C79.9574 160 79.2353 160.819 78.3061 161.405C77.3828 161.991 76.3056 162.284 75.0746 162.284ZM75.0746 160.402C76.0097 160.402 76.7791 160.162 77.3828 159.683C77.9865 159.203 78.4334 158.573 78.7234 157.792C79.0134 157.011 79.1584 156.164 79.1584 155.253C79.1584 154.341 79.0134 153.492 78.7234 152.705C78.4334 151.918 77.9865 151.281 77.3828 150.796C76.7791 150.311 76.0097 150.068 75.0746 150.068C74.1394 150.068 73.37 150.311 72.7663 150.796C72.1626 151.281 71.7158 151.918 71.4258 152.705C71.1358 153.492 70.9908 154.341 70.9908 155.253C70.9908 156.164 71.1358 157.011 71.4258 157.792C71.7158 158.573 72.1626 159.203 72.7663 159.683C73.37 160.162 74.1394 160.402 75.0746 160.402ZM86.547 153.797V162H84.4518V148.364H86.4759V150.494H86.6535C86.9731 149.802 87.4584 149.246 88.1095 148.825C88.7605 148.399 89.6009 148.186 90.6308 148.186C91.5541 148.186 92.362 148.375 93.0544 148.754C93.7469 149.127 94.2855 149.695 94.6702 150.459C95.0549 151.216 95.2473 152.175 95.2473 153.335V162H93.1521V153.477C93.1521 152.406 92.8739 151.571 92.3176 150.974C91.7612 150.37 90.9977 150.068 90.0271 150.068C89.3583 150.068 88.7605 150.213 88.2338 150.503C87.7129 150.793 87.3016 151.216 86.9997 151.773C86.6979 152.329 86.547 153.004 86.547 153.797ZM105.006 148.364V150.139H97.9395V148.364H105.006ZM99.9991 145.097H102.094V158.094C102.094 158.686 102.18 159.129 102.352 159.425C102.529 159.715 102.754 159.911 103.026 160.011C103.305 160.106 103.598 160.153 103.905 160.153C104.136 160.153 104.326 160.142 104.474 160.118C104.622 160.088 104.74 160.065 104.829 160.047L105.255 161.929C105.113 161.982 104.914 162.036 104.66 162.089C104.405 162.148 104.083 162.178 103.692 162.178C103.1 162.178 102.52 162.05 101.952 161.796C101.39 161.541 100.922 161.154 100.55 160.633C100.183 160.112 99.9991 159.455 99.9991 158.662V145.097ZM113.729 162.284C112.415 162.284 111.281 161.994 110.328 161.414C109.382 160.828 108.651 160.011 108.136 158.964C107.627 157.91 107.372 156.685 107.372 155.288C107.372 153.892 107.627 152.661 108.136 151.595C108.651 150.524 109.367 149.689 110.284 149.092C111.207 148.488 112.285 148.186 113.516 148.186C114.226 148.186 114.927 148.304 115.62 148.541C116.312 148.778 116.942 149.163 117.511 149.695C118.079 150.222 118.532 150.92 118.869 151.79C119.206 152.661 119.375 153.732 119.375 155.004V155.892H108.864V154.081H117.244C117.244 153.312 117.09 152.625 116.783 152.021C116.481 151.418 116.049 150.941 115.487 150.592C114.93 150.243 114.273 150.068 113.516 150.068C112.681 150.068 111.959 150.275 111.349 150.69C110.746 151.098 110.281 151.631 109.956 152.288C109.63 152.945 109.467 153.649 109.467 154.401V155.608C109.467 156.638 109.645 157.511 110 158.227C110.361 158.937 110.861 159.479 111.5 159.852C112.14 160.219 112.882 160.402 113.729 160.402C114.279 160.402 114.776 160.325 115.22 160.171C115.67 160.011 116.058 159.775 116.383 159.461C116.709 159.141 116.96 158.745 117.138 158.271L119.162 158.839C118.949 159.526 118.591 160.13 118.088 160.651C117.585 161.165 116.963 161.568 116.223 161.858C115.484 162.142 114.652 162.284 113.729 162.284ZM124.657 153.797V162H122.562V148.364H124.586V150.494H124.764C125.083 149.802 125.569 149.246 126.22 148.825C126.871 148.399 127.711 148.186 128.741 148.186C129.664 148.186 130.472 148.375 131.165 148.754C131.857 149.127 132.396 149.695 132.781 150.459C133.165 151.216 133.358 152.175 133.358 153.335V162H131.262V153.477C131.262 152.406 130.984 151.571 130.428 150.974C129.872 150.37 129.108 150.068 128.137 150.068C127.469 150.068 126.871 150.213 126.344 150.503C125.823 150.793 125.412 151.216 125.11 151.773C124.808 152.329 124.657 153.004 124.657 153.797ZM142.335 162.284C141.199 162.284 140.196 161.997 139.326 161.423C138.456 160.843 137.775 160.026 137.284 158.973C136.793 157.913 136.547 156.661 136.547 155.217C136.547 153.785 136.793 152.542 137.284 151.489C137.775 150.435 138.459 149.621 139.335 149.047C140.211 148.473 141.223 148.186 142.371 148.186C143.259 148.186 143.96 148.334 144.475 148.63C144.996 148.92 145.392 149.251 145.665 149.624C145.943 149.991 146.159 150.293 146.313 150.53H146.49V143.818H148.585V162H146.561V159.905H146.313C146.159 160.153 145.94 160.467 145.656 160.846C145.372 161.219 144.966 161.553 144.439 161.849C143.913 162.139 143.211 162.284 142.335 162.284ZM142.619 160.402C143.46 160.402 144.17 160.183 144.75 159.745C145.33 159.301 145.771 158.689 146.073 157.907C146.375 157.12 146.526 156.212 146.526 155.182C146.526 154.164 146.378 153.273 146.082 152.51C145.786 151.74 145.348 151.142 144.768 150.716C144.188 150.284 143.472 150.068 142.619 150.068C141.732 150.068 140.992 150.296 140.4 150.752C139.814 151.202 139.373 151.814 139.077 152.589C138.787 153.359 138.642 154.223 138.642 155.182C138.642 156.152 138.79 157.034 139.086 157.827C139.388 158.615 139.832 159.242 140.418 159.71C141.01 160.171 141.743 160.402 142.619 160.402Z" fill="#5D8392"/>
    <path d="M207.293 111.293C206.902 111.683 206.902 112.317 207.293 112.707L213.657 119.071C214.047 119.462 214.681 119.462 215.071 119.071C215.462 118.681 215.462 118.047 215.071 117.657L209.414 112L215.071 106.343C215.462 105.953 215.462 105.319 215.071 104.929C214.681 104.538 214.047 104.538 213.657 104.929L207.293 111.293ZM727 111L208 111V113L727 113V111Z" fill="#5D8392"/>
    <path d="M356.707 181.707C357.098 181.317 357.098 180.683 356.707 180.293L350.343 173.929C349.953 173.538 349.319 173.538 348.929 173.929C348.538 174.319 348.538 174.953 348.929 175.343L354.586 181L348.929 186.657C348.538 187.047 348.538 187.681 348.929 188.071C349.319 188.462 349.953 188.462 350.343 188.071L356.707 181.707ZM207.293 180.293C206.902 180.683 206.902 181.317 207.293 181.707L213.657 188.071C214.047 188.462 214.681 188.462 215.071 188.071C215.462 187.681 215.462 187.047 215.071 186.657L209.414 181L215.071 175.343C215.462 174.953 215.462 174.319 215.071 173.929C214.681 173.538 214.047 173.538 213.657 173.929L207.293 180.293ZM356 180L208 180V182L356 182V180Z" fill="#5D8392"/>
    <path d="M727.707 181.707C728.098 181.317 728.098 180.683 727.707 180.293L721.343 173.929C720.953 173.538 720.319 173.538 719.929 173.929C719.538 174.319 719.538 174.953 719.929 175.343L725.586 181L719.929 186.657C719.538 187.047 719.538 187.681 719.929 188.071C720.319 188.462 720.953 188.462 721.343 188.071L727.707 181.707ZM578.293 180.293C577.902 180.683 577.902 181.317 578.293 181.707L584.657 188.071C585.047 188.462 585.681 188.462 586.071 188.071C586.462 187.681 586.462 187.047 586.071 186.657L580.414 181L586.071 175.343C586.462 174.953 586.462 174.319 586.071 173.929C585.681 173.538 585.047 173.538 584.657 173.929L578.293 180.293ZM727 180L579 180V182L727 182V180Z" fill="#5D8392"/>
    <rect x="1" y="1" width="193" height="72" stroke="#5D8392" stroke-width="2"/>
    <path d="M14.9932 46H9.38237V27.8182H15.2417C17.0055 27.8182 18.5147 28.1822 19.7694 28.9102C21.0242 29.6322 21.9859 30.6709 22.6547 32.0263C23.3235 33.3757 23.6579 34.9915 23.6579 36.8736C23.6579 38.7675 23.3206 40.3981 22.6459 41.7653C21.9711 43.1265 20.9887 44.1741 19.6984 44.908C18.4082 45.636 16.8398 46 14.9932 46ZM11.5841 44.0469H14.8511C16.3544 44.0469 17.6003 43.7569 18.5887 43.1768C19.5771 42.5968 20.314 41.7712 20.7993 40.6999C21.2846 39.6287 21.5273 38.3532 21.5273 36.8736C21.5273 35.4058 21.2876 34.1422 20.8081 33.0827C20.3287 32.0174 19.6126 31.2006 18.6597 30.6325C17.7068 30.0584 16.5202 29.7713 15.0997 29.7713H11.5841V44.0469ZM32.6068 46.2841C31.3757 46.2841 30.2956 45.9911 29.3664 45.4052C28.4431 44.8192 27.721 43.9995 27.2002 42.946C26.6853 41.8925 26.4278 40.6615 26.4278 39.2528C26.4278 37.8324 26.6853 36.5924 27.2002 35.533C27.721 34.4736 28.4431 33.6509 29.3664 33.065C30.2956 32.479 31.3757 32.1861 32.6068 32.1861C33.8379 32.1861 34.915 32.479 35.8383 33.065C36.7675 33.6509 37.4896 34.4736 38.0045 35.533C38.5254 36.5924 38.7858 37.8324 38.7858 39.2528C38.7858 40.6615 38.5254 41.8925 38.0045 42.946C37.4896 43.9995 36.7675 44.8192 35.8383 45.4052C34.915 45.9911 33.8379 46.2841 32.6068 46.2841ZM32.6068 44.402C33.5419 44.402 34.3113 44.1623 34.915 43.6829C35.5187 43.2035 35.9656 42.5732 36.2556 41.7919C36.5456 41.0107 36.6906 40.1643 36.6906 39.2528C36.6906 38.3414 36.5456 37.4921 36.2556 36.7049C35.9656 35.9177 35.5187 35.2815 34.915 34.7962C34.3113 34.3108 33.5419 34.0682 32.6068 34.0682C31.6717 34.0682 30.9023 34.3108 30.2986 34.7962C29.6949 35.2815 29.248 35.9177 28.958 36.7049C28.668 37.4921 28.523 38.3414 28.523 39.2528C28.523 40.1643 28.668 41.0107 28.958 41.7919C29.248 42.5732 29.6949 43.2035 30.2986 43.6829C30.9023 44.1623 31.6717 44.402 32.6068 44.402ZM43.9371 41.0284L43.9016 38.4361H44.3278L50.2937 32.3636H52.886L46.5295 38.7912H46.3519L43.9371 41.0284ZM41.984 46V27.8182H44.0792V46H41.984ZM50.6488 46L45.3221 39.2528L46.8136 37.7969L53.3121 46H50.6488ZM64.1764 40.4247V32.3636H66.2716V46H64.1764V43.6918H64.0344C63.7148 44.3842 63.2176 44.9731 62.5429 45.4585C61.8682 45.9379 61.0159 46.1776 59.9861 46.1776C59.1338 46.1776 58.3762 45.9911 57.7133 45.6183C57.0505 45.2395 56.5296 44.6713 56.1508 43.9137C55.772 43.1502 55.5827 42.1884 55.5827 41.0284V32.3636H57.6778V40.8864C57.6778 41.8807 57.956 42.6738 58.5123 43.2656C59.0746 43.8575 59.7907 44.1534 60.6608 44.1534C61.1816 44.1534 61.7113 44.0202 62.2499 43.7539C62.7944 43.4876 63.2501 43.0792 63.6171 42.5288C63.99 41.9783 64.1764 41.277 64.1764 40.4247ZM70.109 46V32.3636H72.1332V34.4943H72.3107C72.5948 33.7663 73.0535 33.2011 73.6868 32.7987C74.3201 32.3903 75.0806 32.1861 75.9684 32.1861C76.868 32.1861 77.6167 32.3903 78.2145 32.7987C78.8182 33.2011 79.2887 33.7663 79.6261 34.4943H79.7681C80.1173 33.79 80.6411 33.2307 81.3395 32.8164C82.0379 32.3962 82.8754 32.1861 83.8519 32.1861C85.0711 32.1861 86.0684 32.5678 86.8438 33.3313C87.6191 34.0889 88.0067 35.2696 88.0067 36.8736V46H85.9116V36.8736C85.9116 35.8674 85.6364 35.1483 85.0859 34.7163C84.5355 34.2842 83.8874 34.0682 83.1417 34.0682C82.1829 34.0682 81.4401 34.3582 80.9134 34.9382C80.3866 35.5123 80.1232 36.2403 80.1232 37.1222V46H77.9925V36.6605C77.9925 35.8852 77.741 35.2608 77.2379 34.7873C76.7348 34.3079 76.0868 34.0682 75.2937 34.0682C74.7492 34.0682 74.2402 34.2132 73.7667 34.5032C73.2991 34.7932 72.9203 35.1957 72.6303 35.7106C72.3462 36.2196 72.2042 36.8085 72.2042 37.4773V46H70.109ZM97.5549 46.2841C96.2409 46.2841 95.1075 45.9941 94.1547 45.4141C93.2077 44.8281 92.4767 44.0114 91.9618 42.9638C91.4528 41.9103 91.1983 40.6851 91.1983 39.2884C91.1983 37.8916 91.4528 36.6605 91.9618 35.5952C92.4767 34.5239 93.1929 33.6894 94.1103 33.0916C95.0336 32.4879 96.1107 32.1861 97.3418 32.1861C98.052 32.1861 98.7534 32.3045 99.4458 32.5412C100.138 32.7779 100.769 33.1626 101.337 33.6953C101.905 34.2221 102.358 34.9205 102.695 35.7905C103.032 36.6605 103.201 37.7318 103.201 39.0043V39.892H92.6898V38.081H101.07C101.07 37.3116 100.917 36.625 100.609 36.0213C100.307 35.4176 99.8749 34.9412 99.3127 34.592C98.7563 34.2428 98.0994 34.0682 97.3418 34.0682C96.5073 34.0682 95.7852 34.2753 95.1756 34.6896C94.5719 35.098 94.1073 35.6307 93.7818 36.2876C93.4563 36.9446 93.2935 37.6489 93.2935 38.4006V39.608C93.2935 40.6378 93.4711 41.5108 93.8262 42.2269C94.1872 42.9371 94.6873 43.4787 95.3265 43.8516C95.9657 44.2185 96.7085 44.402 97.5549 44.402C98.1053 44.402 98.6025 44.325 99.0463 44.1712C99.4962 44.0114 99.8838 43.7746 100.209 43.4609C100.535 43.1413 100.786 42.7448 100.964 42.2713L102.988 42.8395C102.775 43.526 102.417 44.1297 101.914 44.6506C101.411 45.1655 100.789 45.5679 100.05 45.858C99.3097 46.142 98.4782 46.2841 97.5549 46.2841ZM108.483 37.7969V46H106.388V32.3636H108.412V34.4943H108.59C108.91 33.8018 109.395 33.2455 110.046 32.8253C110.697 32.3991 111.537 32.1861 112.567 32.1861C113.491 32.1861 114.298 32.3755 114.991 32.7543C115.683 33.1271 116.222 33.6953 116.607 34.4588C116.991 35.2164 117.184 36.1752 117.184 37.3352V46H115.089V37.4773C115.089 36.406 114.81 35.5715 114.254 34.9737C113.698 34.37 112.934 34.0682 111.964 34.0682C111.295 34.0682 110.697 34.2132 110.17 34.5032C109.649 34.7932 109.238 35.2164 108.936 35.7727C108.634 36.3291 108.483 37.0038 108.483 37.7969ZM126.943 32.3636V34.1392H119.876V32.3636H126.943ZM121.936 29.0966H124.031V42.0938C124.031 42.6856 124.117 43.1295 124.288 43.4254C124.466 43.7154 124.691 43.9107 124.963 44.0114C125.241 44.1061 125.534 44.1534 125.842 44.1534C126.073 44.1534 126.262 44.1416 126.41 44.1179C126.558 44.0883 126.676 44.0646 126.765 44.0469L127.191 45.929C127.049 45.9822 126.851 46.0355 126.597 46.0888C126.342 46.148 126.019 46.1776 125.629 46.1776C125.037 46.1776 124.457 46.0503 123.889 45.7958C123.326 45.5413 122.859 45.1536 122.486 44.6328C122.119 44.112 121.936 43.455 121.936 42.6619V29.0966ZM134.107 46.3196C133.243 46.3196 132.459 46.1568 131.755 45.8313C131.05 45.4999 130.491 45.0234 130.077 44.402C129.662 43.7746 129.455 43.017 129.455 42.1293C129.455 41.348 129.609 40.7147 129.917 40.2294C130.225 39.7382 130.636 39.3535 131.151 39.0753C131.666 38.7971 132.234 38.59 132.855 38.4538C133.483 38.3118 134.113 38.1993 134.746 38.1165C135.575 38.0099 136.247 37.93 136.762 37.8768C137.282 37.8176 137.661 37.7199 137.898 37.5838C138.141 37.4477 138.262 37.2109 138.262 36.8736V36.8026C138.262 35.9266 138.022 35.246 137.543 34.7607C137.069 34.2753 136.35 34.0327 135.386 34.0327C134.385 34.0327 133.601 34.2517 133.033 34.6896C132.465 35.1276 132.065 35.5952 131.834 36.0923L129.846 35.3821C130.201 34.5535 130.674 33.9084 131.266 33.4467C131.864 32.9792 132.515 32.6536 133.219 32.4702C133.93 32.2808 134.628 32.1861 135.315 32.1861C135.753 32.1861 136.256 32.2393 136.824 32.3459C137.398 32.4465 137.951 32.6566 138.484 32.9762C139.023 33.2958 139.469 33.7782 139.824 34.4233C140.18 35.0684 140.357 35.9325 140.357 37.0156V46H138.262V44.1534H138.155C138.013 44.4493 137.777 44.766 137.445 45.1033C137.114 45.4407 136.673 45.7277 136.122 45.9645C135.572 46.2012 134.9 46.3196 134.107 46.3196ZM134.427 44.4375C135.255 44.4375 135.954 44.2747 136.522 43.9492C137.096 43.6237 137.528 43.2035 137.818 42.6886C138.114 42.1737 138.262 41.6321 138.262 41.0639V39.1463C138.173 39.2528 137.978 39.3505 137.676 39.4393C137.38 39.5221 137.037 39.5961 136.646 39.6612C136.262 39.7204 135.886 39.7737 135.519 39.821C135.158 39.8625 134.865 39.898 134.64 39.9276C134.095 39.9986 133.586 40.114 133.113 40.2738C132.645 40.4277 132.266 40.6615 131.976 40.9751C131.692 41.2829 131.55 41.7031 131.55 42.2358C131.55 42.9638 131.82 43.5142 132.358 43.8871C132.903 44.254 133.592 44.4375 134.427 44.4375ZM150.112 32.3636V34.1392H143.045V32.3636H150.112ZM145.105 29.0966H147.2V42.0938C147.2 42.6856 147.286 43.1295 147.457 43.4254C147.635 43.7154 147.86 43.9107 148.132 44.0114C148.41 44.1061 148.703 44.1534 149.011 44.1534C149.242 44.1534 149.431 44.1416 149.579 44.1179C149.727 44.0883 149.845 44.0646 149.934 44.0469L150.36 45.929C150.218 45.9822 150.02 46.0355 149.765 46.0888C149.511 46.148 149.188 46.1776 148.798 46.1776C148.206 46.1776 147.626 46.0503 147.058 45.7958C146.495 45.5413 146.028 45.1536 145.655 44.6328C145.288 44.112 145.105 43.455 145.105 42.6619V29.0966ZM153.263 46V32.3636H155.358V46H153.263ZM154.329 30.0909C153.92 30.0909 153.568 29.9518 153.272 29.6737C152.982 29.3955 152.837 29.0611 152.837 28.6705C152.837 28.2798 152.982 27.9454 153.272 27.6673C153.568 27.3891 153.92 27.25 154.329 27.25C154.737 27.25 155.086 27.3891 155.376 27.6673C155.672 27.9454 155.82 28.2798 155.82 28.6705C155.82 29.0611 155.672 29.3955 155.376 29.6737C155.086 29.9518 154.737 30.0909 154.329 30.0909ZM164.736 46.2841C163.505 46.2841 162.425 45.9911 161.495 45.4052C160.572 44.8192 159.85 43.9995 159.329 42.946C158.814 41.8925 158.557 40.6615 158.557 39.2528C158.557 37.8324 158.814 36.5924 159.329 35.533C159.85 34.4736 160.572 33.6509 161.495 33.065C162.425 32.479 163.505 32.1861 164.736 32.1861C165.967 32.1861 167.044 32.479 167.967 33.065C168.896 33.6509 169.619 34.4736 170.133 35.533C170.654 36.5924 170.915 37.8324 170.915 39.2528C170.915 40.6615 170.654 41.8925 170.133 42.946C169.619 43.9995 168.896 44.8192 167.967 45.4052C167.044 45.9911 165.967 46.2841 164.736 46.2841ZM164.736 44.402C165.671 44.402 166.44 44.1623 167.044 43.6829C167.648 43.2035 168.094 42.5732 168.384 41.7919C168.675 41.0107 168.82 40.1643 168.82 39.2528C168.82 38.3414 168.675 37.4921 168.384 36.7049C168.094 35.9177 167.648 35.2815 167.044 34.7962C166.44 34.3108 165.671 34.0682 164.736 34.0682C163.801 34.0682 163.031 34.3108 162.427 34.7962C161.824 35.2815 161.377 35.9177 161.087 36.7049C160.797 37.4921 160.652 38.3414 160.652 39.2528C160.652 40.1643 160.797 41.0107 161.087 41.7919C161.377 42.5732 161.824 43.2035 162.427 43.6829C163.031 44.1623 163.801 44.402 164.736 44.402ZM176.208 37.7969V46H174.113V32.3636H176.137V34.4943H176.315C176.634 33.8018 177.12 33.2455 177.771 32.8253C178.422 32.3991 179.262 32.1861 180.292 32.1861C181.215 32.1861 182.023 32.3755 182.716 32.7543C183.408 33.1271 183.947 33.6953 184.331 34.4588C184.716 35.2164 184.908 36.1752 184.908 37.3352V46H182.813V37.4773C182.813 36.406 182.535 35.5715 181.979 34.9737C181.422 34.37 180.659 34.0682 179.688 34.0682C179.019 34.0682 178.422 34.2132 177.895 34.5032C177.374 34.7932 176.963 35.2164 176.661 35.7727C176.359 36.3291 176.208 37.0038 176.208 37.7969Z" fill="#5D8392"/>
  </svg>
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
