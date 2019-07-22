<template>
    <v-card rounded outlined>
        <div>
            <v-list-item>
                <v-list-item-avatar>
                    <img src="https://cdn.quasar.dev/img/avatar.png" alt="John">
                </v-list-item-avatar>
                <v-list-item-content class="mt-2">
                    <v-list-item-title class="questrial subtitle">Sadie Marshall</v-list-item-title>
                    <v-list-item-subtitle class="questrial caption indigo--text">Friends</v-list-item-subtitle>
                </v-list-item-content>
                <v-list-item-action>
                    <v-icon @click="">more_horiz</v-icon>
                </v-list-item-action>
            </v-list-item>
        </div>
        <!-- <v-container grid-list-xs fluid style="padding:10px"> -->
            <v-layout wrap>
                <v-flex xs12>
                    <v-card flat tile>
                        <v-img
                        :src="`https://picsum.photos/500/300?image=${12 * 5 + 10}`"
                        :lazy-src="`https://picsum.photos/10/6?image=${12 * 5 + 10}`"
                        aspect-ratio="2"
                        class="grey lighten-2"
                        gradient="to top right, rgba(0,0,0,.2), rgba(0,0,0,.2)"
                        >
                            <v-layout
                            fill-height
                            align-center
                            justify-center
                            ma-0
                            >
                                <v-btn icon>
                                    <v-icon color="grey lighten-3"  large>play_circle_outline</v-icon>
                                </v-btn>
                                    
                            </v-layout>
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
            <v-card-title>
                <div class="questrial font-weight-bold" style="font-size: 17px">Best Jogging Tips For Better Health And Fitness</div>
            </v-card-title>
            <v-card-text>
            <div class="questrial body1 mb-4">{{lorem}}</div>
            <v-divider></v-divider>
            <v-layout class="py-4">
            <v-menu open-on-hover top offset-y min-width="200px">
                    <template v-slot:activator="{ on }">
                <v-flex v-on="on">
                    <v-layout>
                        <v-avatar size="20" class="ml-1">
                            <v-img
                                src="https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/160/facebook/65/smiling-face-with-sunglasses_1f60e.png">
                            </v-img>
                        </v-avatar>
                        <v-avatar size="20" class="ml-1">
                            <v-img
                                src="https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/160/facebook/65/grinning-face_1f600.png">
                            </v-img>
                        </v-avatar>
                        <v-avatar size="20" class="ml-1">
                            <v-img
                                src="https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/160/facebook/65/runner_emoji-modifier-fitzpatrick-type-1-2_1f3c3-1f3fb_1f3fb.png">
                            </v-img>
                        </v-avatar>
                        <div class="questrial ml-3"> +98</div>
                    </v-layout>
                </v-flex>
                </template>
                <Emojis/>
            </v-menu>
                <v-flex class="text-right">
                    <v-layout wrap justify-end>
                        <div class="questrial mr-3 font-weight-bold ">
                        28 Comments 
                        <v-icon  @click="" small>keyboard_arrow_down</v-icon>
                        <v-icon v-if="false" @click="" small>keyboard_arrow_up</v-icon> 
                    </div> 
                    <div class="questrial ml-2 font-weight-bold mr-2">
                        3 Share
                    </div>
                </v-layout>
                </v-flex>
            </v-layout>
            <v-divider></v-divider>
            
        </v-card-text>
         <div class="px-4">
                <v-text-field class="questrial" height="45px" append-icon="photo_camera sentiment_satisfied" background-color="grey lighten-3" placeholder="Write a comment..." rounded></v-text-field>
            </div>
        <!-- </v-container> -->
    </v-card>
</template>

<script>
import Emojis from '../Emoji/Emojis'
export default {
    components:{
        Emojis,
    },
    data(){
        return {
            lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`,
        }
    }
}
</script>

<style>
.v-menu__content{
    border-radius: 25px
}
</style>
