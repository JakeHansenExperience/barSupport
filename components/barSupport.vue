<template>
    <div>
  <v-expansion-panels >
    <v-expansion-panel >
        <v-expansion-panel-header class="purp">
            Bar Audio
        </v-expansion-panel-header>
       
        <v-expansion-panel-content>
            <v-select
            :items="audioOptions"
            variant="outlined"
           
            >

            </v-select>
        </v-expansion-panel-content>
    </v-expansion-panel>

    <v-expansion-panel class="purp">
        <v-expansion-panel-header>
            Bar Volume
        </v-expansion-panel-header>
       
        <v-expansion-panel-content>
            <v-slider
      v-model="audioVolume"
      prepend-icon="mdi-volume-high"
    ></v-slider>
        </v-expansion-panel-content>
    </v-expansion-panel >

    <v-expansion-panel class="purp">
        <v-expansion-panel-header>
            Bar TVs
        </v-expansion-panel-header>
       
        <v-expansion-panel-content>
            <v-container>
                <v-row>
                    <v-col>
                        <v-select
            :items="tvs"
            variant="outlined"
           
            >

            </v-select>
                    </v-col>
                    <v-col>
                        <v-select
            :items="games"
            variant="outlined"
           
            >

            </v-select>
                    </v-col>
                </v-row>
                <v-row>
                    <v-spacer></v-spacer>
                    <v-col>
                        <v-btn> Change Channel</v-btn>
                    </v-col>
                    <v-spacer></v-spacer>
                </v-row>
            </v-container>
        </v-expansion-panel-content>
    </v-expansion-panel>

    <v-expansion-panel class="purp">
        <v-expansion-panel-header>
            LightShows
        </v-expansion-panel-header>
       
        <v-expansion-panel-content>
            <v-select
            :items="lightShows"
            variant="outlined"
           
            >

            </v-select>
        </v-expansion-panel-content>
    </v-expansion-panel>

    <v-expansion-panel class="purp">
        <v-expansion-panel-header>
            Is Bethany Currently Able To Work?
        </v-expansion-panel-header>
       
        <v-expansion-panel-content>
            <v-container>
                <v-row>
                    <v-spacer></v-spacer>
                    <v-col>
                        <v-switch
    v-model="ableToWork"
    hide-details
    true-value="yes"
    false-value="no"
    :label="`${ableToWork}`"
  ></v-switch>
                    </v-col>
                    <v-spacer></v-spacer>
                </v-row>
            </v-container>
            
        </v-expansion-panel-content>
    </v-expansion-panel>
  </v-expansion-panels>

  <v-container>
    <v-row>
        <v-col>
            <v-img
            src="/NeonGolf.png"
            >

            </v-img>
        </v-col>
    </v-row>
  </v-container>
    </div>
    </template>
    
    
    <script>
    
    export default {
      data() {
        return {
            audioOptions: ['Normal Audio', 'Fast Music', 'Astros Game'],
            lightShows: ['Closing Time', 'Flashing Lights'],
            tvs: ['1','2','3','4','5','6','7','8','9','10','11','12','13','14','15','16','17'],
            games: ["Astros vs Mariners", "Rockets vs Heat","Some random high school lacrosse game"],
            audioVolume: 0,
            ableToWork: 'no'
    }
    
    
    },
      props: {
        //the parameters the comopnet accepst
        // message: String,
        // product: Object,
        // email: {
          // type: String
          // required: true,
          // default: 'none'
          // validator: function (value) {
          //   return true if valid
    //       String
    // Number
    // Boolean
    // Array
    // Object
    // Date
    // Function
    // Symbol
          // }
      },
      computed: {
        // fullName: function () {
        //   return this.fistName + ' ' + this.lastName
      },
      watch: {
        //called when firstname changes value
        // firstName: function (value, oldValue) {...}
      },
    
    
      methods: {
    // fetching Data
        // async grabBCData() {
        //   const response = await this.$axios.$get('/api/readAllBusCarts');
        //   this.bcData = response
        //
        //   const startingBay = '202'
        //   this.changeBayParent(startingBay)
        // }
    
    },
    //Lifecycle Hooks: beforeCreate, created, beforeMount, mounted, beforeUPdate, updated, beforeDestroy, destroyed
    // mounted() {
    //   console.log("MountedBaby");
    //   this.grabBCData();
    //
    //   console.log("CalledThatData")
    //
    //
    // }
    
    };
    
    </script>
    
    <style scoped>
    
     /* <v-col class="indigo">
                <v-row>
                  <v-col>
                    <v-icon @click="clickedNum(1)"> mdi-numeric-1-box-outline </v-icon>
                  </v-col>
                  <v-col>
                    <v-icon @click="clickedNum(2)"> mdi-numeric-2-box-outline </v-icon>
                  </v-col>
                  <v-col>
                    <v-icon  @click="clickedNum(3)"> mdi-numeric-3-box-outline </v-icon>
                  </v-col>
                </v-row>
                <v-row>
                  <v-col>
                    <v-icon @click="clickedNum(4)"> mdi-numeric-4-box-outline </v-icon>
                  </v-col>
                  <v-col>
                    <v-icon @click="clickedNum(5)"> mdi-numeric-5-box-outline </v-icon>
                  </v-col>
                  <v-col>
                    <v-icon @click="clickedNum(6)"> mdi-numeric-6-box-outline </v-icon>
                  </v-col>
                </v-row>
                <v-row>
                  <v-col>
                    <v-icon @click="clickedNum(7)"> mdi-numeric-7-box-outline </v-icon>
                  </v-col>
                  <v-col>
                    <v-icon @click="clickedNum(8)"> mdi-numeric-8-box-outline </v-icon>
                  </v-col>
                  <v-col>
                    <v-icon @click="clickedNum(9)"> mdi-numeric-9-box-outline </v-icon>
                  </v-col>
                </v-row>
                <v-row>
                  <v-col>
                    
                  </v-col>
                  <v-col>
                    <v-icon @click="clickedNum(0)"> mdi-numeric-0-box-outline </v-icon>
                  </v-col>
                  <v-col>
                    <v-icon @click="clickedNum('a')"> mdi-backspace-outline</v-icon>
                  </v-col>
                </v-row>
                <v-row>
                  <v-col>
                    <v-text-field v-model="bayNum"  > </v-text-field>
                  </v-col>
                </v-row>
                <v-row>
                  <v-col>
                    <v-btn class="mt-6" @click="runnerUp()">
                      Runner Up!
                    </v-btn>
                  </v-col>
                </v-row>
             
              </v-col> */
    /*
    vuetify styling
    
    ranges from 0-16
    {property} {direction} -{size}
    property is type of spacing, m for margin p for padding
    direction designates the side the property applies to
    t (top)
    b (bottom)
    l (left)
    r (right)
    x (left and right )
    y (top and bottom)
    a (all directions)
    size (1-16)
    1 is 4px, 2 is 8 px, n1 is -4 px or auto
    
    with breakpoints for screen sizes, xs, sm, md, lg, xl
    
    {property}{direction}-{breakpoint}-{size} */
    
    
    </style>
    
    
    
    
    <!-- for axios stuff
    
    new Vue({
      el: '#app',
      data () {
        return {
          info: null
        }
      },
      mounted () {
        axios
          .get('https://api.coindesk.com/v1/bpi/currentprice.json')
          .then(response => (this.info = response))
      }
    }) -->