<template>
   <div class="col-xs-12 col-sm-6">
      <ul class="list-group">
         <Server
            v-for="server in servers"
            :key="server.id"
            :server="server"/>
      </ul>
   </div>
</template>

<script>
import Server from "./Server.vue";

export default {
   data() {
      return {
         servers: [
            { id: 1, status: "Stable" },
            { id: 2, status: "Potato Connection" },
            { id: 3, status: "About to Explode" },
            { id: 4, status: "Will probably Crash..." }
         ]
      };
   },
   components: {
      Server
   }
};
</script>
