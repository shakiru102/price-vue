<template>
  <div>
    <div class="main">
       <v-container class="">
          <v-layout row wrap>
            <v-flex xs12>
      <div class="head">
        <h1 class=" hidden-xs-only pt-8 text-center">Simple, traffic-based pricing</h1>
        <h2 class=" hidden-sm-and-up pt-8 text-center">Simple, traffic-based pricing</h2>
        <div class="hidden-xs-only  grey--text font-weight-light  text-center">Sign-up for our 30-day trial. No credit card required.</div>
        <div class="hidden-sm-and-up px-10  grey--text  font-weight-light  text-center">Sign-up for our 30-day trial. No credit card required.</div>

      </div>
             
            </v-flex>
            <v-flex xs12>
              <div class="content mt-5">
                 <v-container >
                    <v-row >
                      <v-col align="center">
                        <div class="c">
                        <v-card
                        class="hidden-xs-only"
                        flat
                        width="100%">
                          <v-container
                           class="py-10"
                           >
                            <v-row>
                              <v-col>
                                <div class="pageview grey--text ">{{pageview}} PAGEVIEWS</div>
                              </v-col>
                              <v-col>
                                <div class="price "> <span class="pricetag">${{price}}.00</span> <span class="pricetag2 grey--text"> /month</span></div>

                              </v-col>
                            </v-row>
                            <v-row>
                              <v-col align="center">
                                <input type="range" 
                                :style="`background:linear-gradient(90deg, rgb(16, 213, 194)${percent}%, rgb(234, 238, 251) ${percent}%);`"
                                @change="handleMove"
                                @mousemove="handleMove"
                                
                                  min="1" max="100" class="inp"  id="">
                              </v-col>
                              </v-row>
                            <v-row>
                              <v-col>
                                <div class="pl-16">
                                  <span>
                                  <label class="cap grey--text mr-5" for="swt">Monthly Biling</label>
                                  </span>
                                  <v-switch
                                  
                                  @change="handleChange"
                                  color="rgb(16, 213, 194)"
                                   id="swt" class="switch"  inset v-model="values"></v-switch>
                                  <span class="grey--text"> Yearly Biling</span>
                                  <span class="discount error--text ml-5 caption">25% discount</span>
                                </div>
                              </v-col>
                            </v-row>
                            <v-row>
                                  <v-divider
                                    class="py-2"
                                  ></v-divider>
                            </v-row>
                            <v-row>
                              <v-col>
                                <v-list>
                                  <v-list-item
                                  class="list"
                                   v-for="gif in bonus" :key="gif.title">
                                    <v-list-item-icon>
                                       <div class="list-con">
                                  <img :src="require('../assets/'+gif.image)" alt="">

                                </div>
                                    </v-list-item-icon>
                                    <v-list-item-content>
                                      <div class="label grey--text text-left">
                                   {{gif.title}}
                                </div>
                                    </v-list-item-content>
                                  </v-list-item>
                                </v-list>
                              </v-col>
                              <v-col><div class="py-5">
                                    <v-btn dark x-large rounded color="hsl(227, 35%, 25%)">
                                      Start my trial
                                    </v-btn>
                                
                                </div></v-col>
                            </v-row>
                          </v-container>
                        </v-card>
                        </div>
                        

                <!-- small screen sizes -->
                <div class="c1">
                        <v-card
                        class="hidden-sm-and-up"
                        flat
                        width="100%">
                          <v-container
                           class="py-10"
                           >
                            <v-row>
                              <v-col>
                                <div class="pageview grey--text ">{{pageview}} PAGEVIEWS</div>
                              </v-col>
                            </v-row>
                            <v-row>
                              <v-col align="center">
                                <input type="range" 
                                :style="`background:linear-gradient(90deg, rgb(16, 213, 194)${percent}%, rgb(234, 238, 251) ${percent}%);`"
                                @change="handleMove"
                                @mousemove="handleMove"
                                  min="1" max="100" class="inp"  id="">
                              </v-col>
                              </v-row>
                              <v-row>
                                <v-col>
                                <div class="price "> <span class="pricetag">${{price}}.00</span> <span class="pricetag2 grey--text"> /month</span></div>

                              </v-col>
                              </v-row>
                            <v-row>
                              <v-col>
                                <div class="">
                                  <span>
                                  <label class="cap grey--text mr-3" for="swt">Monthly Biling</label>
                                  </span>
                                  <v-switch
                                  
                                  @change="handleChange"
                                  color="rgb(16, 213, 194)"
                                   id="swt" class="switch"  inset v-model="values"></v-switch>
                                  <span class="grey--text"> Yearly Biling</span>
                                  <span class="discount error--text ml-2 caption">-25%</span>
                                </div>
                              </v-col>
                            </v-row>
                            <v-row>
                                  <v-divider
                                    class="py-2"
                                  ></v-divider>
                            </v-row>
                            <v-row>
                              <v-col>
                                <v-list>
                                  <v-list-item
                                  class="list"
                                   v-for="gif in bonus" :key="gif.title">
                                    <v-list-item-icon>
                                       <div class="list-con">
                                  <img :src="require('../assets/'+gif.image)" alt="">

                                </div>
                                    </v-list-item-icon>
                                    <v-list-item-content>
                                      <div class="label grey--text text-left">
                                   {{gif.title}}
                                </div>
                                    </v-list-item-content>
                                  </v-list-item>
                                </v-list>
                              </v-col>
                              <v-col><div class="py-5">
                                    <v-btn dark x-large rounded color="hsl(227, 35%, 25%)">
                                      Start my trial
                                    </v-btn>
                                
                                </div></v-col>
                            </v-row>
                          </v-container>
                        </v-card>
                        </div>



                      </v-col>
                    </v-row>
                  </v-container>
              </div>

            </v-flex>
          </v-layout>
        </v-container>

    </div>

  </div>
</template>

<script>
export default {
  data:()=>({
    price:24,
    pageview: 500 +'K',
    percent:50,
    values:false,
    bonus:[
      {image:'icon-check.svg', title:'Unlimited websites'},
      {image:'icon-check.svg', title:'100% data ownership'},
      {image:'icon-check.svg', title:'Email reports'},
    ]
  }),
  methods:{
    // handleMoves(e){
    //      this.percent = e.target.value
    

    // },
    handleMove(e){
         this.percent = e.target.value
           if(e.target.value <100 ){
       this.pageview = e.target.value * 10 +'K'
     
      }else if(e.target.value == 100){
        this.pageview = e.target.value / 100 +'M'
      }
       
      if(e.target.value <5 && this.values == false){
        this.price = 8
      } else if( this.percent <5 && this.values == true ){
        let amt = 8 * 0.25
        this.price = 8 - amt

      } else if(e.target.value <10 && this.values == false){
        this.price = 12
      } else if( this.percent <10 && this.values == true ){
        let amt = 12 * 0.25
        this.price = 12 - amt

      }else if(e.target.value <50 && this.values == false){
        this.price = 16
      } else if( this.percent <50 && this.values == true ){
        let amt = 16 * 0.25
        this.price = 16 - amt

      }else if( e.target.value <100 && this.values == false){
        this.price = 24
      } else if( this.percent <100 && this.values == true ){
        let amt = 24 * 0.25
        this.price = 24 - amt

      }else if( e.target.value == 100 && this.values == false){
        this.price = 36
      } else if( this.percent == 100 && this.values == true ){
        let amt = 36 * 0.25
        this.price = 36 - amt

      }

    },
    handleChange(){
      if(this.values == true ){
        let amt = this.price * 0.25
        this.price = this.price - amt

      }
      else if( this.percent <5 && this.values == false){
        this.price = 8
      }else if(this.percent <10 && this.values == false){
        this.price = 12
      }else if(this.percent <50 && this.values == false){
        this.price = 16
      }else if( this.percent <100 && this.values == false){
        this.price = 24
      }else if( this.percent == 100 && this.values == false){
        this.price = 36
      }

    }
    

  }

}
</script>

<style scoped>
/* *{
  font-family: manrope;
} */
.main{
  background: url('../assets/bg-pattern.svg');
  /* background-position: center; */
  background-repeat: no-repeat;
  background-size: contain;
  min-height: 100vh;
  width: 100%;
  padding-top: 4em
}
.head{
  background: url('../assets/pattern-circles.svg');
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
  height: 150px;
}
.price{
  display: flex;
  justify-content: center;
}
.pricetag{
  font-size: 2em;
  /* font-family: roboto; */
  font-weight: bold;
}
.pricetag2{
  align-self: center;
  margin-left: 3px;
  /* font-size: 2em; */
  /* font-family: roboto; */
  /* font-weight: bold; */
}
.inp{
  height: 7px;
  width: 80%;
  appearance: none;
  /* background: linear-gradient(90deg, rgb(16, 213, 194) 50%, rgb(234, 238, 251) 50%); */
  outline: none;
  opacity: 0.7;
  /* appearance: none; */
  border-radius: 30px;
   transition: opacity .2s;
  

}
.inp:hover{
  opacity: 1;
}
.inp::-webkit-slider-thumb{
  appearance: none;
  height: 27px;
  width: 27px;
  border-radius: 50%;
  background: url('../assets/icon-slider.svg');
  background-repeat: no-repeat;
  background-position: center;
  background-color: hsl(174, 86%, 45%);
  box-shadow: 5px 5px 10px hsla(174, 86%, 45%, 0.664);
  cursor: pointer;
}
.v-input.switch{
  display: inline-block
}
span.discount{
  padding: 0.3em 0.8em;
  border-radius: 30px;
  background: rgba(245, 124, 124, 0.288);
}
.list.v-list-item{
 margin: -20px;
}
.list-con{
  /* margin: 0; */
  padding-left: 3em;
}
.c{
  width: 50%;
  box-shadow: 5px 5px 30px rgba(207, 203, 203, 0.575);

}
/* @media screen and (max-width: 600px) {
     .c{
       width: 99%;
  box-shadow: 5px 5px 30px rgba(207, 203, 203, 0.575);
     }
  
} */
.c1{
  margin-bottom: 2em;
  /* width: 100%; */
  box-shadow: 5px 5px 30px rgba(207, 203, 203, 0.575);

}
/* .content{
  display: flex;
  justify-content: center;
  align-content: center;
} */

</style>