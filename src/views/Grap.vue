<template>
<div><chartjs-bar v-bind:labels="labels" v-bind:datasets="datasets" v-bind:option="option"></chartjs-bar></div>
 
</template>

<script>    
import axios from 'axios'
export default {
    data(){
        return{
            
            labels: [],
            datasets:[{
                data:[],
                backgroundColor:["Red","Bule","yellow","green","black","orange","grey","pink"]
            }],
            option:{
                title:{
                    display:true,
                    position:"bottom",
                    text: "Fruits"
                }
            }
        };
    },
  mounted(){
      var instance = this
      axios
      .get('https://serene-waters-47671.herokuapp.com/api/detail')
      .then(function(response){
for(var i=0;i<response.data.data.length;i++){
    //console.log(response.data.data[i].unit_price)
instance.labels.push(response.data.data[i].category_name)
instance.datasets[0].data.push(response.data.data[i].count)

}
      })
  }
};
</script>