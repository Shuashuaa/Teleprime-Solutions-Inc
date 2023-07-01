<template>
    <v-app id="inspire">
        <!-- <v-app-bar
			dense
            app
            elevation="0"
            class="mobile-app-bar d-flex d-sm-flex d-md-flex"
        > 
            <v-app-bar-nav-icon class="d-lg-none" id="drawer" @click="drawer = !drawer"></v-app-bar-nav-icon> 
        </v-app-bar>
    
        <v-app-bar
            app
            elevation="0"
            class="d-none d-lg-block d-xl-block"
            color="#efeee5"
        >
            <div style="width: 1000px;"></div>
            <v-icon class="mt-1" style="transform: rotate(150deg);">mdi-timer-sand-empty</v-icon>
            <div style="width: 20000px; color: red;"></div>
            <div
                class="btn"
                v-for="(item, index) in items" :key="index" :to="item.to">
                    <a :href="item.to" style="text-decoration: none; margin-left: 120px;">
                        <p class="list">{{ item.text }}</p>
                    </a>
                    
            </div>        
            <v-btn outlined class="mt-1" elevation="0">
				Contact
            </v-btn>
            <div style="width: 1000px;"></div>
        </v-app-bar>
    
        <v-navigation-drawer 
        disable-resize-watcher
        v-model="drawer" 
        right
        absolute
        class="mobile-drawer"
        app>
            <v-list style="height: 92%;">
                <p class="text-center">components:</p>
                <v-list-item class="btn" v-for="(item, index) in items" :key="index" :to="item.to">
                    <v-list-item-icon>
                    <v-icon>{{ item.icon }}</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title> {{ item.text }} </v-list-item-title>
                </v-list-item>
            </v-list>
            
            <v-list-item>
                <v-list-item-icon>
                    <v-icon>mdi-account</v-icon>
                    </v-list-item-icon>
                <v-list-item-title>Login</v-list-item-title> 
            </v-list-item>

        </v-navigation-drawer> -->
  
        <v-main class="ma-2">
           <router-view></router-view>
        </v-main>
    </v-app>
  </template>
  
  <script>
     export default {
        data: () => ({ 
           drawer: false,
           items:[
              {text:'Home', icon:'mdi-home', to:'/'},
              {text:'Products', icon:'mdi-archive-outline', to:'#products'},
              {text:'Services', icon:'mdi-tools', to:'services'},
              {text:'About us', icon:'mdi-information-outline', to:'about'},
              {text:'Contact', icon:'mdi-phone', to:'contact'},
           ]
        }),
     }
  </script>

<style>
	.v-application .ma-2{
		margin: 0 !important;
	}
    .v-main{
        padding: 50px 0px 0px !important;
    }
    .btn {
        border-radius: 5px;
        font-family: 'Segoe UI';
        font-weight: bold;
    }
    .v-application a{
        color: #3b3e42 !important;
    }
    .list:hover{
        color: green;
    }
    .mobile-drawer{
        width: 100% !important;
    }
    .mobile-app-bar{
        justify-content: end !important;
    }
</style>
