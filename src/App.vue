<template>
  <v-app id="app" >
    <app-navigation></app-navigation>

    <v-container class="mt- mx-auto test" fluid fill-height>
       <v-tabs :right="right" height= 60>
        <v-tab >
          <v-icon left>mdi-view-dashboard</v-icon>
          Dashboard
        </v-tab>
        <v-tab >
        <v-icon>fas fa-edit</v-icon>
           AI
        </v-tab>
         <v-tab-item >
              <v-container fluid fill-height>
                 <iframe src="http://localhost:5601/app/kibana#/dashboard/028f9780-8008-11ea-b349-fd3d6c0e2ff0?embed=true&_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:now-15m,to:now))&_a=(description:'',filters:!(),fullScreenMode:!f,options:(hidePanelTitles:!f,useMargins:!t),panels:!((embeddableConfig:(),gridData:(h:10,i:d80716a9-4cbf-4d47-9581-3288079f8660,w:22,x:0,y:0),id:'47ab15f0-8013-11ea-b349-fd3d6c0e2ff0',panelIndex:d80716a9-4cbf-4d47-9581-3288079f8660,type:visualization,version:'7.6.0'),(embeddableConfig:(),gridData:(h:10,i:'7b466d34-e9c1-4756-bc36-378fc891ccc9',w:26,x:22,y:0),id:'11cfd020-8012-11ea-b349-fd3d6c0e2ff0',panelIndex:'7b466d34-e9c1-4756-bc36-378fc891ccc9',type:visualization,version:'7.6.0'),(embeddableConfig:(hiddenLayers:!(),isLayerTOCOpen:!f,mapCenter:(lat:45.52056,lon:-73.64564,zoom:9.93),openTOCDetails:!()),gridData:(h:22,i:'3b4e0714-00d3-4acb-a49d-853f04bc067c',w:22,x:0,y:10),id:e3d13840-8006-11ea-b349-fd3d6c0e2ff0,panelIndex:'3b4e0714-00d3-4acb-a49d-853f04bc067c',type:map,version:'7.6.0'),(embeddableConfig:(),gridData:(h:22,i:'3af59c35-0c29-43c5-9455-f28b05136561',w:26,x:22,y:10),id:f8eeae10-8042-11ea-b349-fd3d6c0e2ff0,panelIndex:'3af59c35-0c29-43c5-9455-f28b05136561',type:lens,version:'7.6.0'),(embeddableConfig:(),gridData:(h:21,i:'9ba1f549-5109-4b31-80ba-8d24b3963e91',w:17,x:0,y:32),id:'658f2be0-8042-11ea-b349-fd3d6c0e2ff0',panelIndex:'9ba1f549-5109-4b31-80ba-8d24b3963e91',type:lens,version:'7.6.0'),(embeddableConfig:(),gridData:(h:21,i:de606fb9-ce10-4801-b665-a038da6cdd19,w:12,x:17,y:32),id:d64b0680-800e-11ea-b349-fd3d6c0e2ff0,panelIndex:de606fb9-ce10-4801-b665-a038da6cdd19,type:visualization,version:'7.6.0'),(embeddableConfig:(),gridData:(h:21,i:f8558c99-183f-4a56-8b8e-64a2b8381ac3,w:19,x:29,y:32),id:'78d3d260-8023-11ea-b349-fd3d6c0e2ff0',panelIndex:f8558c99-183f-4a56-8b8e-64a2b8381ac3,type:lens,version:'7.6.0')),query:(language:kuery,query:''),timeRestore:!f,title:Airbnb_Dashboard,viewMode:view)" height="1000" width=100%></iframe> 
              </v-container>
        </v-tab-item>
          <v-tab-item >
            <v-container height=100%>
                <HelloWorld/>
            </v-container>
        </v-tab-item >
        </v-tabs>
    </v-container>  

  <v-footer color="teal lighten-3" padless>
    <v-row justify="center" no-gutters >
      <v-btn v-for="link in links" :key="link" color="white" text rounded class="my-2">
        {{ link }}
      </v-btn>
      <v-col class="teal lighten-2 py-4 text-center white--text" cols="12">
        {{ new Date().getFullYear() }} — <strong>© by Bewave</strong>
      </v-col>
    </v-row>
    </v-footer>  
  </v-app>
</template>

<script>


import HelloWorld from './components/HelloWorld';
import AppNavigation from '@/components/AppNavigation';

  export default {
  name: 'App',

  components: {
    AppNavigation,
    HelloWorld,
  },

  data: () => ({
    links: [
        'Home',
        'About Us',
        'Team',
        'Services',
        'Blog',
        'Contact Us',
      ],
  }),
};
</script>

<style>
   #app {
     background-image: url('https://www.technocrazed.com/wp-content/uploads/2015/12/Home-Wallpaper-9.jpg');
     /* background-color: #8f2c2c; */
    height: 100%;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
  }
  .test { opacity: 0.95;

  }
</style>


