---
theme: ./theme
layout: default
themeConfig:
  primary: '#3b82f6'
  showTotalPageCount: false
  showPageProcessBar: true
  literatureSlideNumber: -1
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

<AppReferenceToWrittenWork :pages="['3.2.']" v-click />

<AppIntroLogoFullscreen />

<!--
<div class="text-2xl text-red-600">in 00:00 - out 01:00</div>

* Begrüßung zu MA Verteidigung -> zahlreich erschienen
* 30 min Vortrag
  * Übersicht meiner Arbeit und der Ergebnisse
  * Zeit knapp, die rund 120 Seiten komplett vorzustellen
  * Fragen bitte notieren und am Ende stellen.
  * Gäste, die nicht vom Fach sind, sind heute hier
* 30 min Fragen & Diskussion
  * Tiefergehende Informationen bei Interesse
* Oben rechts Flagge für Kapitelreferenz auf schriftliche Arbeit -> wie hier, da der Name `FMADB` diesem Kapitel entstammt
-->

---
layout: two-cols
---

<h1>Über mich</h1>

<div class="flex flex-col justify-center items-center mt-20">
  <img class="w-50 rounded-full"
      src="/assets/persons/Thorsten-Seyschab.jpg"
  />
  <h2 class="mt-4">Thorsten Seyschab</h2>
</div>

::right::

<VClicks class="space-y-2 text-xl h-full mt-28">

* <mdi-school-outline class="baseColor mr-2" /> Technische Universität Dresden
* <mdi-desktop-classic class="baseColor mr-2" /> Informatiker aus Deutschland<br>
  <span class="text-sm ml-10">Spezialisiert in Web Technologien & Datenbanken</span>
* <mdi-web class="baseColor mr-2" /> [https://todde.tv/](https://todde.tv/)
  * <mdi-github class="baseColor mr-2" /> [toddeTV](https://github.com/toddeTV)
  * <mdi-gitlab class="baseColor mr-2" /> [toddeTV](https://gitlab.com/toddeTV)
* <mdi-email class="baseColor mr-2" /> [business@todde.tv](business@todde.tv)

</VClicks>

<!-- * <mdi-console class="baseColor mr-2" /> Full Stack Web Developer -->

<!--
<div class="text-2xl text-red-600">in 01:00 - out 02:00</div>

* offenkundig Student der TUD im MA Studium, welches ich voraussichtlich heute abschließen werden, da dies meine
  letzte Prüfungsleistung ist
* im Bachelor auf Datenbanken spezialisiert -> BA Arbeit
* später dann die Liebe zur Webentwicklung entdeckt -> MA Arbeit
* Im Bachelor beruflich orientiert
* Doch worum geht es in meiner Arbeit?
-->

---
clicks: 3
---

<AppReferenceToWrittenWork :pages="['1.1.', '1.2.']" />

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

<div class="absolute right-60 top-25 flex flex-col justify-center items-center" v-click="1">
  <img class="w-35 rounded-full"
      src="/assets/persons/Susanne-Hardt.jpg"
  />
  <span class="mt-2 text-xl">Susanne Hardt</span>
</div>

<div v-click="3" class="text-2xl text-center mt-8 baseColor">
  <mdi-arrow-right class="mr-2 pt-1" />
  <span>Geht das nicht ohne die Informatik?</span>
  <mdi-arrow-left class="ml-2 pt-1" />
</div>

<!--
<div class="text-2xl text-red-600">in 02:00 - out 03:00</div>

* "Modell" ist falsch, eigentlich "Filmmusikalische Topologien"
* Ohne Informatiker: Gibt es schon vergleichbares, an dem man sich orientieren kann?
-->

---

<AppReferenceToWrittenWork :pages="['1.1.', '2.3.', '2.4.']" />

# Warum gibt es solch große Korpusstudien noch nicht?

<VClicks class="space-y-12 text-xl pt-15">

* <mdi-image-size-select-small class="baseColor mr-2" /> Umfang
  <span class="text-sm ml-10">Dateneingabe und Auswertung vereinfachen</span>
* <mdi-select-compare class="baseColor mr-2" /> Vergleichbarkeit
  <span class="text-sm ml-10">einheitliche Struktur bereitstellen</span>
  
</VClicks>

<div v-click class="text-2xl text-center mt-20 text-gray-400">
  <mdi-arrow-right class="mr-2 pt-1" />
  <span class="line-through">Geht das nicht ohne die Informatik?</span>
  <mdi-arrow-left class="ml-2 pt-1" />
</div>

<div v-after class="text-2xl text-center mt-1 baseColor">
  <mdi-arrow-right class="mr-2 pt-1" />
  <span>Wir brauchen die Informatik als Lösung!</span>
  <mdi-arrow-left class="ml-2 pt-1" />
</div>

<!--
<div class="text-2xl text-red-600">in 03:00 - out 04:00</div>

* <span class="text-red-500">Keine vollständigen Filmübergreifende wissenschaftliche Arbeiten</span>
  * Betrachtung einzelner Filmcharaktere in kontextlosen und abstrakten Bewegbilder
    * Bethold Hoeckner lässt Filmdramaturgie komplett weg
  * Einzelfilmanalysen
    * Annabel Cohen zu dem Film "The red Violin"
  * Filmübergreifende eingeschänkte Analysen
    * Pascal Rudolph nur zu ausgewählten Musikeinsätzen in 12 Filmen (Buch "Präexistente Musik im Film" 2022)
  * Filmübergreifende vollständige Analysen
    * NOPE
* <span class="text-red-500">Keine existierenden Softwarelösungen:</span>
  * Analyse Audiodatei vs Musiknoten
  * existierende Datenbanken: Metainfos & Musikkataloge
* nur vereinzelte filmübergreifende Studien, da sehr komplex und umfangreich
* Möglichkeit der Vereinheitlichung der Analysen filmübergreifend, da Film sehr individuell
  * Pascal Rudolph "Präexistente Musik im Film" 2022 [?] sagt schon in seiner Einleitung, dass er ueberall anders
    vorgehen musste
* von anderen kann man nicht nutzen, da nichts Einheitliches
-->

---

<AppReferenceToWrittenWork :pages="['3.1.', '4.2.1.', '4.2.2.']" />

# Das Ergebnis: FMADB

<div v-click class="mt-15 text-xl">

* Webservice in Englisch unter: <a href="https://fmadb.org/" target="_blank">https://fmadb.org/</a>

</div>

<div v-click class="mt-2 text-xl">

* Interdisziplinäre Zusammenarbeit mit unterschiedlichen Instituten unterschiedlicher Länder

</div>

<div class="w-full flex flex-row justify-center mt-2" v-after>
  <div>
    <img class="h-20 p-4"
         src="/assets/attribution_logos/TU-Dresden.svg"
    />
  </div>
  <div>
    <img class="h-20 p-4 mx-10"
         src="/assets/attribution_logos/HfmDD.png"
    />
  </div>
  <div>
    <img class="h-20 p-4"
         src="/assets/attribution_logos/epfl.svg"
    />
  </div>
</div>

<div v-click class="mt-2 text-xl">

* Software vorgestellt auf Kongressen
  * Jahreskongress der Gesellschaft für Musiktheorie (2022-09-30 bis 2022-10-02 in Salzburg)
  * Symposium "Musiktheorie und audiovisuelle Medien - musiktheoretische und pädagogische Perspektiven"
    (2022-10-28 bis 2022-10-29 in Dresden)

</div>

<!--
<div class="text-2xl text-red-600">in 04:00 - out 05:00</div>

* Hfm vertreten durch Susanne
* TU-Dresden vertreten durch mich
* Epfl in der Schweiz als Expertenfeedback
* und und und
-->

---
clicks: 5
---

# Probleme & Lösungen

<div class="relative">

<AppAnalysisPipeline :animation="5" />

<div class="absolute bg-white w-35 h-full top-0 left-30" v-click-hide></div>
<div class="absolute bg-white w-30 h-full top-0 left-65" v-click-hide></div>
<div class="absolute bg-white w-37 h-full top-0 left-95" v-click-hide></div>
<div class="absolute bg-white w-39 h-full top-0 left-132" v-click-hide></div>

</div>

<!--
<div class="text-2xl text-red-600">in 05:00 - out 06:00</div>

* Am Anfang stehen viele Filme ...
* ... am Ende wollen wir Erkenntnisse aus den Filmmusiken dieser haben
* Erkenntnisse vergleichbar mit anderen, nicht nur für sich selbst.
-->

---

<AppReferenceToWrittenWork :pages="['3.5.', '3.6.1.', '4.5.6.']" />

# Probleme & Lösungen

<AppAnalysisPipeline />

<AppArrowUp :nbr="1" />

<div class="px-3 flex flex-row relative">

<div class="w-45 mr-10 flex-shrink-0">
  <img src="/assets/movie-covers/tmdb-120.jpg" />
  <div class="text-right text-xs">
    &copy; themoviedb.org
  </div>
</div>

<VClicks class="text-lg pt-9">

* Unterschiedliche Namen & Erscheinungsjahre
  * [ger] Der Herr der Ringe - Die Gefährten
  * [eng] The Lord of the Rings: The Fellowship of the Ring
* Unterschiedliche Längen zwischen und innerhalb Länder
  * Kinofassung: 171 Minuten
  * Extended Edition: 218 Minuten
* Medium (Konvertierung & Kompression)
  * DVD, Netflix, Amazon Prime, ...

</VClicks>

<div class="w-full flex flex-row text-lg absolute left-56.5" v-click>
  <mdi-check class="text-green-500 mr-2" />
  Filme mit Metainformationen automatisch von
  <img src="/assets/TMDB_Asset3.svg" class="h-2.5 mx-2 mt-2.5" />
  crawlen
</div>

<div class="w-full text-lg absolute left-63.5 top-18 bg-white h-18" v-click>
<mdi-check class="text-green-500" /> nur englische Titel durch crawlen nutzen<br>
<mdi-check class="text-green-500" /> nur amerikanisches Erscheinungsjahr
</div>

<div class="w-full text-lg absolute left-63.5 top-42.5 bg-white h-18" v-click>
<mdi-check class="text-green-500" /> individuell vermerkbare Filmlänge durch Nutzer
</div>

<div class="w-full text-lg absolute left-63.5 top-67 bg-white" v-click>
<mdi-check class="text-green-500" /> individuell vermerkbar durch Nutzer
</div>

</div>

<!--
<div class="text-2xl text-red-600">in 06:00 - out 08:00</div>
-->

---

<AppReferenceToWrittenWork :pages="['3.6.2.', '3.7.']" />

# Probleme & Lösungen

<AppAnalysisPipeline />

<AppArrowUp :nbr="2" />

<div class="px-3 text-lg relative">

<VClicks>

* viele <mdi-exclamation-thick class="text-red-500" />
  * BPM, Time Signature, Dynamic, Scale, Effect, Cluster, Function, ...
* Parameter sind verschieden und facettenreich
  * z.B. BPM nicht nur reine Zahlen (Accelerando, Unbekannt, ...)
* unterschiedliche Herangehensweisen für gleiche Parameter
  * Hansjörg Pauli definiert 3 Funktionen von Filmmusik
  * Norbert Jürgen Schneider definiert 20 Funktionen von Filmmusik
* unterschiedliche Bezeichnungen für gleiche Parameter
  * Diegetische Musik == Inzidenzmusik == Source-Musik

</VClicks>

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

<div class="w-full absolute top-25 left-8 bg-white" v-click>
<mdi-check class="text-green-500" /> Sonderfälle durch individuelle Lösungen abdecken
</div>

<div class="w-full absolute top-42 left-8 bg-white h-18" v-click>
<mdi-check class="text-green-500" /> festlegen und User ggf Freiraum ermöglichen
</div>

<div class="w-full absolute top-67 left-8 bg-white" v-click>
<mdi-check class="text-green-500" /> festlegen und User ggf Terminologieänderungen ermöglichen
</div>

</div>

<!--
<div class="text-2xl text-red-600">in 08:00 - out 10:00</div>

* viele Parameter, welche nehme ich, welche bringen mir etwas?
* Musiktheoretischer Parameter
  * aufgrund Umfang hierauf konzentriert
-->

---
clicks: 6
---

<AppReferenceToWrittenWork :pages="['2.2.', '2.4.']" />

# Probleme & Lösungen

<AppAnalysisPipeline />

<AppArrowUp :nbr="3" />

<div class="px-3 text-lg relative">

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

<div class="absolute flex flex-row left-111 top-1.5 z-10" v-click="6">
  <div class="border border-green-500 rounded-lg w-30 h-10 mr-2">
  </div>
  <mdi-check class="text-green-500 text-xl mt-1.5" />
</div>

</div>

<!--
<div class="text-2xl text-red-600">in 10:00 - out 11:00</div>

* separat veröffentlichte Soundtracks weichen von Filmen ab
* Doch wie visualisieren während der Analysen und der Eingaben der Daten?
* Rechtliche Probleme!
-->

---
clicks: 8
---

<AppReferenceToWrittenWork :pages="['3.3.', '3.4.']" />

# Probleme & Lösungen

<AppAnalysisPipeline />

<AppArrowUp :nbr="4" />

<table class="-mt-4 -mb-5">
  <thead class="!font-bold">
    <tr>
      <td class="w-1/2 border-r-1">
        <div v-click="1">
          Tabellarisch
        </div>
        <div class="text-gray-400 font-normal" v-click="1">
          mit Varianten:
        </div>
      </td>
      <td class="align-top">
        <div v-click="5">
          Zeitleiste (= Timeline)
        </div>
        <div class="text-gray-400 font-normal" v-click="6">
          mit Zeitleistenelementtypen:
        </div>
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
             class="mt-1 animImg1" v-click="3" />
      </td>
      <td>
      </td>
    </tr>
  </tbody>
</table>

<AppBiggerPresentationTables />

<div class="absolute top-59 left-130" v-click="7">
  <div class="mb-3">1. Ein Wert, sequentiell (z.B. BPM, dynamic, root)</div>
  <div class="mb-3">2. Mehrere Werte, sequentiell (als Typ 3 darstellbar)</div>
  <div class="mb-3">3. Ein Wert, parallel (z.B. Orchestration)</div>
  <div class="mb-3">4. Mehrere Werte, parallel (als Typ 3 darstellbar)</div>
</div>

<!-- <div class="flex flex-row">
  <mdi-check class="text-green-500" />
  <span class="font-bold mx-1.5">Timeline</span>
  als Visualisierung mit Eingabehilfe
</div> -->

<div class="absolute top-90 left-135" v-click="6">
  <img src="/assets/miniTimeline.svg" class="w-95" />
</div>

<div class="absolute flex flex-row left-125 top-42 z-10" v-click="8">
  <div class="border border-green-500 rounded-lg w-65 h-12.5 mr-2">
  </div>
  <mdi-check class="text-green-500 text-xl mt-1.5" />
</div>

<!--
<div class="text-2xl text-red-600">in 11:00 - out 14:00</div>

* Ein Parameter hat Startzeit, Endzeit und Wert
* Tabellen schlecht
  * Doppelte Einträge bei gleichbleibenden Werten
  * Pausen nicht gut erkennbar
* <span class="text-red-500 font-bold text-lg">semantische Zusammenhänge: Dirty/Clean Logik</span>
-->

---

<AppReferenceToWrittenWork :pages="['3.8.', '4.13.']" />

# Das Problem

<AppAnalysisPipeline />

<AppArrowUp :nbr="5" />

<VClicks class="px-3 text-lg space-y-2">

* Schön wären Diagramme
* Tabellen oder Diagramme miteinander vergleichen

</VClicks>

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

<!--
<div class="text-2xl text-red-600">in 14:00 - out 15:00</div>

* Wort `Auswertung` hier etwas irreführend, da nun zweierlei gemeint ist:
  * leichte Eingabe mit Visualisierung
  * Evaluation als Erkenntnissgewinn nach Dateneingabe
-->

---

# Probleme & Lösungen

<AppAnalysisPipeline />

<AppArrowUp :nbr="6" />

<div class="space-y-2 text-xl px-3">

* Anderen zeigen und sich freuen

</div>

<div class="space-y-2 text-xl pl-10 pt-3" v-click>
  <mdi-check class="text-green-500" /> Umfangreichere Korpusstudien möglich 🤩
</div>

<!--
<div class="text-2xl text-red-600">in 15:00 - out 15:00</div>
-->

---

<AppReferenceToWrittenWork :pages="['4.']" />

# Ecosystem

<div class="w-full flex flex-row justify-center mt-30">
  <img src="/assets/EcosystemCommunication.svg" class="h-42" />
</div>

<!--
<div class="text-2xl text-red-600">in 15:00 - out 16:00</div>
-->

---

<AppReferenceToWrittenWork :pages="['4.']" />

# Polyrepo

<div class="relative -mt-5">
  <div class="flex flex-row justify-between absolute">
    <div class="py-1 px-4 w-73 flex-shrink-0" v-click>
      <div>
        <mdi-github class="mr-2" />
        <a href="https://github.com/toddeTV/FMADB_backend" target="_blank">toddeTV/FMADB_backend</a>
      </div>
      <div class="pl-7.5 mt-3">
        <div class="flex flex-col space-y-3">
          <div>
            <LogosTypescriptIcon class="mr-2" /> TypeScript
          </div>
          <div>
            <LogosYarn class="mr-2" /> Yarn3
          </div>
          <div>
            <mdi-github class="mr-2" /> GitHub Actions (CI/CD)
          </div>
          <div>
            <mdi-docker class="mr-2" style="color: #2497ED;" /> Docker
          </div>
          <div>
            <LogosNestjs class="mr-2" /> NestJS
          </div>
          <div>
            <logos-eslint class="mr-2" /> ESLint
          </div>
          <div>
            <VscodeIconsFileTypeGraphql class="mr-2" /> GraphQL
          </div>
          <div>
            <LogosPrisma class="mr-2" /> Prisma
          </div>
          <div>
            <LogosPostgresql class="mr-2" /> PostgreSQL
          </div>
          <div>
            <VscodeIconsFileTypeRest class="mr-2" /> REST
          </div>
        </div>
      </div>
    </div>
    <div class="py-1 px-4 w-73 flex-shrink-0" v-after>
      <div>
        <mdi-github class="mr-2" />
        <a href="https://github.com/toddeTV/FMADB_frontend" target="_blank">toddeTV/FMADB_frontend</a>
      </div>
      <div class="pl-7.5 mt-3">
        <div class="flex flex-col space-y-3">
          <div>
            <LogosTypescriptIcon class="mr-2" /> TypeScript
          </div>
          <div>
            <LogosYarn class="mr-2" /> Yarn3
          </div>
          <div>
            <mdi-github class="mr-2" /> GitHub Actions (CI/CD)
          </div>
          <div>
            <mdi-docker class="mr-2" style="color: #2497ED;" /> Docker
          </div>
          <div>
            <LogosVue class="mr-2" /> Vue3
          </div>
          <div>
            <logos-eslint class="mr-2" /> ESLint
          </div>
          <div>
            <file-icons-graphql-codegenerator class="mr-2" /> graphql-codegen
          </div>
          <div>
            <LogosApollostack class="mr-2" /> Apollo
          </div>
          <div>
            <LogosVueuse class="mr-2" /> VueUse
          </div>
          <div>
            <VscodeIconsFileTypeLightQuasar class="mr-2" /> Quasar
          </div>
          <div>
            <material-symbols-music-note-rounded class="mr-2" /> Verovio
          </div>
          <div>
            <simple-icons-apacheecharts class="mr-2" style="color: #E43961;" /> Apache ECharts
          </div>
          <div>
            <logos-tailwindcss-icon class="mr-2" /> TailwindCSS
          </div>
          <div>
            <logos-headlessui-icon class="mr-2" /> HeadlessUI
          </div>
          <!-- <div>
            <VscodeIconsFileTypeLightQuasar class="mr-2" /> date-fns
          </div> -->
        </div>
      </div>
    </div>
    <div class="py-1 px-4 w-83 flex-shrink-0" v-after>
      <div>
        <mdi-github class="mr-2" />
        <a href="https://github.com/toddeTV/FMADB_documentation" target="_blank">toddeTV/FMADB_documentation</a>
      </div>
      <div class="pl-7.5 mt-3">
        <div class="flex flex-col space-y-3">
          <div>
            <LogosTypescriptIcon class="mr-2" /> TypeScript
          </div>
          <div>
            <LogosYarn class="mr-2" /> Yarn3
          </div>
          <div>
            <mdi-github class="mr-2" /> GitHub Actions (CI/CD)
          </div>
          <div>
            <mdi-docker class="mr-2" style="color: #2497ED;" /> Docker
          </div>
          <div>
            <LogosVue class="mr-2" /> Vue3
          </div>
          <div>
            <LogosVitejs class="mr-2" /> VitePress
          </div>
        </div>
      </div>
    </div>
  </div>

  <div v-click class="w-full h-33 bg-red-600/10 border-2 border-red-600 rounded-lg absolute top-7.5"></div>

  <div v-click class="w-72 h-8 bg-green-600/10 border-2 border-green-600 rounded-lg absolute top-41"></div>
  <div v-after class="w-155.5 h-8 bg-green-600/10 border-2 border-green-600 rounded-lg absolute top-41 left-72.5"></div>

  <div v-click class="w-145 h-8 bg-blue-600/10 border-2 border-blue-600 rounded-lg absolute top-49.5"></div>
  
  <div v-click class="w-73 h-8 bg-yellow-600/10 border-l-2 border-y-2 border-yellow-600 rounded-l-lg absolute top-58"></div>
  <div v-after class="w-72 h-16 bg-yellow-600/10 border-r-2 border-y-2 border-yellow-600 rounded-r-lg absolute top-58 left-73"></div>
  <div v-after class="w-72 h-8 border-l-2 border-yellow-600 rounded-r-lg absolute top-65.5 left-73"></div>

  <div v-click class="w-72.5 h-16 bg-fuchsia-600/10 border-2 border-fuchsia-600 rounded-lg absolute top-66.5"></div>
</div>

<!--
<div class="text-2xl text-red-600">in 16:00 - out 18:00</div>

* Polyrepo einfacher für schnelleres Deployment
* Monorepo einfacher für Versionen untereinander
-->

---

# Demo Video

Wenn hier kein Video zu sehen ist, unterstützt der Browser keine Videoeinbindungen.

Bitte in diesem Fall einen anderen Browser nutzen.

<video controls class="absolute bottom-0 left-0 z-100">
  <source src="/assets/demo-videos/main.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

<!--
<div class="text-2xl text-red-600">in 18:00 - out 23:00</div>
-->

---
clicks: 7
---

<AppReferenceToWrittenWork :pages="['3.6.', '4.5.4.']" />

# Datenmodell

<AppDatamodel />

<!-- <img src="/assets/memes/what.jpg" class="absolute w-50 top-45 left-95" /> -->
<!-- <img src="/assets/memes/sense-now.jpg" class="absolute w-55 top-17 left-135" /> -->

<!--
<div class="text-2xl text-red-600">in 23:00 - out 25:00</div>

1. What?
2. Gruppen
3. Metadatenmodell:
   * User
   * Movie
   * Genre
   * Timeline
4. Timelineelemente haben alle die gleichen Grundvariablen
   * z.B. Timelineelement: Bpm -> Werte in sich
5. Timelineelement: Dynamic -> mit Enums
6. gesamt -> verstanden, macht Sinn & gut strukturiert
-->

---

<AppReferenceToWrittenWork :pages="['3.7.', '4.5.2.', '4.5.3.', '4.6.3.', '4.12.']" />

# Besondere Hürden

<VClicks class="space-y-2 text-xl">

* Konzeptionell schwierig:
  * Umfang des Datenmodells bewältigen
  * Parameter `Orchestration`: Detailgrad
* Programierung schwierig:
  * Prisma in NestJS als Code-First-Approach mit automatischen Datenbankmigrationen
  * Prisma Client in GraphQL in NestJS nutzen
  * Pagination mit Prisma Client in NestJS
  * Yarn v3 PnP nicht mit Prisma möglich
  * Apollo Anomalien in Vue3: Mehrfaches triggern von Queries und Mutations
  * Parameter `Transcription`: Musikdateien parsen
  * Semantische Zusammenhänge zwischen Parametern (Timeline Logik: Dirty/Clean)

</VClicks>

<!-- * globaler Pool für `Keywords` und `Instrumente` -->

<!--
<div class="text-2xl text-red-600">in 25:00 - out 27:00</div>

* Orchestration:
  * nicht zu detailliert, da es dann eine Transkription ist
  * muss aber noch genug Informationen beinhalten
* Umfang und Komplexität des Projektes (Parameter mit je individuellen Evaluationen)
-->

---

<AppReferenceToWrittenWork :pages="['4.6.3.']" />

<div class="flex flex-row">
  <h1>Besondere Hürden</h1>
  <div class="pt-3 pl-8 text-xl baseColor">Entwicklung des Timeline-Ansatzes</div>
</div>

<div class="flex flex-row justify-between">
  <div class="w-20/41" v-click>
    <div class="mb-3">
      Erster Ansatz: Div Container
    </div>
    <div class="h-60">
      <img src="/assets/timeline-development/Countdown_old.png" />
    </div>
    <div class="flex flex-col space-y-2">
      <div><mdi-plus class="text-green-600 mr-2" />Dynamische Höhe pro Zeile</div>
      <div><mdi-minus class="text-red-600 mr-2" />Horizontales Scrollen ohne Offset (Rücksprünge)</div>
      <div><mdi-minus class="text-red-600 mr-2" />Zoomen extern mit Faktor und Positionsverlust</div>
      <div><mdi-minus class="text-red-600 mr-2" />Keine relativen Zeiten bei Klicken in eine Zeile</div>
    </div>
  </div>
  <div class="w-20/41" v-click>
    <div class="mb-2">
      Zweiter Ansatz: Apache ECharts
    </div>
    <div class="h-60">
      <img src="/assets/timeline-development/Countdown_new.png" />
    </div>
    <div class="flex flex-col space-y-2">
      <div><mdi-minus class="text-red-600 mr-2" />Keine dynamische Höhe pro Zeile</div>
      <div><mdi-plus class="text-green-600 mr-2" />Horizontales Scrollen und Zoom kontrollierbar</div>
      <div><mdi-plus class="text-green-600 mr-2" />Position bleibt bei Datenänderungen und Zoom</div>
      <div><mdi-plus class="text-green-600 mr-2" />Relativen Zeiten bei Klicken in eine Zeile</div>
    </div>
  </div>
</div>

<div class="text-xs mt-4 text-right text-gray-400">
  &copy;
  <a href="https://fmadb.org/movie/one/cl8bmhyu7568250soulp89d9bt/cl8bmiy01570540souzehyq8xb" target="_blank">
  https://fmadb.org/movie/one/cl8bmhyu7568250soulp89d9bt/cl8bmiy01570540souzehyq8xb
  </a>
</div>

<!--
<div class="text-2xl text-red-600">in 27:00 - out 28:00</div>

* echte Daten des Films `Countdown`
-->

---

# Mehr in meiner schriftlichen Arbeit

<div class="flex flex-row justify-between">
  <img src="/assets/written-work/page-001_cover-page.jpg" class="h-100 mx-auto border" />
</div>

<!--
<div class="text-2xl text-red-600">Endspurt</div>

* Mehr nachzulesen in meiner schriftlichen Arbeit
* Titel vorlesen
* Welche sich über 127 großartige Seiten erstreckt ...
-->

---

# Mehr in meiner schriftlichen Arbeit

<div class="flex flex-row justify-between">
  <img src="/assets/written-work/page-005_table-of-contents-1.jpg" class="h-100 mx-auto border" />
  <img src="/assets/written-work/page-006_table-of-contents-2.jpg" class="h-100 mx-auto border" />
  <img src="/assets/written-work/page-007_table-of-contents-3.jpg" class="h-100 mx-auto border" />
</div>

<!--
<div class="text-2xl text-red-600">Endspurt</div>

* ... und wie folgt strukturiert ist
-->

---

<AppIntroLogoWithInformation />
