<template>
  <div
    :class="
      i === sectionStore.id
        ? 'collapse collapse-arrow border border-base-300 bg-base-100 rounded collapse-open'
        : 'collapse collapse-arrow border border-base-300 bg-base-100 rounded'
    "
    tabindex="0"
    v-for="(el, i) in sectionData"
    :key="i"
    v-on:click="setDefaultSection(i, el)"
  >
    <div
      :class="
        i === sectionStore.id
          ? 'collapse-title text-xl font-medium bg-[#570df8] text-white'
          : 'collapse-title text-xl font-medium'
      "
    >
      {{ el.title }}
    </div>
    <div class="collapse-content">
      <div class="p-3" v-html="el.content"></div>
    </div>
  </div>
</template>

<script setup>
// Base Imports
import { ref } from 'vue';

// Import Data
import rawSectionData from '../../assets/files/data.json';

// Import Stores
import { useSectionStore } from '../../stores/module/sections';

// Set Datas
const sectionData = ref(rawSectionData);

const sectionStore = useSectionStore();

// Set Functions
const setDefaultSection = (sectionID, section) => {
  sectionStore.setSectionData(sectionID, section);
};
</script>
