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
            <v-layout row wrap >
              <v-flex xs12 lg12 xl12>
                <v-card color="white" class="white--text">
                  <v-container  grid-list-lg>
                    <v-layout row>
                      <v-flex xs6 lg6 xl6>
                        <div style="color: black">
                          {{ imageArr }}
                        </div>
                        <v-carousel :cycle="false" >
                          <v-carousel-item v-for="(item, index, key) in imageArr" :key="index"
                                           >
                            k:{{key}}
                            {{`step1_${index}`}}
                            <ProductZoomer
                              :nameSpaceOptions="`step1_${index}`"
                              :base-images="item.images"
                              :base-zoomer-options="item.containerSquareOptions"/>
                          </v-carousel-item>
                        </v-carousel>
                      </v-flex>
                    </v-layout>
                  </v-container>
                </v-card>
              </v-flex>
            </v-layout>
            <v-btn
              color="primary"
              @click="e1 = 2"
            >
              Continue
            </v-btn>
          </v-stepper-content>
          <v-stepper-content step="2">
            <v-layout row wrap >
              <v-flex xs12 lg12 xl12>
                <v-card color="white" class="white--text">
                  <v-container  grid-list-lg>
                    <v-layout row>
                      <v-flex xs6 lg6 xl6>
                        <div style="color: black">
                          {{ imageArr }}
                        </div>
                        <v-carousel :cycle="false">
                          <v-carousel-item v-for="(item, index) in imageArr" :key="index"
                                                    >
                            {{`step${e1}_${index}`}}
                            <ProductZoomer
                              :nameSpaceOptions="`step2_${index}`"
                              :base-images="item.images"
                              :base-zoomer-options="item.containerSquareOptions"/>
                          </v-carousel-item>
                        </v-carousel>
                      </v-flex>
                    </v-layout>
                  </v-container>
                </v-card>
              </v-flex>
            </v-layout>

            <v-btn
              color="primary"
              @click="e1 = 1"
            >
              Regresar
            </v-btn>
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
    computed:{
      imageArr (){
        //Objeto con un elemento raiz, y en cada uno de ellos crea una instancia de un objeto interno
        let arrimg = this.imagesAll;
        let arrFinal = []
        let i = 0;
        for( i=0;i<arrimg.length; i++){
          console.log("element" +arrimg[i]);
          arrFinal.push(
            {
              images: {
                normal_size: [
                  {
                    id:i,
                    url:arrimg[i]
                  }
                ]
              },
              'containerSquareOptions': {
                'zoomFactor': 4,
                'pane': 'container-square',
                // 'namespace': 'inline-zoomer'+i,
                'hoverDelay': 300,
              }
            }
          )
        }
        console.log( "Resultado final" )
        console.log( arrFinal )
        console.log( "Resultado final arreglof" )
        console.log( this.images )
        return arrFinal;
      }
    },
    created(){
      this.activo = 1
      // this.imagesRender = this.imageArr;
      // console.log("images created" )
      // console.log(this.imagesRender)
    },
    data: ()=>({
      e1: 0,
      activo:0,
      imagesRender:[],
      imagesAll:[
        '/src/assets/logo.png',
        'http://yoohooworld.com/images/vue_product_zoomer/normal_size/2.jpeg',
        'http://yoohooworld.com/images/vue_product_zoomer/normal_size/3.jpeg',
      ],
    })
  }
</script>
