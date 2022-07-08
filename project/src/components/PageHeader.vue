<template>
  <div class="container_my">
		<div class="logo_container">
			<img src="../assets/img/icons8-spotify-48.png" alt="logo">
		</div>
  </div>
</template>

<script>
export default {
  name: 'PageHeader',

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
	@import  '../style/variables.scss';
	.logo_container{
		width: 100px;
	}
	.container_my{
		background-color:$brand_color_a;
		width: 100%;
		color: white;
		font-size: 80px;
		padding: 10px 40px;
	}
</style>