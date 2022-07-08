<template>
  <div class="container">
		<div class="container_card">
			<ProductCard v-for="element, index in soundList" :key="index" :info="element" />
		</div>
		
  </div>
</template>

<script>
/* eslint-disable */
import ProductCard from "./ProductCard";
import axios from "axios";
export default {
  name: 'MainPage',
  components: {
	ProductCard,
  },
	data() {
		return{
			url: "https://flynn.boolean.careers/exercises/api/array/music",
			soundList: [],		
			}
	},
	created(){
		this.getSound();
	},
	 methods:{
		getSound(){
			axios.get(this.url).then((result)=>{
				this.soundList = result.data.response;
			}
			);
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