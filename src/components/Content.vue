<template> 
    <div>
        <Divider />
        <v-container :class="[isMobile ? 'content-mobile' : 'content']">
          <img v-if="!isMobile" src="../assets/fish1.png" width="20%" height="30%"/>
          <div :class="[isMobile ? 'text-content-mobile' : 'text-content']">
              <h1>Submersive world</h1>
              <p>Lorem inpsum Lorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsum</p>
              <p>Lorem inpsum Lorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsum</p>
          </div>
          <img v-if="isMobile" src="../assets/fish1.png" width="40%"/>
        </v-container>

        <Divider />

        <v-container :class="[isMobile ? 'content-mobile' : 'content']">
            <div :class="[isMobile ? 'text-content-mobile' : 'text-content']">
              <h1>Amazing Ecology</h1>
              <p>Lorem inpsum Lorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsum Lorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsum</p>
              <p>Lorem inpsum Lorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsum</p>
            </div>
            <img v-if="!isMobile" src="../assets/fish2.png" width="20%" height="30%"/>
            <img v-else src="../assets/fish2.png" width="40%"/>
        </v-container>

        <img src="../assets/Group 15.svg" width="100%"/>

        <div class="title">
            <span>Exists more than you know</span>
        </div>

        <img v-if="isMobile" class="img-water2" src="../assets/water2.svg"> 

        <Carousel :isMobile="isMobile"/>

        <div :class="[isMobile ? 'content-after-footer-mobile' : 'content-after-footer']">
            <div :class="[isMobile ? 'text-content-mobile' : 'text-content']">
            <h1>Never forget it!</h1>
                <p>Lorem inpsum Lorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsum</p>
                <p>Lorem inpsum Lorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsumLorem inpsum</p>
            </div>
            <img src="../assets/water2.svg" class="img-water2 hidden-xs-only" width="50%"/>
        </div>
    </div>
</template>

<script>

import Divider from './Divider';
import Carousel from './Carousel';

export default {
    components: { Divider, Carousel },
    props: { isMobile: Boolean }
}
</script>

<style>
    
  .title {
    margin: 50px 30px 80px;
    color: #fff;
    text-align: center;
  }

  .title span {
    font-size: 2.8rem;
  }

  .content {
    color: #fff;

    display: flex;
    align-items: center;
    justify-content: space-around;
    clear: both;
    
  }

  .content-mobile {
    color: #fff;

    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .text-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 50%;
    text-align: center;
  }

   .text-content-mobile {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
    text-align: center;
  }

  .text-content h1 {
    margin-bottom: 30px;
  }

  .text-content p {
    padding: 0 10px;
  }

  .img-water2 {
    float: right;
    width :70%;
  }

  .content-after-footer {
    padding-top: 50px;
    color: #fff;

    display: flex;
    align-items: center;
    justify-content: space-between;
    clear: both;
    margin-bottom: 200px;
  }

  .content-after-footer .text-content {
      margin-left: 50px;
  }

  .content-after-footer-mobile {
    padding-top: 50px;
    color: #fff;

    display: flex;
    align-items: center;
    justify-content: center;
    clear: both;
    margin-bottom: 200px;
  }

</style>