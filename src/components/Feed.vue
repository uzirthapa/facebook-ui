<template>
    <v-container grid-list-md>
        <v-layout wrap>
            <v-flex xs12 sm6>
                <v-layout wrap column>
                    <v-flex xs12>
                        <v-card rounded outlined>
                            <v-card-title>
                                <v-layout>
                                    <v-btn text class="questrial font-weight-bold text-none">Make Post</v-btn>
                                    <v-btn text class="questrial text-none">Live Video</v-btn>
                                    <v-btn text class="questrial text-none">List</v-btn>
                                </v-layout>
                            </v-card-title>
                            <div class="px-3">
                                <v-layout>
                                    <v-flex xs12>
                                        <v-text-field class="questrial no-top-padding" background-color="grey lighten-3" height="44px" append-icon="photo_camera sentiment_satisfied" rounded placeholder="What's on your mind, Uzir?">
                                    </v-text-field>
                                    </v-flex>
                                </v-layout>
                            </div>
                        </v-card>
                    </v-flex>
                    <v-flex d-inline-flex xs6>
                        <JeanetteSun/>
                        
                    </v-flex>
                    <v-flex xs12>
                        <MaggieLamb/>
                        
                    </v-flex>
                </v-layout>
            </v-flex>
            <v-flex xs12 sm6>
                <v-layout wrap column>
                    <v-flex xs12>
                        <SadieMarshall/>
                    </v-flex>
                    <v-flex xs12>
                        <LandonWatts/>
                    </v-flex>
                </v-layout>
            </v-flex>
        </v-layout>
    </v-container>
</template>

<script>
import JeanetteSun from './FeedComponents/JeanetteSun'
import SadieMarshall from './FeedComponents/SadieMarshall'
import LandonWatts from './FeedComponents/LandonWatts'
import MaggieLamb from './FeedComponents/MaggieLamb'
export default {
    components: {
        JeanetteSun,
        SadieMarshall,
        LandonWatts,
        MaggieLamb
    }
}
</script>

<style>
@import url("//maxcdn.bootstrapcdn.com/font-awesome/4.1.0/css/font-awesome.min.css");
.search { position: relative; }
.search input { text-indent: 30px;}
.search .fa-search { 
  position: absolute;
  top: 24px;
  left: 7px;
  font-size: 15px;
}
.no-top-padding.v-text-field{
    padding-top: 0!important
}

.v-text-field .v-input__append-inner{
    padding-top: 5px;
}


</style>
