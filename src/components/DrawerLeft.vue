<template>
    <v-navigation-drawer width="300px" color="grey lighten-5" floating clipped app permanent>
        <v-container>
            <v-card dark color="indigo darken-1" rounded outlined>
                 <v-list-item class="pt-5">
                    <v-list-item-avatar>
                        <img src="https://cdn.quasar.dev/img/boy-avatar.png" alt="John">
                    </v-list-item-avatar>
                    <v-list-item-content class="mt-2">
                        <v-list-item-title class="questrial subtitle">Uzir Thapa</v-list-item-title>
                        <v-list-item-subtitle class="questrial caption">Cedar Rapids, IA</v-list-item-subtitle>
                    </v-list-item-content>
                </v-list-item>
                <v-container>
                    <v-divider style="opacity:0.2" color="white"></v-divider>
                    <v-layout wrap justify-space-around class="py-2">
                        <v-flex xs6 style="text-align: center">
                            <div class="questrial caption font-weight-bold"> 143 Posts</div>
                        </v-flex>
                        <v-flex xs6 style="text-align: center">
                            <div class="questrial caption font-weight-bold"> 1265 Friends</div>
                        </v-flex>
                    </v-layout>
                    
                    <v-divider style="opacity:0.2" color="white"></v-divider>
                </v-container>
                
                <v-list dense >
                    
                    <v-list-item-group v-model="item" active-class="active-list-item">
                        <v-subheader class="questrial font-weight-bold ml-5">FEED</v-subheader>
                         <v-list-item @click="" v-for="item in items" dense style="height:20px" >
                            <v-list-item-action>
                                <v-icon color="grey lighten-3">{{item.icon}}</v-icon>
                            </v-list-item-action>
                            <v-list-item-content>
                                <!-- <div v-if="n">
                                    <v-list-item-title class="questrial body1 font-weight-bold">{{item.text}}</v-list-item-title>
                                </div> -->
                                
                                <v-list-item-title class="questrial body1">{{item.text}}</v-list-item-title>
                            </v-list-item-content>
                        </v-list-item>
                    </v-list-item-group>
                </v-list>
            </v-card>
            <v-card class="mt-3" rounded outlined>
                <v-card-title class="mb-2">
                    <div class="questrial body-2 font-weight-bold">News</div>
                    <v-spacer></v-spacer>
                    <v-icon @click="" small>more_horiz</v-icon>
                </v-card-title>
                <v-divider></v-divider>
                <v-list-item dense>   
                    <v-list-item-icon>
                        <v-icon>video_call</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                        <div class="questrial caption text--grey">There is a meetup in your city on Friday at 8:45pm. <div class="indigo--text font-weight-bold"> See Details</div></div>
                    </v-list-item-content>
                </v-list-item>
                <v-list-item dense>   
                    <v-list-item-icon>
                        <v-icon>video_call</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                        <div class="questrial caption text--grey">20% off coupons at Pharmaprix</div>
                    </v-list-item-content>
                </v-list-item>
            </v-card>
            <v-card class="mt-2" rounded outlined>
               <v-card-title class="mb-2">
                    <div class="questrial body-2 font-weight-bold">Gallery</div>
                    <div class="questrial caption font-weight-bold ml-4 grey--text text--darken-1">132 Pics</div>
                    <v-spacer></v-spacer>
                    <v-icon @click="" small>more_horiz</v-icon>
                </v-card-title>
                <v-container grid-list-xs fluid style="padding:0">
          <v-layout row wrap>
            <v-flex
              v-for="n in 9"
              :key="n"
              xs4
            >
              <v-card flat tile>
                <v-img
                  :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
                  :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
                  aspect-ratio="1"
                  class="grey lighten-2"
                >
                  <template v-slot:placeholder>
                    <v-layout
                      fill-height
                      align-center
                      justify-center
                      ma-0
                    >
                      <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                    </v-layout>
                  </template>
                </v-img>
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
            </v-card>   
        </v-container>
    </v-navigation-drawer>
</template>

<script>
export default {
    data(){
        return {
            item: 1,
            items: [
                {text: 'News Feed', icon: 'assignment'},
                {text: 'Pages', icon: 'fa-comments'},
                {text: 'Pages Feed', icon: 'fa-briefcase'},
                {text: 'Events', icon: 'event'},
                {text: 'Saved', icon: 'bookmark'},
                {text: 'Reccomendations', icon: 'store'},
                {text: 'Memories', icon: 'fa-gamepad'},

            ]
        }
    }
}
</script>

<style>
.active-list-item .v-list-item--dense .v-list-item__title, .v-list-item--dense .v-list-item__subtitle, .v-list--dense .v-list-item .v-list-item__title, .v-list--dense .v-list-item .v-list-item__subtitle {
    font-family: 'Questrial';
    font-weight: 'bold';
}
</style>
