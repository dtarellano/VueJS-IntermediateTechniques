<template>
    <div class="col-xs-12 col-sm-6">
        <p v-if="!server">Select a Server</p>
        <p v-else>You have selected Server No. {{server.id}}, its Status is: {{server.status}} </p>
        <hr>
        <button @click="changeToStable">Fix Server</button>
    </div>
</template>

<script>
import { serverBus } from "../main";

export default {
   data() {
      return {
         server: null
      };
   },
   methods: {
      changeToStable() {
         this.server.status = "Stable";
      }
   },
   created() {
      serverBus.$on("selectServer", server => {
         this.server = server;
      });
   }
};
</script>
