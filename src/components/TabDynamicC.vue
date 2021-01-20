<template>
  <div class="container-fluid">
    <button
        v-for="(tab,index) in tabs"
        :key="index"
        :class="['btn', { 'btn-success':currentTab === tab}]"
        @click="currentTab = tab"
    >
      {{ tab }}
    </button>
      <transition name="fade">
        <component :is="currentTabComponent"></component>
      </transition>
  </div>
</template>

<script>
  import TDAlerts1 from "./TDAlerts1.vue";
  import TDAlerts2 from "./TDAlerts2.vue";
  import UserLogin from "./UserLogin.vue";
  export default {
    components:{},
    computed:{
      currentTabComponent(){
        if (this.currentTab === "container") return TDAlerts1;
        else if (this.currentTab === "TDAlerts2") return TDAlerts2;
        else if (this.currentTab === "UserLogin") return  UserLogin;
      },
    },
    data(){
      return{
        currentTab: "container",
        tabs:["container","TDAlerts2","UserLogin"],
      }
    }
  };
</script>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 1s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

</style>