<template>
   <div class="container">
      <Header/>
      <hr>
      <div class="row">
         <ServerList/>
         <ServerStatus/>
      </div>
      <hr>
      <Footer/>
    </div>
</template>

<script>
import Header from "./Components/Header.vue";
import Footer from "./Components/Footer.vue";
import ServerList from "./Components/ServerList.vue";
import ServerStatus from "./Components/ServerStatus.vue";

export default {
   components: {
      Header,
      ServerList,
      ServerStatus,
      Footer
   }
};
</script>
