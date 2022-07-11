<template>
  <div class="container">
		<div>
			<SelectCard   />
		</div>
		<div class="container_card">
			<ProductCard v-for="element, index in filterListDisk" :key="index" :info="element" />
		</div>
		
  </div>
</template>

<script>
/* eslint-disable */
import ProductCard from "./ProductCard";
import axios from "axios";
import SelectCard from "./SelectCard";

export default {
  name: 'MainPage',
  components: {
	ProductCard,
	SelectCard,
  },
 props: {
    details:String
  },
	data() {
		return{
			url: "https://flynn.boolean.careers/exercises/api/array/music",
			soundList: [],	
			listSelect:[],	
			}
	},
	created(){
		this.getSound();
		this.$emit('diskClass', this.listSelect)
	},
	computed:{
		filterListDisk(){
			if(this.details === "all"){
				return this.soundList
			}
			return this.soundList.filter(() =>{
				return item.genere.toLowerCase().includes(this.detalist.toLowerCase())
			},
			)
		},
	},
	 methods:{
		getSound(){
			axios.get(this.url).then((result)=>{
				this.soundList = result.data.response;
				this.allGen();
			}
			);
		}
	 },
	 allGen(){
		for(let i = 0; i < this.soundList.length; i++){
			if(!this.listSelect.push(this.soundList[i].genere)){
				this.listSelect.push(this.soundList[i].genere)
			}
		}
	 }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
	@import  '../style/variables.scss';

	.container{
		width: 100%;
		padding: 0 25%;
		display: flex;
		align-items: center;
	}
		
	.container_card{
		display: flex;
		flex-wrap: wrap;	
		margin-top: 100px;		
	}

</style>