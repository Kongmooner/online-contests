
<template>
  <v-app>
    <VNavigationDrawer permanent app  width="300">
      <v-row cols="12" justify="center" class="primary">
          <h1 height="100" class="white--text py-5" >Student e-portal</h1>
      </v-row>
        <v-container grid-list-xs>
            <v-col height="fill-height">
                <v-row cols="12" justify="center">
                    <img class="profile elevation-12" src="https://pbs.twimg.com/profile_images/1157994852791050240/wLGN40sL_400x400.jpg" alt="" height="100">
                </v-row>
                <v-row cols="12" justify="center" class="text-sm-center py-2">
                    <h2 class="background--text">{{sName}}</h2>
                </v-row>
                <v-row v-for="item in panes" :key="item.id" cols="12" justify="left" class="text-sm-center py-2" flat>
                      <VBtn text width="100%" ><v-icon small left>{{item.icon}}</v-icon> {{ item.name }}</VBtn>
                </v-row>
            </v-col>
        </v-container>
    </VNavigationDrawer>

    <v-content>
      <router-view class="px-5 pt-2"></router-view>
    </v-content>
  </v-app>
</template>

<script>

export default {
  name: 'App',
  
  components: {
  },

  data: () => ({
    sName: 'Pruthvi Vikram',
    panes: [
      {"name": "Profile", "icon": "mdi-account"},
      {"name": "Grades", "icon": "mdi-account"},
      {"name": "Courses", "icon": "mdi-account"},
      {"name": "Discussion forum", "icon": "mdi-account"},
      {"name": "Logout", "icon": "mdi-account"}
    ]
  }),
};
</script>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Yellowtail&display=swap');

  /* Hide scrollbar for Chrome, Safari and Opera */
  body::-webkit-scrollbar {
    display: none;
  }

  /* Hide scrollbar for IE, Edge and Firefox */
  body {
    -ms-overflow-style: none;  /* IE and Edge */
    scrollbar-width: none;  /* Firefox */
  }

  img.profile{
    border-radius: 100px;
  }
