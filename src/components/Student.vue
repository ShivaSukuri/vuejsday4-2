<template>
<h1>Student name is : {{myName}} : {{message}}</h1>
<div>
<ul v-for="x in fruits">
<li>{{x}}</li>
</ul>
</div>
</template>
<script setup lang="ts">

defineProps<{
  myName: string
  message?: string
  fruits
}>()
</script>