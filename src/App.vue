<template>
  <main>
    <div>
      <div style="width: 400px">
        <ProductZoomer
          :base-images="images"
          :base-zoomer-options="containerRoundOptions"
        />
      </div>
    </div>
  </main>
</template>

<script>
  import ProductZoomer from './components/ProductZoomer'

  export default {
    name: 'app',
    data () {
      return {
        images: {
          thumbs: [
            {
              'id': 1,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/1.jpeg'
            },
            {
              'id': 2,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/2.jpeg'
            },
            {
              'id': 3,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/3.jpeg'
            },
            {
              'id': 4,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/4.jpeg'
            },
            {
              'id': 5,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/5.jpeg'
            },
            {
              'id': 6,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/6.jpeg'
            },
            {
              'id': 7,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/7.jpeg'
            },
            {
              'id': 8,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/8.jpeg'
            },
            {
              'id': 9,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/9.jpeg'
            }
          ],
          'normal_size': [
            {
              'id': 1,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/1.jpeg'
            },
            {
              'id': 2,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/2.jpeg'
            },
            {
              'id': 3,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/3.jpeg'
            },
            {
              'id': 4,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/4.jpeg'
            },
            {
              'id': 5,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/5.jpeg'
            },
            {
              'id': 6,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/6.jpeg'
            },
            {
              'id': 7,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/7.jpeg'
            },
            {
              'id': 8,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/8.jpeg'
            },
            {
              'id': 9,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/9.jpeg'
            }
          ],
          'large_size': [
            {
              'id': 1,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/1.jpeg'
            },
            {
              'id': 2,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/2.jpeg'
            },
            {
              'id': 3,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/3.jpeg'
            },
            {
              'id': 4,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/4.jpeg'
            },
            {
              'id': 5,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/5.jpeg'
            },
            {
              'id': 6,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/6.jpeg'
            },
            {
              'id': 7,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/7.jpeg'
            },
            {
              'id': 8,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/8.jpeg'
            },
            {
              'id': 9,
              'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/9.jpeg'
            }
          ]
        },
        'zoomerOptions': {
          'zoomFactor': 3,
          'pane': 'pane',
          'hoverDelay': 300,
          'namespace': 'zoomer',
          'move_by_click':false,
          'scroll_items': 7,
          'choosed_thumb_border_color': "#dd2c00"
        },
        'containerRoundOptions': {
          'zoomFactor': 4,
          'pane': 'container-round',
          'hoverDelay': 300,
          'namespace': 'inline-zoomer',
          'move_by_click':true,
          'scroll_items': 5,
          'choosed_thumb_border_color': "#bbdefb"
        },
        'containerOptions': {
          'zoomFactor': 4,
          'pane': 'container',
          'hoverDelay': 300,
          'namespace': 'container-zoomer',
          'move_by_click':true,
          'scroll_items': 4,
        }
      }
    },
    components: {
      ProductZoomer
    }
  }
</script>



<!--<template>-->
  <!--<div id="app">-->
    <!--<v-app id="inspire">-->
      <!--<v-stepper v-model="e1">-->
        <!--<v-stepper-header>-->
          <!--<v-stepper-step :complete="e1 > 1" step="1">Name of step 1</v-stepper-step>-->

          <!--<v-divider></v-divider>-->

          <!--<v-stepper-step :complete="e1 > 2" step="2">Name of step 2</v-stepper-step>-->

          <!--<v-divider></v-divider>-->

          <!--<v-stepper-step step="3">Name of step 3</v-stepper-step>-->
        <!--</v-stepper-header>-->

        <!--<v-stepper-items >-->
          <!--<v-stepper-content step="1">-->
            <!--<div style="width: 50%">-->
              <!--<ProductZoomer-->
                <!--:base-images="images"-->
                <!--:base-zoomer-options="zoomerOptions"-->
              <!--/>-->
            <!--</div>-->

            <!--<v-btn-->
              <!--color="primary"-->
              <!--@click="e1 = 2"-->
            <!--&gt;-->
              <!--Continue-->
            <!--</v-btn>-->

            <!--<v-btn flat>Cancel</v-btn>-->
          <!--</v-stepper-content>-->

          <!--<v-stepper-content step="2">-->
            <!--<v-card-->
              <!--class="mb-5"-->
              <!--color="grey lighten-1"-->
              <!--height="200px"-->
            <!--&gt;</v-card>-->

            <!--<v-btn-->
              <!--color="primary"-->
              <!--@click="e1 = 3"-->
            <!--&gt;-->
              <!--Continue-->
            <!--</v-btn>-->

            <!--<v-btn flat>Cancel</v-btn>-->
          <!--</v-stepper-content>-->

          <!--<v-stepper-content step="3">-->
            <!--<v-card-->
              <!--class="mb-5"-->
              <!--color="grey lighten-1"-->
              <!--height="200px"-->
            <!--&gt;</v-card>-->

            <!--<v-btn-->
              <!--color="primary"-->
              <!--@click="e1 = 1"-->
            <!--&gt;-->
              <!--Continue-->
            <!--</v-btn>-->

            <!--<v-btn flat>Cancel</v-btn>-->
          <!--</v-stepper-content>-->
        <!--</v-stepper-items>-->
      <!--</v-stepper>-->
    <!--</v-app>-->
  <!--</div>-->
<!--</template>-->
<!--<script>-->
  <!--import ProductZoomer from './components/ProductZoomer'-->
  <!--export default {-->
    <!--components:{-->
      <!--ProductZoomer-->
    <!--},-->
    <!--data: ()=>({-->
      <!--e1: 0,-->
      <!--images: {-->
        <!--thumbs: [-->
          <!--{-->
            <!--'id': 1,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/1.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 2,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/2.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 3,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/3.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 4,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/4.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 5,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/5.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 6,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/6.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 7,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/7.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 8,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/8.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 9,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/thumbs/9.jpeg'-->
          <!--}-->
        <!--],-->
        <!--'normal_size': [-->
          <!--{-->
            <!--'id': 1,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/1.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 2,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/2.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 3,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/3.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 4,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/4.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 5,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/5.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 6,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/6.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 7,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/7.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 8,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/8.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 9,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/normal_size/9.jpeg'-->
          <!--}-->
        <!--],-->
        <!--'large_size': [-->
          <!--{-->
            <!--'id': 1,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/1.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 2,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/2.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 3,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/3.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 4,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/4.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 5,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/5.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 6,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/6.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 7,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/7.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 8,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/8.jpeg'-->
          <!--},-->
          <!--{-->
            <!--'id': 9,-->
            <!--'url': 'http://yoohooworld.com/images/vue_product_zoomer/large_size/9.jpeg'-->
          <!--}-->
        <!--]-->
      <!--},-->
      <!--'containerRoundOptions': {-->
        <!--'zoomFactor': 4,-->
        <!--'pane': 'container-round',-->
        <!--'hoverDelay': 300,-->
        <!--'namespace': 'inline-zoomer',-->
        <!--'move_by_click':true,-->
        <!--'scroll_items': 5,-->
        <!--'choosed_thumb_border_color': "#bbdefb"-->
      <!--},-->
    <!--})-->
  <!--}-->
<!--</script>-->
