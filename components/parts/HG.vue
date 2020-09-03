<template>

    <span class="hg">
        <div class="social">
          <v-row>
            <v-col cols="12">
              <p class="social-text">Follow us</p>
            </v-col>
            <v-col cols="12">
              <v-icon class="social-icon">mdi-instagram</v-icon>
            </v-col>
            <v-col cols="12 zero-padding">
              <v-icon class="social-icon">mdi-twitter</v-icon>
            </v-col>
          </v-row>
        </div>
        <div class="main-content">
            <p class='main-content-preview'>A Hiking guide</p>
            <h1 class="main-content-title">Be prepared for the Mountains and beyond!</h1>
            <v-btn width="17%" class="scroll-text" text color="#fff">
              scroll down <v-icon>mdi-arrow-down</v-icon>
            </v-btn>
        </div>
    </span>
    
</template>


<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Khula&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Bentham&display=swap');
  .hg {
    position: absolute;
    width: 100%;
    height: 111%;
    left: 0;
    top: 0%;
    background: linear-gradient(330.24deg, rgba(11, 29, 38, 0) 31.06%, #0B1D26 108.93%), url('~assets/images/HG.png') no-repeat center center;
    background-size: cover;
    transform: scale(1.1);
  }

  .main-content {
    display: flex;
    flex-direction: column;
    padding: 0px;

    position: absolute;
    width: 50%;
    height: 29%;
    left: 27%;
    top: 28%;
  }

  .main-content-preview {
    font-family: 'Khula', sans-serif;;
    font-style: normal;
    font-weight: 800;
    font-size: 100%;
    line-height: 22px;
    
    letter-spacing: 6px;
    text-transform: uppercase;

    color: #FBD784;
  }

  .main-content-title {
    width: 100%;

    font-family: 'Bentham', serif;
    font-weight: 600;
    font-size: 550%;
    line-height: 100px;

    text-transform: capitalize;

    color: #FFFFFF;

    flex: none;
    align-self: center;
    margin: 0px 32px;
  }

  .scroll-text {
    font-family: 'Khula', sans-serif;
    font-weight: 800;
    font-size: 70%;

    letter-spacing: 6px;
    text-transform: uppercase;

    color: #FFFFFF;
  }

  .social {
    margin-left: 50px;
    position: absolute;
    left: 4%;
    top: 34%;
  }

  .social-text {
    width: 77px;
    height: 22px;
    
    font-family: 'Khula', sans-serif;;
    font-style: normal;
    font-weight: bold;
    font-size: 18px;
    /* identical to box height */


    color: #FFFFFF;

    transform: rotate(90deg);
  }

  .social-icon {
    padding-top: 36px;
    width: 77px;
    height: 22px;
    color: #FFFFFF;
  }

  .zero-padding {
    padding-top: 0;
  }
</style>