<template>
  <div>
     <div class="selection-gropu">
		<select name="genre" id="" @change="$emit('search', $event.target.value)">
            <option value="all">All</option>
            <option v-for="item, index in list" :key="index">{{item}}</option>
        </select>
		</div>

  </div>
</template>

<script>


export default {
  name: "SelectCard",
  props: {
      list:Array
  }
};
  
</script>

<style  scoped lang="scss">

</style>