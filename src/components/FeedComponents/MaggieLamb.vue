<template>
    <v-card rounded outlined>
        <div>
            <v-list-item>
                <v-list-item-avatar>
                    <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John">
                </v-list-item-avatar>
                <v-list-item-content class="mt-2">
                    <v-list-item-title class="questrial subtitle">Maggie Lamb</v-list-item-title>
                    <v-list-item-subtitle class="questrial caption indigo--text">Add to Group</v-list-item-subtitle>
                </v-list-item-content>
                <v-list-item-action>
                    <v-icon @click="">more_horiz</v-icon>
                </v-list-item-action>
            </v-list-item>
        </div>
        <v-divider></v-divider>
        <v-card-text>
            <div class="questrial body1 mb-4">{{lorem}}</div>
            <v-divider></v-divider>
            <v-layout class="py-4">

                <v-menu attach open-on-hover top offset-y min-width="200px">
                    <template v-slot:activator="{ on }">
                <v-flex v-on="on" xs4>
                    <v-layout>
                        <v-avatar size="20" class="ml-1">
                            <v-img
                                src="https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/160/facebook/65/blue-heart_1f499.png">
                            </v-img>
                        </v-avatar>
                        <v-avatar size="20" class="ml-1">
                            <v-img
                                src="https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/160/facebook/65/winking-face_1f609.png">
                            </v-img>
                        </v-avatar>
                        <v-avatar size="20" class="ml-1">
                            <v-img
                                src="https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/160/facebook/65/slice-of-pizza_1f355.png">
                            </v-img>
                        </v-avatar>
                        <div class="questrial ml-3"> +26</div>
                    </v-layout>
                </v-flex>
                    </template>
                    <Emojis/>
                </v-menu>
                <v-flex class="text-right">
                    <v-layout wrap justify-end>
                        <div class="questrial mr-3 font-weight-bold ">
                        4 Comments 
                        <v-icon  @click="" small>keyboard_arrow_down</v-icon>
                        <v-icon v-if="false" @click="" small>keyboard_arrow_up</v-icon> 
                    </div> 
                    <div class="questrial ml-2 font-weight-bold mr-2">
                        1 Share
                    </div>
                </v-layout>
                </v-flex>
            </v-layout>
            <v-divider></v-divider>
        </v-card-text>
         <div class="px-4">
                <v-text-field class="questrial" height="45px" background-color="grey lighten-3" append-icon="photo_camera sentiment_satisfied" placeholder="Write a comment..." rounded></v-text-field>
            </div>
    </v-card>
</template>

<script>
import Emojis from '../Emoji/Emojis'
export default {
    components: {
        Emojis
    },
    data(){
        return{
            lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`,
        }
    }
}
</script>

<style>

</style>
