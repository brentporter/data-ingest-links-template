<template>
  <h2>Helpful Links</h2>
  <v-row dense class="v-responsive">
    <v-col
        v-for="item in CardInfo"
        :key="item.title"
        cols="12"
        style="width: 100%;"
        class="align-center"
    >
      <v-card elevation="2"
              class="ml-2"
          :subtitle="item.content"
          :title="item.title"

      ><v-card-actions>Application URL <a class="mr-3" style="color: #00acc1" :href="item.url" target="_blank">{{item.title}}</a>
        Code Repo <a class="ml-1" style="color:#00acc1" target="_blank" :href="item.repo">{{item.repo}}</a>
      </v-card-actions></v-card>
    </v-col>
  </v-row>
</template>
<script>
//https://www.the-qrcode-generator.com/
export default {
  name: "ContentList",
  data () {
    return {
      CardInfo:[
        { title:'Metadata Explorer',
          content: "Link to the Metadata Portal",
          url:"https://ms2-dev.tacc.utexas.edu/metadata_app/",
          repo: "https://github.com/In-For-Disaster-Analytics/metadata-portal"
        },
        { title: 'Survey 123 Connect',
          content: 'Data Layer Ingest Test/Demo',
          url: 'https://sitestories.io/survey123/share/a9422e7cdf0240b5848b4d343d154572?portalUrl=https://sitestories.io/portal',
          repo: "NA"
        },
        { title:'REDI CLI Java Ingest',
          content: "Link to GitHub Repo",
          url:"https://github.com/brentporter/chai-s3-datasync/blob/master/README.md",
          repo: "https://github.com/brentporter/chai-s3-datasync"
        },
        {
          title:'Core DB Metadata API',
          content:"API for building out access to CoreDB/Metadata",
          url:"https://ms2-dev.tacc.utexas.edu/redi-api/explorer/",
          repo: "https://github.com/In-For-Disaster-Analytics/metadata-api"
        },
        {
          title: 'Survey Attachment Ingest',
          content: "Survey Attachment Website",
          url:"https://ms2-dev.tacc.utexas.edu/survey-attachments",
          repo: "https://github.com/In-For-Disaster-Analytics/sites-stories-upload"
        },
        { title:'REDI CKAN Client',
          content: "Link to Azure CKAN Instance",
          url:"http://ckan-kmp-setx.eastus.cloudapp.azure.com/",
          repo: "https://github.com/ckan/"
        },
        { title:'Survey123 Main Site',
          content: "Survey Builder Website",
          url:"https://sitestories.io/survey123",
          repo: "NA"
        },
        { title:'REDI GIS Portal',
          content: "Link to the ArcGIS Azure Portal",
          url:"https://sitestories.io/portal/home",
          repo: "NA"
        },
        {
          title:'MinIo Corral',
          content:"MinIO Website",
          url:"https://web.corral.tacc.utexas.edu:9005/",
          repo: "NA"
        }
      ],
      CardContent:[
          "Survey Builder Website https://sitestories.io/survey123",
          "Survey Attachment Website https://sitestories.io/survey123",
          "MinIO Website https://sitestories.io/survey123"
      ]
    }
  }
}
</script>

<style scoped>

</style>