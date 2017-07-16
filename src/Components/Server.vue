<template>
   <li class="list-group-item" :style="serverStatus ? stable : warning">
      Server # {{ server.id }} Status: {{ server.status }}
   </li>

</template>

<script>
export default {
   props: ["server"],
   data() {
      return {
         serverStatus: true
      };
   },
   methods: {
      changeStyle() {
         if (server.status !== "Stable") {
            this.serverStatus = false;
         }
      }
   },
   computed: {
      warning() {
         return {
            border: "3px solid red",
            backgroundColor: "pink"
         };
      },
      stable() {
         return {
            border: "3px solid green",
            backgroundColor: "lightgreen"
         };
      }
   }
};
</script>

<style scoped>
   .red {
      border: 3px solid red;
      border-radius: 10px;
      background-color: pink;
      margin-top: 5px;
   }.

   .green {
      border: 3px solid green;
      border-radius: 10px;
      background-color: lightgreen;
      margin-top: 5px;
   }
</style>
