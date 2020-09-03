<template>
    <div id="app">
        <HG />
        <span class='mg'></span>
        <VG />
        <v-app id="inspire">
            <div>
            <v-app-bar
                color="#ffffff00"
                flat         
                dense
                dark
                height="120px"
            >
        
                <v-toolbar-title class='ml-15 logo'>MNTN</v-toolbar-title>
        
                <v-spacer></v-spacer>
                
                <v-toolbar-title class='mr-4 text-headers'>Equipment</v-toolbar-title>
                <v-toolbar-title class='mx-2 text-headers'>About us</v-toolbar-title>
                <v-toolbar-title class='ml-4 text-headers'>Blog</v-toolbar-title>
            
                
                <v-spacer></v-spacer>
        
                <v-btn text class='text-headers mr-15'>
                <v-icon>mdi-account-circle-outline</v-icon>
                <v-toolbar-title class="text-capitalize pl-1 pt-1">Account</v-toolbar-title>
                </v-btn>
                
            </v-app-bar>
            </div>
        </v-app>
    </div>
</template>

<script>
import HG from '~/components/parts/HG.vue'
import VG from '~/components/parts/VG.vue'
export default {
    components: {
        HG,
        VG
    }
}
</script>


<style>
  @import url('https://fonts.googleapis.com/css2?family=Khula&display=swap');
 
  .mg {
    position: absolute;
    width: 100%;
    height: 131%;
    left: 0px;
    top: 60%;

    background: url('~assets/images/MG.png') no-repeat center center;
    background-size: cover;
    transform: scale(1.1);
  }

  .vg {
    position: absolute;
    width: 100%;
    height: 95%;
    left: 0px;
    top: 84%;

    background: linear-gradient(180deg, rgba(11, 29, 38, 0) 0%, #0B1D26 61.38%), url('~assets/images/VG.png') no-repeat center center;
    background-size: cover;
    transform: scale(1.1);
  }
  
  .logo {
    font-family: Chronicle Display;
    font-size: 32px;
    line-height: 38px;
    letter-spacing: 0.01em;
    text-transform: capitalize;
    
  }
  
  .text-headers {
    font-family: 'Khula', sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 18px;
    line-height: 22px;
  }
 
</style>