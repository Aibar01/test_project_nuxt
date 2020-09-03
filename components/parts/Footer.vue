<template>
  <v-footer
    
    color="#0B1D26"
    padless
    width='100%'
  >
    <v-container>
        <v-row
        class="mb-0"
        justify="center"
        no-gutters
        >
        <v-col cols="4">
            <h1 class="title-text">MNTN</h1>
            <p class="footer-text">Get out there & discover your next slope, mountain & destination!</p>
        </v-col>
        <v-spacer></v-spacer>
        <v-col cols="5">
            <v-row>
                <v-col cols="6">
                    <p class="mb-4 footer-title">More on The Blog</p>
                    <p class="mb-4 footer-text">About MNTN</p>
                    <p class="mb-4 footer-text">Contributors & Writers</p>
                    <p class="mb-4 footer-text">Write For Us</p>
                    <p class="mb-4 footer-text">Contact Us</p>
                    <p class="mb-4 footer-text">Privacy Policy</p>
                </v-col>
                <v-col class="text-right" cols="6">
                    <p class="mb-4 footer-title">About MNTN</p>
                    <p class="mb-4 footer-text">About MNTN</p>
                    <p class="mb-4 footer-text">About MNTN</p>
                    <p class="mb-4 footer-text">About MNTN</p>
                    <p class="mb-4 footer-text">About MNTN</p>
                    <p class="mb-4 footer-text">About MNTN</p>
                </v-col>
            </v-row>
        </v-col>
        </v-row>
    </v-container>
  </v-footer>
</template>

<script>
  export default {
    
  }
</script>

<style scoped>
  .preview-text {
    margin-top: 80px;
    font-family: 'Khula', sans-serif;
    font-style: normal;
    font-weight: 800;
    font-size: 100%;
    line-height: 22px;
    
    letter-spacing: 6px;
    text-transform: uppercase;

    color: #FBD784;
  }

  .title-text {
    width: 100%;

    padding-top: 30px;
    font-family: 'Bentham', serif;
    font-weight: 600;
    font-size: 250%;
    line-height: 100px;

    text-transform: capitalize;

    color: #FFFFFF;

    flex: none;
    align-self: center;
    margin: 0px 32px;
  }

  .footer-title {
    font-family: 'Khula', sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 32px;
    line-height: 32px;
    /* or 178% */


    color: #FBD784;


    /* Inside Auto Layout */

    flex: none;
    order: 2;
    align-self: center;
    margin: 0px 27px;
  }

  .footer-text {
    font-family: 'Khula', sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 18px;
    line-height: 32px;
    /* or 178% */


    color: #FFFFFF;


    /* Inside Auto Layout */

    flex: none;
    order: 2;
    align-self: center;
    margin: 0px 27px;
  }
</style>