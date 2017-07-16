<template>
   <li class="list-group-item"
       :style="this.server.status === 'Stable' ? stable : warning"
       @click="selectServer">
      Server # {{ server.id }} Status: {{ server.status }}
   </li>

</template>

<script>
import { serverBus } from "../main";

export default {
   props: ["server"],
   methods: {
      selectServer() {
         serverBus.$emit("selectServer", this.server);
      }
   },
   computed: {
      warning() {
         return {
            border: "3px solid red",
            backgroundColor: "pink",
            borderRadius: "10px",
            marginTop: "5px"
         };
      },
      stable() {
         return {
            border: "3px solid green",
            backgroundColor: "lightgreen",
            borderRadius: "10px",
            marginTop: "5px"
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
