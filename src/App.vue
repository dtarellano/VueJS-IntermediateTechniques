<template>
   <div class="container">
      <app-header/>
      <hr>
      <div class="row">
         <ServerList :name="name"/>
         <ServerStatus/>
      </div>
      <hr>
      <app-footer/>
    </div>
</template>

<script>
import Header from "./Components/Header.vue";
import Footer from "./Components/Footer.vue";
import ServerList from "./Components/ServerList.vue";
import ServerStatus from "./Components/ServerStatus.vue";

export default {
   components: {
      "app-header": Header,
      ServerList,
      ServerStatus,
      "app-footer": Footer
   }
};
</script>
