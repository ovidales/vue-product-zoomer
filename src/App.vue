<template>
  <div id="app">
    <v-app id="inspire">
      <v-stepper v-model="e1">
        <v-stepper-header>
          <v-stepper-step :complete="e1 > 1" step="1">Name of step 1</v-stepper-step>

          <v-divider></v-divider>

          <v-stepper-step :complete="e1 > 2" step="2">Name of step 2</v-stepper-step>

          <v-divider></v-divider>

          <v-stepper-step step="3">Name of step 3</v-stepper-step>
        </v-stepper-header>

        <v-stepper-items >
          <v-stepper-content step="1">
            <v-card
              class="mb-5"
              color="grey lighten-1"

            >
              <v-carousel :cycle="false">
                <v-carousel-item v-for="(item,i) in images" :key="i">
                  <div style="width: 40%">
                  <ProductZoomer
                    :nameSpaceOptions="i"
                    :base-images="images"
                    :base-zoomer-options="containerRoundOptions"/>
                  </div>
                </v-carousel-item>
                <!--<v-carousel-item-->
                  <!--v-for="(item,i) in images"-->
                  <!--:key="i"-->
                  <!--:src="item.src"-->
                <!--&gt;</v-carousel-item>-->
              </v-carousel>

            </v-card>

            <v-btn
              color="primary"
              @click="e1 = 2"
            >
              Continue
            </v-btn>

            <v-btn flat>Cancel</v-btn>
          </v-stepper-content>

          <v-stepper-content step="2">
            <v-card
              class="mb-5"
              color="grey lighten-1"
              height="200px"
            ></v-card>

            <v-btn
              color="primary"
              @click="e1 = 3"
            >
              Continue
            </v-btn>

            <v-btn flat>Cancel</v-btn>
          </v-stepper-content>

          <v-stepper-content step="3">
            <v-card
              class="mb-5"
              color="grey lighten-1"
              height="200px"
            ></v-card>

            <v-btn
              color="primary"
              @click="e1 = 1"
            >
              Continue
            </v-btn>

            <v-btn flat>Cancel</v-btn>
          </v-stepper-content>
        </v-stepper-items>
      </v-stepper>
    </v-app>
  </div>
</template>
<script>
  import ProductZoomer from './components/ProductZoomer'
  export default {
    components:{
      ProductZoomer
    },
    data: ()=>({
      e1: 0,
      images: {
        'normal_size': [
          {

            url: 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/1.jpeg'
          },
          {

            url: 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/2.jpeg'
          },
          {

            url: 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/3.jpeg'
          },
          {

            url: 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/4.jpeg'
          },
          {

            url: 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/5.jpeg'
          },
          {

            url: 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/6.jpeg'
          },
          {

            url: 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/7.jpeg'
          },
          {

            'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/8.jpeg'
          },
          {

            url: 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/9.jpeg'
          }
        ],
        'large_size': [
          {

            url: 'http://yoohooworld.com/images/vue_product_zoomer/large_size/1.jpeg'
          },
          {

            url: 'http://yoohooworld.com/images/vue_product_zoomer/large_size/2.jpeg'
          },
          {

            url: 'http://yoohooworld.com/images/vue_product_zoomer/large_size/3.jpeg'
          },
          {

            url: 'http://yoohooworld.com/images/vue_product_zoomer/large_size/4.jpeg'
          },
          {

            url: 'http://yoohooworld.com/images/vue_product_zoomer/large_size/5.jpeg'
          },
          {

            url: 'http://yoohooworld.com/images/vue_product_zoomer/large_size/6.jpeg'
          },
          {

            url: 'http://yoohooworld.com/images/vue_product_zoomer/large_size/7.jpeg'
          },
          {

            url: 'http://yoohooworld.com/images/vue_product_zoomer/large_size/8.jpeg'
          },
          {

            url: 'http://yoohooworld.com/images/vue_product_zoomer/large_size/9.jpeg'
          }
        ]
      },
      'containerRoundOptions': {
        'zoomFactor': 4,
        'pane': 'container-round',
        'hoverDelay': 300,
        'move_by_click':true,
        'scroll_items': 5,
        'choosed_thumb_border_color': "#grey lighten-1"
      }
    })
  }
</script>
