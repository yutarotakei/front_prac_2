<template>
  <v-app>
    
      <v-navigation-drawer app v-model="drawer" clipped >
        <v-container>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title class="title grey--text text--darken-2">
                Navigation lists
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>


          <v-divider></v-divider>

          <v-list nav dense>
            <v-list-group 
            v-for="nav_list in nav_lists" 
            :key="nav_list.name" 
            :prepend-icon="nav_list.icon" 
            no-action 
            :append-icon="nav_list.lists ? undefined : ''"> 
              <template v-slot:activator>
                <v-list-item-content>
                  <v-list-item-title>{{ nav_list.name }}</v-list-item-title>
                </v-list-item-content>
              </template>
              <v-list-item v-for="list in nav_list.lists" :key="list">
                <v-list-item-content>
                  <v-list-item-title>{{ list }}</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list-group>
          </v-list>
        </v-container>
      </v-navigation-drawer>

    <v-app-bar color="primary" dark app clipped-left>
    <v-app-bar-nav-icon @click="drawer=!drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>英米文学テクスト分析ツール</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items>
      <v-btn text>For Enterprise</v-btn>
      <v-menu offset-y>
        <template v-slot:activator="{on}">
        <v-btn v-on="on" text>For Private<v-icon>mdi-menu-down</v-icon></v-btn>
        </template>

        <v-list>
          <v-subheader>Get help</v-subheader>
            <v-list-item v-for="support in supports" :key="support.name">
              <v-list-item-icon>
              <v-icon>{{ support.icon }}</v-icon>
              </v-list-item-icon>
              <v-list-item-content>
              <v-list-item-title>{{ support.name }}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
        </v-list>


      </v-menu>
    </v-toolbar-items>
    </v-app-bar>

<v-main>
  <router-view />
</v-main>



  <v-footer color="primary" dark app>
      Vuetify
  </v-footer>
  </v-app>
</template>

<script>
export default {
  data(){
    return{
        drawer: null,
        supports:[
          {name: 'Support',icon: 'mdi-vuetify'},
        ],
        nav_lists:[
          {
            name: '英米文学のテクスト分析',
            icon: 'mdi-speedometer',
            lists:[]
          },
        ]
    }
  }
}
</script>