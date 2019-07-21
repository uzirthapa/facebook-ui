<template>
    <v-navigation-drawer color="grey lighten-5" floating right clipped app permanent>
      <v-container>
        <v-card>
          <v-card-title>
            <v-spacer></v-spacer>
            <v-icon>more_horiz</v-icon>
          </v-card-title>
          <v-divider></v-divider>
          <v-list-item>
            <!-- <v-list-item-content> -->
              <v-text-field height="50px" solo flat placeholder="Search" append-icon="search"></v-text-field>
            <!-- </v-list-item-content> -->
          </v-list-item>
          <v-divider></v-divider>
          <v-list-item>
            <v-list-item-content>
              <div class="questrial caption font-weight-bold blue--text">FRIENDS</div>
            </v-list-item-content>
            <v-list-item-action>
              <div class="questrial caption font-weight-bold grey--text" >ADD</div>
            </v-list-item-action>
          </v-list-item>
          <template v-for="item in friends">
            <ChatUser :user="item"/>
          </template>
           <v-divider></v-divider>
          <v-list-item>
            <v-list-item-content>
              <div class="questrial caption font-weight-bold blue--text">COLLEAGUES</div>
            </v-list-item-content>
            <v-list-item-action>
              <div class="questrial caption font-weight-bold grey--text" >ADD</div>
            </v-list-item-action>
          </v-list-item>
          <template v-for="item in colleagues">
            <ChatUser :user="item"/>
          </template>
           <v-divider></v-divider>
          <v-list-item>
            <v-list-item-content>
              <div class="questrial caption font-weight-bold blue--text">CLUBS</div>
            </v-list-item-content>
            <v-list-item-action>
              <div class="questrial caption font-weight-bold grey--text" >ADD</div>
            </v-list-item-action>
          </v-list-item>
          <template v-for="item in clubs">
            <ChatUser :user="item"/>
          </template>

          
        </v-card>
      </v-container>
    </v-navigation-drawer>
</template>

<script>
import ChatUser from '../components/ChatUser/ChatUser'
export default {
  components: {
    ChatUser
  },
  data(){
    return {
      friends: [
        { name: 'Shelton Izaiah', avatar: require('../assets/avatars/1.png'), online: true },
        { name: 'Patrick Solomon', avatar: require('../assets/avatars/2.png'), online: true },
        { name: 'Greer Megan', avatar: require('../assets/avatars/3.png'), online: false },
        { name: 'Merritt Alessandro', avatar: require('../assets/avatars/4.png'), online: true },
        { name: 'Noble Cameron', avatar: require('../assets/avatars/5.png'), online: false },
      ],
      colleagues: [
        { name: 'Small Kaydence', avatar: require('../assets/avatars/6.png'), online: false },
        { name: 'Valenzuela Rudy', avatar: require('../assets/avatars/7.png'), online: false },
        { name: 'Harris Marin', avatar: require('../assets/avatars/8.png'), online: true },
        { name: 'Bailey Kirsten', avatar: require('../assets/avatars/9.png'), online: false },
        { name: 'Rice Wade', avatar: require('../assets/avatars/10.png'), online: true },
      ],
      clubs: [
        { name: 'Chang Zander', avatar: require('../assets/avatars/11.png'), online: true },
        { name: 'Calhoun Kayla', avatar: require('../assets/avatars/12.png'), online: false },
        { name: 'Kramer Riley', avatar: require('../assets/avatars/13.png'), online: true },
        { name: 'Valentine Maci', avatar: require('../assets/avatars/14.png'), online: true },
        { name: 'Malone Terrance', avatar: require('../assets/avatars/15.png'), online: false },
      ]
    }
  }
}
</script>

<style>

</style>
