<script setup>
import * as data from "~/data/data.ts";
</script>

<template>
  <div class="flex flex-col gap-12">
    <!-- Big image -->
    <div class="flex w-full cursor-pointer flex-row">
      <img
        src="/cover.jpg"
        alt="Tin at National Science Museum"
        class="h-full w-full rounded-xl object-cover"
      />
    </div>

    <!-- Title & Subtitle -->
    <section class="flex flex-col items-center gap-2">
      <h1 class="text-center text-5xl md:text-6xl">
        {{ data.about.name.split(" ")[0] }} "{{ data.about.nick }}"
        {{ data.about.name.split(" ")[1] }}
      </h1>
      <h2 class="text-center text-xl italic text-gray-500 md:text-2xl">
        ({{ data.about.aka }})
      </h2>
    </section>

    <!-- About -->
    <article class="text-left text-lg">
      {{ data.about.desc }}
    </article>

    <!-- Personal Info & Connect -->
    <LazyAboutInfoAndConnect :data="data" />

    <!-- Education -->
    <LazyAboutEducation :data="data" />

    <!-- Events -->
    <LazyAboutEvents :data="data" />

    <!-- Projects -->
    <LazyAboutProjects :data="data" />

    <!-- Tech & Interests -->
    <LazyAboutTechAndInterests :data="data" />
  </div>
</template>
