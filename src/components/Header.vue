<template>
  <header>
    <!-- Filter Component -->
    <label for="type">
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

    <label for="attack">
      Attack:
      <input 
        type="number"
        v-model.number="filter.attack"
        step="10"
      >
    </label>

    <label for="defense">
      Defense:
      <input 
        type="number"
        v-model.number="filter.defense"
        step="10"
      >
    </label>

    <!-- Sort Component -->
    <label for="name">
      Sort By:
      <select v-model="sort.field">
        <option value="type">Type</option>
        <option value="attack">Attack</option>
        <option value="defense">Defense</option>
      </select>
      <select v-model="sort.direction">
        <option value="1">Asc</option>
        <option value="-1">Desc</option>
      </select>
    </label>
  </header>  
</template>

<script>
export default {
  props: {
    filter: Object,
    types: Array,
    sort: Object
  }
};
</script>

<style>
select {
  width: 10%;
}
</style>
