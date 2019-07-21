<template>
    <v-list-item @click="">
        <v-list-item-avatar>
            <div class="container">
            <v-avatar size="40px">
                <v-img :src="user.avatar" alt="John"></v-img>
            </v-avatar>
            <div class="circle" v-if="user.online" style="top: 25px; left: 2px; position:absolute"></div>
            </div>
        </v-list-item-avatar>

        <v-list-item-content>
            <div class="questrial" style="font-size:16px">{{user.name}}</div>
        </v-list-item-content>
        </v-list-item>
</template>

<script>
export default {
    props: ['user']
}
</script>

<style>
.circle {
  background-color:rgb(32, 204, 26);
  border:2px solid white;
  height:19px;
  border-radius:50%;
  -moz-border-radius:50%;
  -webkit-border-radius:50%;
  width:19px;
  /* position: 'relative'; */
}

.container {
    position: 'fixed';    
}
</style>
