<template>
  <header>
    <label>
      Type:
      <select v-model="filter.type" name="filter" id="filter" >
        <option value="">All</option>
        <option 
          v-for="type in types" 
          v-bind:key="type"
          v-bind:value="type"
        >
        {{ type }}
        </option>
      </select>
    </label>
  </header>  
</template>

<script>
export default {
  props: {
    filter: Object,
    types: Array
  }
};
</script>

<style>
select {
  width: 15%;
}
</style>
