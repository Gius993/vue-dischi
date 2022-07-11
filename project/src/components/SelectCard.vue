<template>
  <div>
     <div class="selection-gropu">
		<select v-model="userGenre" @change="$emit('searchGender', userGenre)">
            <option value="All">All</option>
            <option value="Metal">Metal</option>
            <option value="Pop">Pop</option>
            <option value="Rock">Rock</option>
            <option value="Jazz">Jazz</option>
        </select>
		</div>

  </div>
</template>

<script>


export default {
  name: "SelectCard",
//   props: {
//       list:Array
//   },
  data() {
	return {
		userGenre: 'All'
	}
  }
};
  
</script>

<style  scoped lang="scss">

</style>