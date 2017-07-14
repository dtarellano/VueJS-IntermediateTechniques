<template>
   <div class="container">
      <app-header></app-header>
      <hr>
      <div class="row">
         <app-servers></app-servers>
         <app-server-details></app-server-details>
      </div>
      <hr>
      <app-footer></app-footer>
    </div>
</template>

<script>
import Header from "./Header.vue";
import Footer from "./Footer.vue";
import ServerList from "./ServerList.vue";
import ServerStatus from "./ServerStatus.vue";

export default {
   components: {
      "app-header": Header,
      "app-servers": ServerList,
      "app-server-details": ServerStatus,
      "app-footer": Footer
   }
};
</script>
