<template>
  <label >Day Select (in the format MM/D)</label>
  <input id="selectedDayTextInput" type="text" v-model="selectedDayText" />
  <div v-if="!dayFound">No confidants available for this day</div>
  <div v-if="dayFound">
    Confidants available today:
    <ul class="list list--bare">
      <li v-for="confidant in selectedDay" :key="confidant">
        {{ confidant }}
      </li>
    </ul>
  </div>
</template>

<script>
import data from "@/data/data.json";
import confidantMap from "@/data/confidantMap.json";

export default {
  name: "MainView",

  data() {
    return {
      selectedDayText: "4/19",
      selectedDay: data["4/19"].map((x) => confidantMap[x]),
      dayFound: true,
    };
  },
  watch: {
    selectedDayText(newVal, old) {
      if (newVal in data) {
        this.selectedDay = data[this.selectedDayText].map((x) => confidantMap[x]);
        this.dayFound = true;
      } else {
        this.dayFound = false;
      }
    },
  },
};
</script>
