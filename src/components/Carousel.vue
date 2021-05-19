<template>
    <v-container>
    <v-carousel v-if="!isMobile">
    <v-carousel-item  
        v-for="(item, i) in carouse_items"
        :key="i"
    >
        <v-sheet height="100%" color="transparent" tile>
        <v-row class="fill-height flex-direction" align="center" justify="center" >
            <div class="text-carousel">
            <p>Name: {{item.name}}</p>
            <span>Type: <span class="dangerous">{{item.type}}</span></span>
            </div>
            
            <img :src='item.img' width="30%"/>
        </v-row>
        </v-sheet>
    </v-carousel-item>
    </v-carousel>

    <v-carousel v-if="isMobile">
    <v-carousel-item  
        v-for="(item, i) in carouse_items"
        :key="i"
    >
        <v-sheet height="100%" color="transparent">
        <v-row class="fill-height flex-direction-mobile" align="center" justify="center" >
        
            <img :src='item.img' width="50%"/>
            <div class="text-carousel-mobile">
            <p>Name: {{item.name}}</p>
            <span>Type: <span class="dangerous">{{item.type}}</span></span>
            </div>
        </v-row>
        </v-sheet>
    </v-carousel-item>
    </v-carousel>
</v-container>
</template>

<script>
export default {
    props: {isMobile: Boolean},
    data: () => ({
      carouse_items: [
        {
          img: 'slider1.svg',
          name: 'Blighter',
          type: 'Agressive'
        }, {
          img: 'slider2.svg',
          name: 'Crabsquid',
          type: 'Agressive'
        }, {}
      ]
    })
}
</script>

<style>
  .flex-direction {
    flex-direction: row;
  }

  .flex-direction-mobile {
    flex-direction: column;
  }

  .text-carousel {
    display: flex;
    flex-direction: column;
    justify-content:center;
    align-items: center;
    margin-right: 100px;
  }

  .text-carousel-mobile {
    margin-top: 10px;
  }

  .dangerous {
    color: #f00;
    font-weight: bold;
  }

</style>