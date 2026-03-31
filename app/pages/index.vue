<script setup lang="ts">
const items = [
  "/images/nick.png",
  "/images/damian.png",
  "/images/layaan.png",
  "/images/thomas.png",
  "/images/nora.jpeg",
];
import { ref } from "vue";

const openSprint = ref<number | null>(null);
const toggleSprint = (index: number) => {
  openSprint.value = openSprint.value === index ? null : index;
};
</script>

<template>
  <Title>TimeThiefs</Title>
  <div
    class="relative bg-gradient-to-r from-purple-600 to-blue-600 h-screen text-white overflow-hidden"
  >
    <div class="absolute inset-0">
      <img
        src="/images/Background.jpg"
        alt="Background Image"
        class="object-cover object-center w-full h-100vh"
      />
      <div class="absolute inset-0"></div>
    </div>

    <div
      class="relative z-10 flex flex-col justify-center items-center h-full text-center hero-content"
    >
      <img src="/images/logo.png" alt="Time Thieves" class="w-256 mb-4" />
    </div>
  </div>
  <div class="justify-center flex mt-5">
    <div class="text-6xl text-white mb-5">Ontmoet De Time Thieves</div>
  </div>
  <!-- <div class="mt-10 mb-20">
        <UCarousel v-slot="{ item }" auto-scroll="true" loop="true" :items="items" :ui="{
            item: 'basis-[40%] transition-opacity'
        }" class="">
            <img :src="item" width="264" height="274" class="rounded-4xl">
        </UCarousel>
    </div> -->
  <div class="flex justify-center mb-20 gap-8">
    <UCard variant="solid" class="w-64 flex flex-col">
      <template #header>
        <div class="justify-self-center">Thomas Martini</div>
      </template>

      <img class="w-64 rounded-xl" src="/images/thomas.png" />

      <template class="flex" #footer>
        <div>Creatieve Media en Game Technologie</div>

        <div class="text-sm text-gray-400">1013596@hr.nl</div>
      </template>
    </UCard>
    <UCard variant="solid" class="w-64 flex flex-col">
      <template #header>
        <div class="justify-self-center">Nick Wijmans</div>
      </template>

      <img class="w-64 rounded-xl" src="/images/nick.png" />

      <template class="flex" #footer>
        <div>Informatica</div>

        <div class="text-sm text-gray-400">1071792@hr.nl</div>
      </template>
    </UCard>
    <UCard variant="solid" class="w-64 flex flex-col">
      <template #header>
        <div class="justify-self-center">Damian Breuer</div>
      </template>

      <img class="w-64 rounded-xl" src="/images/damian.png" />

      <template class="flex" #footer>
        <div>Communication and Multimedia Design</div>

        <div class="text-sm text-gray-400">1077853@hr.nl</div>
      </template>
    </UCard>
    <UCard variant="solid" class="w-64 flex flex-col">
      <template #header>
        <div class="justify-self-center">Nora Amghar</div>
      </template>

      <img
        class="w-64 rounded-xl"
        src="/images/nora.jpeg"
        style="height: 208px; overflow: hidden; object-fit: cover"
      />

      <template class="flex" #footer>
        <div>Applied Data Science & AI</div>

        <div class="text-sm text-gray-400">1082597@hr.nl</div>
      </template>
    </UCard>
  </div>

  <div class="w-full text-center mt-20">
    <button
      @click="toggleSprint(0)"
      class="text-5xl font-bold text-white mb-10 flex items-center justify-center gap-4 w-full"
    >
      Sprint 0
      <span>{{ openSprint === 0 ? "▲" : "▼" }}</span>
    </button>
  </div>

  <!-- CONTENT -->
  <transition name="fade">
    <div v-if="openSprint === 0">
      <!-- De Opdracht -->
      <div class="w-[80%] mx-auto py-24 flex items-center justify-center">
        <div class="text-center text-white max-w-3xl">
          <h2 class="text-5xl font-bold mb-6">De Opdracht</h2>
          <p class="text-lg text-gray-300 mb-8">
            Hoe kunnen we de historie van Rotterdam, met behulp van 3DRotterdam,
            op een leuke en interactieve manier overbrengen naar de de jongeren
            in Rotterdam, zodat zij meer naar buiten gaan en de stad beter leren
            kennen?
          </p>
        </div>
      </div>
      <div
        class="w-[80%] mx-auto flex flex-col md:flex-row items-center justify-between gap-10 py-20"
      >
        <!-- Tekst links -->
        <div class="md:w-1/2 text-white">
          <h2 class="text-4xl font-bold mb-6">De Huidige Situatie</h2>
          <p class="text-lg text-gray-300 mb-6">
            We hebben van het Stadsarchief en de Gemeente Rotterdam de opdracht
            gekregen om te kijken naar manieren om met behulp van 3D Rotterdam
            de inwoners van de stad beter kennis te laten maken met de historie
            van de stad. Er is al een 3D versie van Rotterdam beschikbaar, maar
            deze toont alleen de moderne stad en wordt momenteel nog niet
            gebruikt voor andere doeleinden. De Gemeente Rotterdam wil dat er
            nieuwe toepassingen komen voor 3D Rotterdam, zodat dit voor meer
            doeleinden ingezet kan gaan worden in combinatie met het Open Urban
            Platform. Het Stadsarchief Rotterdam heeft waardevolle historische
            bronnen, maar deze zijn vooral statisch en lastig te bereiken voor
            een breed publiek. Zij zijn op zoek naar nieuwe manieren om deze
            documenten in te zetten voor educatie.
          </p>
        </div>

        <!-- Afbeelding rechts -->
        <div class="md:w-1/2">
          <img
            src="/images/Rotterdam3D.jpg"
            alt="Time Thiefs"
            class="w-full h-[400px] object-cover rounded-3xl shadow-2xl"
          />
        </div>
      </div>
      <div
        class="w-[80%] mx-auto flex flex-col md:flex-row items-center justify-between gap-10 py-20"
      >
        <!-- Afbeelding links -->
        <div class="md:w-1/2">
          <img
            src="/images/Rotterdam.jpg"
            alt="Time Thiefs"
            class="w-full h-[400px] object-cover rounded-3xl shadow-2xl"
          />
        </div>

        <!-- Tekst rechts -->
        <div class="md:w-1/2 text-white">
          <h2 class="text-4xl font-bold mb-6">De Gewenste Situatie</h2>
          <p class="text-lg text-gray-300 mb-6">
            We willen een werkende, immersieve applicatie maken, waarin de
            inwoners van Rotterdam de stad op een interactieve manier kunnen
            ontdekken. De gebruikers kunnen hiermee inzicht krijgen in de
            historische ontwikkeling van de stad Rotterdam. We maken hierbij
            gebruik van 3D Rotterdam en de data van het Open Urban Platform. We
            willen het Stadsarchief Rotterdam hierbij gaan betrekken, zodat we
            in samenwerking met hun een interactieve gamification kunnen gaan
            ontwikkelen, waarbij het verleden van de stad in de belangstelling
            staat en het jongeren aanmoedigt om meer naar buiten te gaan om meer
            over de stad te weten te komen.
          </p>
        </div>
      </div>
      <div
        class="w-[80%] mx-auto flex flex-col md:flex-row items-center justify-between gap-10 py-20"
      >
        <!-- Tekst links -->
        <div class="md:w-1/2 text-white">
          <h2 class="text-4xl font-bold mb-6">Eerste Concept En Verhaal</h2>
          <p class="text-lg text-gray-300 mb-6">
            Eerste concept<br /><br />
            The TimeThiefs:<br />
            Een educatieve game dat doormiddel van storytelling verschillende
            historische gebeurtenissen en monumenten aan het licht brengt.<br /><br />

            Het verhaal:<br />
            Rotterdam wordt langzaam veranderd: de TimeThiefs stelen niet alleen
            gebouwen en monumenten, maar ook de geschiedenis en identiteit van
            de stad. Wat ooit het hart van Rotterdam was, dreigt voorgoed
            verloren te gaan.<br /><br />

            Herstel de geschiedenis van Rotterdam door gebouwen, monumenten en
            herinneringen terug te brengen, en ontdek tegelijkertijd het geheim
            achter de TimeThiefs.
          </p>
        </div>

        <!-- Afbeelding rechts -->
        <div class="md:w-1/2">
          <img
            src="/images/storyboard.jfif"
            alt="Time Thiefs"
            class="w-full h-[400px] object-cover rounded-3xl shadow-2xl"
          />
        </div>
      </div>
      <div
        class="w-[80%] mx-auto flex flex-col md:flex-row items-center justify-between gap-10 py-20"
      >
        <!-- Tekst links -->
        <div class="md:w-1/2 text-white">
          <h2 class="text-4xl font-bold mb-6">De Scope</h2>
          <p class="text-lg text-gray-300 mb-6">
            Binnen de scope:<br />
            Het bouwen van een immersieve viewer<br />
            De basisinteractie in een augmented reality (tijdswissel +
            informatiepunten)<br />
            Documentatie voor overdraagbaarheid<br />
            <br />
            Buiten de scope:<br />
            Volledige stad<br />
            Multiplayer<br />
            <br />
            Beperkingen:<br />
            Tijd: 20 weken<br />
            Technische leercurve Unreal en 3D tiles<br />
            Beperkte informatie over historie<br />
          </p>
        </div>

        <!-- Afbeelding rechts -->
        <div class="md:w-1/2">
          <img
            src="/images/watertaxi.jpg"
            alt="Time Thiefs"
            class="w-full h-[400px] object-cover rounded-3xl shadow-2xl"
          />
        </div>
      </div>
      <div
        class="w-[80%] mx-auto flex flex-col md:flex-row items-center justify-between gap-10 py-20"
      >
        <!-- Afbeelding links -->
        <div class="md:w-1/2">
          <img
            src="/images/Rotterdam2.jpg"
            alt="Time Thiefs"
            class="w-full h-[400px] object-cover rounded-3xl shadow-2xl"
          />
        </div>

        <!-- Tekst rechts -->
        <div class="md:w-1/2 text-white">
          <h2 class="text-4xl font-bold mb-6">De Randvoorwaarden</h2>
          <p class="text-lg text-gray-300 mb-6">
            Het ontwerp van de 3D-game moet gebruikmaken van het Urban Open
            Platform (OUP) en het Stadsarchief Rotterdam, waarbij uitsluitend
            open of AVG-proof datasets worden gebruikt. De dataverwerking moet
            reproduceerbaar en goed gedocumenteerd zijn, zonder offline kopieën
            op te slaan. Het systeem moet draaien op standaard laptops en
            mobiele apparaten en ontwikkeld worden met open-source tools. Er
            mogen geen persoonsgegevens worden verwerkt en GPS-gegevens mogen
            alleen geanonimiseerd worden gebruikt. De game moet transparant zijn
            over datagebruik. De toepassing moet begrijpelijk zijn voor jongeren
            (12–18 jaar), speelbaar zonder uitgebreide voorkennis en
            mobielvriendelijk en toegankelijk voor iedereen. Het project moet
            binnen één semester realiseerbaar zijn, met focus op een selectie
            van belangrijke monumenten. Functioneel moet het systeem monumenten
            kunnen verbergen en laten verschijnen, verhalen uit het OUP
            integreren en locatiegebaseerde interacties ondersteunen. Het
            ontwerp moet technisch haalbaar, AVG-proof, inclusief en schaalbaar
            zijn binnen de beschikbare tijd.
          </p>
        </div>
      </div>
      <div
        class="w-[80%] mx-auto flex flex-col md:flex-row items-center justify-between gap-10 py-20"
      >
        <!-- Tekst links -->
        <div class="md:w-1/2 text-white">
          <h2 class="text-4xl font-bold mb-6">De Doelgroep</h2>
          <p class="text-lg text-gray-300 mb-6">
            <b>Middelbare scholieren (12–18 jaar)</b><br />
            Interactief leren over Rotterdam<br />
            Spelenderwijs de geschiedenis ontdekken<br />
            Inzicht in hoe de stad zich door de tijd ontwikkelde<br /><br />

            <b>(Nieuwe) Rotterdammers</b><br />
            Interesse in geschiedenis en stedelijke ontwikkeling<br />
            Inzicht krijgen in waarom Rotterdam er nu zo uitziet<br />
            Interactieve 3D-ervaring van stad en gebeurtenissen<br />
          </p>
        </div>

        <!-- Afbeelding rechts -->
        <div class="md:w-1/2">
          <img
            src="/images/Doelgroep.jpg"
            alt="Time Thiefs"
            class="w-full h-[400px] object-cover rounded-3xl shadow-2xl"
          />
        </div>
      </div>
      <div class="w-[80%] mx-auto py-24 flex items-center justify-center">
        <div class="text-center text-white max-w-3xl">
          <h2 class="text-5xl font-bold mb-6">Team waarden</h2>

          <p class="text-lg text-gray-300 mb-8">
            Team Waarden:<br />
            - Plezier:<br />
            We moeten ons richten op ontspanning en cultuur, om zo de hybride
            stad levendig en menselijk te houden.<br />

            We willen de mensen van Rotterdam op een leuke en interactieve
            manier betrekken bij de geschiedenis van de stad.<br /><br />

            - Vriendschap:<br />
            We moeten informele netwerken en gemeenschapsvorming actief
            stimuleren als bron van kansen.<br />

            Met ons product willen we inwoners van Rotterdam met elkaar
            verbinden en aanzetten om samen er op uit te gaan.<br /><br />

            - Bestaanszekerheid:<br />
            We moeten zorgen dat iedereen kan meekomen in de samenleving en dus
            ook in de hybride wereld.<br />

            We willen inwoners meer betrekken bij de stad om zo de samenleving
            met elkaar te verbinden.<br /><br />

            - Uitdaging:<br />
            We moeten bereid zijn om gevestigde systemen fundamenteel te
            herzien, Rotterdam kan zich alleen blijven ontwikkelen als we durven
            te experimenteren.<br />

            We proberen onszelf uit te dagen door naar nieuwe oplossingen te
            zoeken en zijn bereid om te experimenteren en onze ideeën te herzien
            om het beste eruit te halen.<br /><br />

            - Vertrouwen:<br />
            We moeten vertrouwen opbouwen tussen mens en technologie door met
            burgers, bedrijven en overheid transparant samen te werken, om zo
            samen te kunnen groeien.<br />

            We willen dat de gebruiker zich vertrouwd voelt bij ons product en
            zich veilig voelt.<br />
          </p>
        </div>
      </div>
      <div
        class="w-[80%] mx-auto flex flex-col md:flex-row items-center justify-between gap-10 py-20"
      >
        <!-- Tekst links -->
        <div class="md:w-1/2 text-white">
          <h2 class="text-4xl font-bold mb-6">De Backlog</h2>
          <p class="text-lg text-gray-300 mb-6">
            Als gebruiker wil ik een 3D versie van Rotterdam kunnen bekijken,
            zodat ik meer van Rotterdam kan ontdekken.<br />
            Als gebruiker wil ik punten in de stad kunnen bezoeken, zodat ik
            meer informatie kan verzamelen over de stad.<br />
            Als gebruiker wil ik de historische veranderingen door de tijd
            kunnen bekijken, zodat ik een beter beeld krijg van Rotterdam door
            de tijd
          </p>
        </div>

        <!-- Afbeelding rechts -->
        <div class="md:w-1/2">
          <img
            src="/images/markthal-rotterdam.jpg"
            alt="Time Thiefs"
            class="w-full h-[400px] object-cover rounded-3xl shadow-2xl"
          />
        </div>
      </div>
      <div
        class="w-[80%] mx-auto flex flex-col md:flex-row items-center justify-between gap-10 py-20"
      >
        <!-- Tekst links -->
        <div class="md:w-1/2 text-white">
          <h2 class="text-4xl font-bold mb-6">Sprint 1 Doel En Planning</h2>
          <p class="text-lg text-gray-300 mb-6">
            Aan het einde van deze sprint is er een onderbouwde projectdefinitie
            waarin:<br />
            De hoofdvraag is aangescherpt<br />
            De haalbaarheid binnen 1 semester is vastgelegd<br />
            De technische en inhoudelijke uitvoeringsvorm is gekozen<br />
            De verdeling per discipline helder is<br /><br />

            Deze sprint richten we ons op:<br />
            Het onderzoeken van technische mogelijkheden<br />
            Het bepalen van de meest haalbare uitvoeringsvorm<br />
            Rolverdeling van disciplines<br /><br />

            Sprint is succesvol wanneer:<br />
            Hoofdvraag en deelvragen definitief zijn geformuleerd<br />
            Gap-analyse is uitgewerkt<br />
            Er een beargumenteerde keuze is gemaakt voor één uitvoeringsvorm<br />
            Randvoorwaarden en scope definitief zijn vastgesteld<br />
            Er een duidelijke rolverdeling per discipline is gemaakt<br />
            Globale planning voor komende sprints is opgebouwd
          </p>
        </div>

        <!-- Afbeelding rechts -->
        <div class="md:w-1/2">
          <img
            src="/images/Rotterdam.jpg"
            alt="Time Thiefs"
            class="w-full h-[400px] object-cover rounded-3xl shadow-2xl"
          />
        </div>
      </div>
      <div class="w-[80%] mx-auto py-24 flex items-center justify-center">
        <div class="text-center text-white max-w-3xl">
          <h2 class="text-5xl font-bold mb-6">Stakeholders</h2>

          <p class="text-lg text-gray-300 mb-8">
            <b>Gemeente Rotterdam OUP</b><br />
            Joris Koolen<br />
            j.koolen@rotterdam.nl<br /><br />

            <b>Stadsarchief Rotterdam</b><br />
            Ingmar Vroomen<br />
            ih.vroomen@rotterdam.nl<br /><br />

            <b>Gemeente Rotterdam Citiverse</b><br />
            Isabel Fokkens<br />
            i.fokkens@rotterdam.nl
          </p>
        </div>
      </div>
    </div>
  </transition>
  <div class="w-full text-center mt-20">
    <button
      @click="toggleSprint(1)"
      class="text-5xl font-bold text-white mb-10 flex items-center justify-center gap-4 w-full"
    >
      Sprint 1
      <span>{{ openSprint === 1 ? "▲" : "▼" }}</span>
    </button>
  </div>

  <transition name="fade">
    <div v-if="openSprint === 1">
      <div
        class="w-[80%] mx-auto flex flex-col md:flex-row items-center justify-between gap-10 py-20"
      >
        <div class="md:w-1/2 text-white">
          <h2 class="text-4xl font-bold mb-6">
            <b>Inzichten Deskresearch Gamification</b>
          </h2>
          <p class="text-lg text-gray-300 mb-6">
            Gebruikt spelelementen, is geen losstaand spel.
            <br />Aansporen en motiveren om iets te gaan doen. <br />Focussen op
            langdurig proces/verandering. <br />Niet elke speler vind hetzelfde
            leuk.<br />
            Moeite en tijd van gebruiker.
          </p>
        </div>

        <div class="md:w-1/2">
          <img
            src="/images/gamification.png"
            class="w-full h-[400px] object-cover rounded-3xl shadow-2xl"
          />
        </div>
      </div>

      <div
        class="w-[80%] mx-auto flex flex-col md:flex-row items-center justify-between gap-10 py-20"
      >
        <!-- Afbeelding links -->
        <div class="md:w-1/2">
          <img
            src="/images/stakeholderAnalyse.png"
            alt="Time Thiefs"
            class="w-full h-[500px] object-cover rounded-3xl shadow-2xl"
          />
        </div>

        <!-- Tekst rechts -->
        <div class="md:w-1/2 text-white">
          <h2 class="text-4xl font-bold mb-6">Stakeholder Analyse</h2>
          <p class="text-lg text-gray-300 mb-6">
            <b>Direct:</b>
            <br />(Time Thiefs) <br />Stadsarchief, Ingmar Wetenschappelijk
            Adviseur - Raadplegen van historische bronnen <br />Open Urban
            Platform, Joris - Gebruik van data <br />3D Rotterdam, Joris -
            Achterhalen verloop proces <br />Studio docenten <br />Cityverse -
            Digitale stad toegankelijker maken, Relatie tussen inwoners en
            digitaal platform<br /><br />

            <b>Indirect:</b>
            <br />Gemeente Rotterdam - Vooruitstrevend <br />Jan 360fabriek -
            Achterhalen verloop proces en technische realisatie
            <br />Katoenhuis, Marjolein <br />Scholen Rotterdam <br />CMI
            <br />Techpartners binnen Rotterdam - Uitwerken innovatief concept
            <br />Reisbureau/Informatiepunt Rotterdam<br /><br />

            <b>Samenleving:</b>
            <br />Rotterdamse middelbare scholieren - Leren door Gamification
            <br />Nieuwe inwoners Rotterdam - De stad leren kennen
            <br />Hogeschool Rotterdam <br />Toeristen Rotterdam - Rotterdam
            ontdekken <br />Beleidmakers Rotterdam - Beleid maken
          </p>
        </div>
      </div>
      <div class="w-[80%] mx-auto py-20 text-white">
        <!-- Titel + tekst -->
        <div class="max-w-3xl mb-10">
          <h2 class="text-4xl font-bold mb-6">
            Technisch Onderzoek naar Cesium i.c.m. Unreal
          </h2>

          <p class="text-lg text-gray-300 mb-6">
            Er is tijdens de eerste sprint technisch onderzoek gedaan naar het
            gebruik van Cesium in Unreal Engine. Dit is vooral een verkennend
            onderzoek geweest naar de mogelijkheden van Cesium in Unreal en of
            het bruikbaar gaat zijn voor het maken van ons definitieve
            prototype.
          </p>

          <p class="text-lg text-gray-300 mb-6">
            Deze verkenning ging met name om:
            <br />Unreal Engine ontdekken <br />Cesium installeren en laten
            werken in Unreal <br />Inladen van Google Maps data met Cesium als
            eerste proof of concept <br />Inladen van OUP data met Cesium als
            uiteindelijk proof of concept <br />Conclusies trekken aan de hand
            van bevindingen
          </p>
        </div>

        <div class="flex flex-col md:flex-row gap-6">
          <!-- Afbeelding 1 -->
          <div class="relative w-full md:w-1/2">
            <img
              src="/images/cesium1.png"
              class="w-full h-[600px] object-cover rounded-3xl shadow-2xl"
            />

            <!-- Tekst linksonder -->
            <div class="absolute bottom-0 left-0 p-4">
              <p
                class="text-white text-lg font-semibold bg-black/50 px-4 py-2 rounded-xl"
              >
                Cesium in Unreal met Google Maps data
              </p>
            </div>
          </div>

          <!-- Afbeelding 2 -->
          <div class="relative w-full md:w-1/2">
            <img
              src="/images/cesium2.png"
              class="w-full h-[600px] object-cover rounded-3xl shadow-2xl"
            />

            <!-- Tekst linksonder -->
            <div class="absolute bottom-0 left-0 p-4">
              <p
                class="text-white text-lg font-semibold bg-black/50 px-4 py-2 rounded-xl"
              >
                Cesium in Unreal met OUP data
              </p>
            </div>
          </div>
        </div>
      </div>
      <div class="w-[80%] mx-auto py-20 text-white">
        <!-- Titel + tekst -->
        <div class="max-w-3xl mb-10">
          <h2 class="text-4xl font-bold mb-6">
            Technisch onderzoek naar CesiumJS in de browser
          </h2>

          <p class="text-lg text-gray-300 mb-6">
            Tijdens deze sprint is er gekeken naar de technische mogelijkhede
            van cesium binnen een browser. Er is gekeken naar de mogelijkheden
            van cesium binnen een browser en of het mogelijk is om hiermee een
            prototype te maken. Er is gekeken naar het inladen van google maps
            data en OUP data in cesium binnen een browser. Verder is er ook nog
            research gedaan naar AR mogelijkheden binnen een browser. Dit wordt
            verder onderzocht in sprint 2. Er is ook gekeken naar het inladen
            van 3D objecten op de map met cesium binnen een browser. Dit is
            gelukt en er zijn 3D eendjes op de map geladen met de data van 3D
            rotterdam.
          </p>

          <p class="text-lg text-gray-300 mb-6">
            Deze verkenning ging met name om:
            <br />De mogelijkheden van cesium binnen een browser ontdekken
            <br />Cesium installeren en laten werken in een browser
            <br />Inladen van Google Maps data met Cesium als eerste proof of
            concept <br />Inladen van OUP data met Cesium als uiteindelijk proof
            of concept <br />Conclusies trekken aan de hand van bevindingen
            <br />3D objecten inladen op de map met cesium
          </p>
        </div>

        <div class="flex flex-col md:flex-row gap-6">
          <!-- Afbeelding 1 -->
          <div class="relative w-full md:w-1/2">
            <img
              src="/images/rotterdam upclose.PNG"
              class="w-full h-[600px] object-cover rounded-3xl shadow-2xl"
            />

            <!-- Tekst linksonder -->
            <div class="absolute bottom-0 left-0 p-4">
              <p
                class="text-white text-lg font-semibold bg-black/50 px-4 py-2 rounded-xl"
              >
                Cesium geladen in een browser via javascript
              </p>
            </div>
          </div>

          <!-- Afbeelding 2 -->
          <div class="relative w-full md:w-1/2">
            <img
              src="/images/rotterdam duckies.PNG"
              class="w-full h-[600px] object-cover rounded-3xl shadow-2xl"
            />

            <!-- Tekst linksonder -->
            <div class="absolute bottom-0 left-0 p-4">
              <p
                class="text-white text-lg font-semibold bg-black/50 px-4 py-2 rounded-xl"
              >
                3D eendjes die zijn geladen op de map met de data van 3D
                rotterdam
              </p>
            </div>
          </div>
        </div>
      </div>
      <div
        class="w-[80%] mx-auto flex flex-col md:flex-row items-center justify-between gap-10 py-20"
      >
        <!-- Afbeelding links -->
        <div class="md:w-1/2">
          <img
            src="/images/stadsarchief_rotterdam.png"
            alt="Time Thiefs"
            class="w-full h-[500px] object-cover rounded-3xl shadow-2xl"
          />
        </div>

        <!-- Tekst rechts -->
        <div class="md:w-1/2 text-white">
          <h2 class="text-4xl font-bold mb-6">
            Stadsarchief historische kaarten
          </h2>
          <p class="text-lg text-gray-300 mb-6">
            Tijdens deze sprint is er onderzoek gedaan naar hoe historische
            kaarten, uit het Stadsarchief Rotterdam, gebruikt kunnen worden als
            basis voor een 3D-omgeving. Hieruit blijkt dat historische kaarten
            eerst omgezet moeten worden in bruikbare data voordat het gebruikt
            kan worden in een game.<br /><br />

            <b>Drie belangrijke stappen:</b><br />
            Georeferencing: Het koppelen van een historische kaart aan echte
            coördinaten, zodat de kaart op de juiste plek ligt (QGIS) <br />
            Vectoriseren: Het omzetten van gebouwen, wegen, en andere elementen
            naar digitalen vormen. Data exporteren: het opslaan van deze
            gegevens in formaten zoals GeoJSON, zodat deze gebruikt kunnen
            worden in 3D-tools en game-engines. <br /><br />

            <b>Acties voor sprint 2:</b><br />
            Een geschikte historische kaart van Rotterdam selecteren<br />
            Deze kaart georeferencen<br />
            Een deel van de kaart vectoriseren (rekening houden met de gekozen
            monumenten)<br />
            Data exporteren naar bruikbaar formaat<br />
            Van 2D naar 3D gebouwen (Nog onderzoeken)<br />
          </p>
        </div>
      </div>
      <div
        class="w-[80%] mx-auto flex flex-col md:flex-row items-center justify-between gap-10 py-20"
      >
        <!-- Tekst links -->
        <div class="md:w-1/2 text-white">
          <h2 class="text-4xl font-bold mb-6">
            Deskresearch naar de geschiedenis van Rotterdam 
          </h2>
          <p class="text-lg text-gray-300 mb-6">
            Deskresearch naar de geschiedenis van Rotterdam is uitgevoerd
            waarbij de belangrijkste gebeurtenissen van vóór 1940 tot heden zijn
            verzameld en geanalyseerd.<br /><br />

            Hierbij is specifiek gekeken naar keerpunten zoals het Bombardement
            op Rotterdam en de daaropvolgende wederopbouw.<br /><br />

            Het doel van dit onderzoek is om relevante historische data te
            selecteren en deze te verwerken in ons project, zodat belangrijke
            gebeurtenissen als basis kunnen dienen voor het game design.
          </p>
        </div>

        <!-- Afbeelding rechts -->
        <div class="md:w-1/2">
          <img
            src="/images/image 5.png"
            alt="Time Thiefs"
            class="w-full h-[400px] object-cover rounded-3xl shadow-2xl"
          />
        </div>
      </div>
    </div>
  </transition>
  <div class="w-full text-center mt-20">
    <button
      @click="toggleSprint(2)"
      class="text-5xl font-bold text-white mb-10 flex items-center justify-center gap-4 w-full"
    >
      Sprint 2
      <span>{{ openSprint === 2 ? "▲" : "▼" }}</span>
    </button>
  </div>

  <transition name="fade">
    <div v-if="openSprint === 2">
      <div
        class="w-[80%] mx-auto flex flex-col md:flex-row items-center justify-between gap-10 py-20"
      >
        <div class="md:w-1/2 text-white">
          <h2 class="text-4xl font-bold mb-6">
            <b>Doelgroep aangescherpt</b>
          </h2>
          <p class="text-lg text-gray-300 mb-6">
            We hebben onze doelgroep aangescherpt naar<br /><br />
            Toeristen die op bezoek zijn in Rotterdam en door de stad heen
            willen ontdekken<br />
            Middelbare scholieren<br />
            Inwoners van Rotterdam die graag meer willen weten over de
            geschiedenis van de stad<br />
          </p>
        </div>

        <div class="md:w-1/2">
          <img
            src="/images/Doelgroep2.jpg"
            class="w-full h-[400px] object-fit rounded-3xl shadow-2xl"
          />
        </div>
      </div>

      <div
        class="w-[80%] mx-auto flex flex-col md:flex-row items-center justify-between gap-10 py-20"
      >
        <!-- Afbeelding links -->
        <div class="md:w-1/2">
          <img
            src="/images/watertaxi.jpg"
            alt="Time Thiefs"
            class="w-full h-[500px] object-cover rounded-3xl shadow-2xl"
          />
        </div>

        <!-- Tekst rechts -->
        <div class="md:w-1/2 text-white">
          <h2 class="text-4xl font-bold mb-6">ETL Gebruiken</h2>
          <p class="text-lg text-gray-300 mb-6">
            ETL gebruiken Voor dit onderzoek is onderzocht hoe het ETL-proces
            (Extract, Transform, Load) toegepast kan worden binnen het project.
            Hierbij ligt de focus op het verzamelen van relevante data, het
            transformeren naar bruikbare informatie en het integreren ervan in
            de game. Door ETL toe te passen, kan het concept van dynamische
            veranderingen, zoals het laten verschijnen en verdwijnen van
            monumenten, op een gestructureerde en schaalbare manier worden
            gerealiseerd.
          </p>
        </div>
      </div>
      <div class="w-[80%] mx-auto py-20 text-white">
        <!-- Titel + tekst -->
        <div class="max-w-3xl mb-10">
          <h2 class="text-4xl font-bold mb-6">Eerste versie UI</h2>
        </div>

        <div class="flex flex-col md:flex-row gap-6">
          <!-- Afbeelding 1 -->
          <div class="relative w-full md:w-1/2">
            <img
              src="/images/MainView.png"
              class="w-full h-[600px] object-fit rounded-3xl shadow-2xl"
            />

            <!-- Tekst linksonder -->
            <div class="absolute bottom-0 left-0 p-4">
              <p
                class="text-white text-lg font-semibold bg-black/50 px-4 py-2 rounded-xl"
              >
                Main view
              </p>
            </div>
          </div>

          <!-- Afbeelding 2 -->
          <div class="relative w-full md:w-1/2">
            <img
              src="/images/Inventory.png"
              class="w-full h-[600px] object-fit rounded-3xl shadow-2xl"
            />

            <!-- Tekst linksonder -->
            <div class="absolute bottom-0 left-0 p-4">
              <p
                class="text-white text-lg font-semibold bg-black/50 px-4 py-2 rounded-xl"
              >
                Inventory
              </p>
            </div>
          </div>
          <div class="relative w-full md:w-1/2">
            <img
              src="/images/ZoomIn.png"
              class="w-full h-[600px] object-fit rounded-3xl shadow-2xl"
            />

            <!-- Tekst linksonder -->
            <div class="absolute bottom-0 left-0 p-4">
              <p
                class="text-white text-lg font-semibold bg-black/50 px-4 py-2 rounded-xl"
              >
                Inzoomen
              </p>
            </div>
          </div>

          <!-- Afbeelding 2 -->
          <div class="relative w-full md:w-1/2">
            <img
              src="/images/ZoomOut.png"
              class="w-full h-[600px] object-fit rounded-3xl shadow-2xl"
            />

            <!-- Tekst linksonder -->
            <div class="absolute bottom-0 left-0 p-4">
              <p
                class="text-white text-lg font-semibold bg-black/50 px-4 py-2 rounded-xl"
              >
                Uitzoomen
              </p>
            </div>
          </div>
          <div class="relative w-full md:w-1/2">
            <img
              src="/images/ColoredAreas.png"
              class="w-full h-[600px] object-fit rounded-3xl shadow-2xl"
            />

            <!-- Tekst linksonder -->
            <div class="absolute bottom-0 left-0 p-4">
              <p
                class="text-white text-lg font-semibold bg-black/50 px-4 py-2 rounded-xl"
              >
                Gedeeltes van de map waar AR geactiveerd kan worden
              </p>
            </div>
          </div>

          <!-- Afbeelding 2 -->
          <div class="relative w-full md:w-1/2">
            <img
              src="/images/ARExperience.png"
              class="w-full h-[600px] object-fit rounded-3xl shadow-2xl"
            />

            <!-- Tekst linksonder -->
            <div class="absolute bottom-0 left-0 p-4">
              <p
                class="text-white text-lg font-semibold bg-black/50 px-4 py-2 rounded-xl"
              >
                AR view met informatiepunten en 3D objecten
              </p>
            </div>
          </div>
        </div>
      </div>
      <div class="w-[80%] mx-auto py-20 text-white">
        <!-- Titel + tekst -->
        <div class="max-w-3xl mb-10">
          <h2 class="text-4xl font-bold mb-6">
            Nieuwe Versie cesiumJS met Geolocatie tracker
          </h2>

          <p class="text-lg text-gray-300 mb-6">
            Er is deze periode gewerkt aan het maken van een nieuwe versie van
            cesiumJS in de browser, waarbij er een geolocatie tracker is
            toegevoegd. Deze tracker maakt het mogelijk om de locatie van de
            gebruiker te volgen en deze te gebruiken om interactieve elementen
            op de kaart te activeren. Dit is een belangrijke stap in het
            ontwikkelen van ons prototype, omdat het ons in staat stelt om
            locatiegebaseerde interacties te implementeren en zo een meer
            immersieve ervaring te creëren voor de gebruiker.
          </p>
        </div>

        <div class="flex flex-col md:flex-row gap-6">
          <!-- Afbeelding 1 -->
          <div class="relative w-full md:w-1/2">
            <img
              src="/images/geolocation 2.jpeg"
              class="w-full h-[600px] object-scale-down rounded-3xl shadow-2xl"
            />

            <!-- Tekst linksonder -->
            <div class="absolute bottom-0 left-0 p-4">
              <p
                class="text-white text-lg font-semibold bg-black/50 px-4 py-2 rounded-xl"
              >
                De geolocatie van de speler wordt weergegeven met de hulp van
                een eendje
              </p>
            </div>
          </div>
        </div>
      </div>

      <div
        class="w-[80%] mx-auto flex flex-col md:flex-row items-center justify-between gap-10 py-20"
      >
        <!-- Tekst links -->
        <div class="md:w-1/2 text-white">
          <h2 class="text-4xl font-bold mb-6">Data verzamelen</h2>
          <p class="text-lg text-gray-300 mb-6">
            Op dit moment wordt er onderzoek gedaan naar het vinden van
            bruikbare ruwe data. Daarbij is data gevonden van het Centraal
            Bureau voor de Statistiek (CBS) over rijksmonumenten in Nederland
            (1965-2024). Deze dataset bevat betrouwbare en definitieve cijfers
            en is onderverdeeld naar onder andere provincie, gemeente en type
            monument. Op basis hiervan wordt er specifiek gericht op de
            monumenten in Rotterdam. Door deze te analyseren wordt verwacht dat
            belangrijke inzichten worden gevonden, zoals de verdeling en
            historische ontwikkeling van monumenten, die gebruikt kunnen worden
            als inspiratie en onderbouwing voor het ontwikkelen van de game.
          </p>
        </div>

        <!-- Afbeelding rechts -->
        <div class="md:w-1/2">
          <img
            src="/images/data.png"
            alt="Time Thiefs"
            class="w-full h-[400px] object-cover rounded-3xl shadow-2xl"
          />
        </div>
      </div>
      <div
        class="w-[80%] mx-auto flex flex-col md:flex-row items-center justify-between gap-10 py-20"
      >
        <!-- Afbeelding links -->
        <div class="md:w-1/2">
          <img
            src="/images/image 11.png"
            alt="Time Thiefs"
            class="w-full h-[500px] object-cover rounded-3xl shadow-2xl"
          />
        </div>

        <!-- Tekst rechts -->
        <div class="md:w-1/2 text-white">
          <h2 class="text-4xl font-bold mb-6">Gekozen Monumenten</h2>
          <p class="text-lg text-gray-300 mb-6">
            We hebben een aantal monumenten geselecteerd om te verwerken in ons
            prototype. Hiervoor hebben we een onderzoeksverslag opgesteld en een
            ronde door de stad gelopen om te bepalen welke monumenten het meest
            geschikt zijn voor ons project.<br /><br />
            De verwoeste stad<br />
            De boeg<br />
            Erasmusbeeld<br />
            Monument voor alle gevallenen 1940-1945<br />
            Calandmonument
          </p>
        </div>
      </div>
      <div
        class="w-[80%] mx-auto flex flex-col md:flex-row items-center justify-between gap-10 py-20"
      >
        <!-- Tekst links -->
        <div class="md:w-1/2 text-white">
          <h2 class="text-4xl font-bold mb-6">
            Samenvatting van gesprek met Jan van 360Fabriek
          </h2>
          <p class="text-lg text-gray-300 mb-6">
            Tijdens het gesprek met Jan hebben we besproken hoe we 8th Wall
            kunnen inzetten binnen ons huidige concept, waarin momenteel Cesium
            in de webbrowser wordt gebruikt. Volgens Jan is het mogelijk om een
            bestaande open-source binary te gebruiken als basis en deze verder
            uit te breiden voor onze toepassing.<br /><br />
            Een belangrijk onderdeel van het concept is het gebruik van OUP
            (Open Urban Platform). We kunnen een bestaande informatielaag uit
            OUP ophalen en deze koppelen aan onze applicatie. Daarnaast is het
            mogelijk om zelf een nieuwe laag toe te voegen aan OUP, bijvoorbeeld
            met eigen data of objecten. Voor de dataopslag en koppeling kan
            gebruik worden gemaakt van WFS (Web Feature Service) in combinatie
            met database-hosting. Ook kunnen 3D Tiles worden aangemaakt en
            toegevoegd aan OUP voor visualisatie in een 3D-omgeving.<br /><br />Het
            idee is om per GPS-coördinaat een AR-scene te maken. Wanneer een
            gebruiker zich binnen een bepaalde straal van een locatie bevindt
            (bijvoorbeeld een monument), kan de app automatisch informatie uit
            OUP tonen via augmented reality. Dit kan worden weergegeven met
            AR-teksten die altijd naar de gebruiker gericht zijn (front-facing)
            en eventueel gecombineerd met interactieve elementen.<br /><br />
            Jan liet een experiment zien waarin dit principe al werkt: zodra je
            dicht bij een monument komt, verschijnt relevante informatie uit
            OUP. Hierbij wordt gebruikgemaakt van een 3D viewer, route en
            locatie-gebaseerde visualisatie met camera en AR.<br /><br />
            Voor een proof of concept adviseerde Jan:<br />
            Een vaste route te kiezen.<br />
            Ongeveer 3 tot 5 AR-scenes te maken op specifieke locaties.<br />
            Een interactief element toe te voegen, zoals een trivia of
            multiple-choice vraag.<br />
            De applicatie eventueel zelf te hosten.<br /><br />
            Technisch gezien kunnen we de benodigde componenten ophalen via
            GitHub, inclusief de XR engine en world effects. Belangrijk is dat
            3D-modellen goed geoptimaliseerd zijn (bij voorkeur maximaal 15-20
            MB). Tools zoals Geobase kunnen hierbij helpen.<br /><br />
            Andere technologieën zoals Visual Positioning Systems (zoals
            multiset.ai) bestaan ook, maar zijn momenteel lastig te koppelen en
            voor nu daarom minder relevant.<br /><br />
            Tot slot gaf Jan aan dat het belangrijk is om alles goed te
            documenteren en aandacht te besteden aan codekwaliteit, zodat het
            project later makkelijk verder ontwikkeld kan worden.
          </p>
        </div>

        <!-- Afbeelding rechts -->
        <div class="md:w-1/2">
          <img
            src="/images/8thwall.png"
            alt="Time Thiefs"
            class="w-full h-[400px] object-cover rounded-3xl shadow-2xl"
          />
        </div>
      </div>
    </div>
  </transition>
</template>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: all 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}

.image-container {
  position: relative;
  display: inline-block;
}

.image-text {
  position: absolute;
  bottom: 20px;
  left: 20px;
  color: white;
  font-size: 1.5rem;
  font-weight: bold;
}
</style>
