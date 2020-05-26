<template>
  <div class="home">
    <v-data-table
      :headers="headers"
      :items="allData"
      :sort-by="['calories', 'fat']"
      :sort-desc="[false, true]"
      multi-sort
      class="elevation-1"
    ></v-data-table>
  </div>
</template>

<script>
import allData from '../../data.json'

export default {
  name: "Home",
  data() {
    return {
      headers: [
        {
          align: "start",
          sortable: false,
          value: "name"
        },
        { text: "IG Handle", value: "ig_handle" },
        { text: "Squat", value: "squat" },
        { text: "Bench", value: "bench" },
        { text: "Deadlift", value: "deadlift" },
        { text: "Total", value: "total" }
      ],
      allData: allData
    };
  },
  created(){
      console.log(this.desserts)
  }
};
</script>
