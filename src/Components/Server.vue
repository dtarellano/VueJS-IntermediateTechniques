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
