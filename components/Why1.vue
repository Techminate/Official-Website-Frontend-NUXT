<template>
    <v-container fluid>
        <v-row class="">
            <v-col cols="12" sm="12" md="6" lg="6">
                <div class="text-center">
                    <span class="hidden-sm-and-down">
                        <img class="mt-15" src="~/assets/why/why1.png" quality="90" width="620" height="500" fit="fill" />
                    </span>
                </div>
            </v-col>
            <v-col cols="12" sm="12" md="6" lg="5">
                <div class="text-uppercase hidden-sm-and-down">
                    <p class="font-weight-medium text-h5 mt-10">We Increase Business Success With Technology</p>
                    <p class="mt-5">Technology has enabled business owners and leaders to stay on top of their projects by tracking time and progress.</p>
                </div>
                <div class="mt-10">
                    <span v-for="(pro, index) in progress" :key="index">
                        <p>{{ pro.title }}</p>
                        <v-progress-linear :color="pro.color" :buffer-value="pro.buffer" :value="pro.value" stream ></v-progress-linear>
                        <br>
                    </span>
                </div>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
  metaInfo: {
    
  },
  data(){
    return{
      progress:[
        {"title":"Software Development","color":"blue", "buffer":"95", "value":"90"},
        {"title":"Website Development","color":"purple", "buffer":"0", "value":"95"},
        {"title":"UI/UX Design","color":"red", "buffer":"90", "value":"85"},
        {"title":"Cloud & DevOps","color":"green", "buffer":"80", "value":"70"},
        {"title":"Analytic Solutions","color":"orange", "buffer":"95", "value":"85"},
        {"title":"Database Administration","color":"teal", "buffer":"0", "value":"95"}
      ]
    }
  }
}
</script>

<style scoped>

</style>
