<template>
<div>
<h1>{{foodName}}</h1>
<p>{{desc}}</p>
<button @click="$emit('submit-form',this.foodName)">submit</button>
</div>

</template>
<script setup lang="ts">

defineProps<{
           foodName
           desc
           isFavorite
}>()

defineEmits(["submit-form"])

</script>
<style>
div{
    border:2px solid black;
    margin:5px;
    /* display:grid;
    grid-template-rows:repeat(autofill,minmax(200px,1fr)) */
}
</style>