<template>
    <v-card rounded outlined>
        <div>
            <v-list-item>
                <v-list-item-avatar>
                    <img src="https://avatars0.githubusercontent.com/u/9064066?v=4&s=460" alt="John">
                </v-list-item-avatar>
                <v-list-item-content class="mt-2">
                    <v-list-item-title class="questrial subtitle ">Landon Watts</v-list-item-title>
                    <v-list-item-subtitle class="questrial caption blue--text">Friends</v-list-item-subtitle>
                </v-list-item-content>
                <v-list-item-action>
                    <v-icon @click="">more_horiz</v-icon>
                </v-list-item-action>
            </v-list-item>
        </div>
        <v-container fluid grid-list-md>
            <v-layout row wrap>
            <v-flex xs6>
                <v-card color="purple" dark>
                <v-img
                    :src="`https://picsum.photos/500/300?image=${10 * 5 + 10}`"
                    :lazy-src="`https://picsum.photos/10/6?image=${10 * 5 + 10}`"
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
            <v-flex d-flex xs6>
                <v-layout row wrap>
                <v-flex v-for="n in 4" xs6>
                    <v-card color="indigo" dark>
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
            </v-flex>
            </v-layout>
        </v-container>
        <v-card-text>
            <div class="questrial body1 mb-4">{{lorem}}</div>
            <v-divider></v-divider>
            <v-layout class="py-4">
                <v-menu attach open-on-hover top offset-y min-width="200px">
                    <template v-slot:activator="{ on }">
                <v-flex v-on="on">
                    <v-layout>
                        <v-avatar size="20" class="ml-1">
                            <v-img
                                src="https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/160/facebook/65/smiling-face-with-heart-shaped-eyes_1f60d.png">
                            </v-img>
                        </v-avatar>
                        <v-avatar size="20" class="ml-1">
                            <v-img
                                src="https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/160/facebook/65/smiling-cat-face-with-heart-shaped-eyes_1f63b.png">
                            </v-img>
                        </v-avatar>
                        <v-avatar size="20" class="ml-1">
                            <v-img
                                src="https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/160/facebook/65/hamburger_1f354.png">
                            </v-img>
                        </v-avatar>
                        <div class="questrial ml-3"> +8</div>
                    </v-layout>
                </v-flex>
                    </template>
                    <Emojis/>
                </v-menu>
                <v-flex class="text-right">
                    <v-layout wrap justify-end>
                        <div class="questrial mr-3 font-weight-bold ">
                        5 Comments 
                        <v-icon  @click="" small>keyboard_arrow_down</v-icon>
                        <v-icon v-if="false" @click="" small>keyboard_arrow_up</v-icon> 
                    </div> 
                    <div class="questrial ml-2 font-weight-bold mr-2">
                        Share
                    </div>
                </v-layout>
                </v-flex>
            </v-layout>
            <v-divider></v-divider>
        </v-card-text>
        <div class="px-4">
                <v-text-field class="questrial" height="45px" append-icon="photo_camera sentiment_satisfied" background-color="grey lighten-3" placeholder="Write a comment..." rounded></v-text-field>
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
