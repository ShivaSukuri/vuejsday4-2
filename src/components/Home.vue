<template>
<!-- <Student my-name="Ram" message="Hello Good Morning"/> -->
<!-- <Teacher name="Shiva Shekhar" designation="Maths professor"/> -->
<!-- <Student :fruits="['banana','apple']" my-name="12"/> -->
<center 
v-for="food of foods"
:food-name=food.name
:desc="food.desc"
:isFavorite="food.favorite"
@submit-form="receiveEmit"/>
</template>
<script setup>
import Student from './Student.vue';
import Teacher from './Teacher.vue';
import center from './center.vue';

 const foods= [
        { name: 'Apples', desc: 'Apples are a type of fruit that grow on trees.', favorite: true},
        { name: 'Pizza', desc: 'Pizza has a bread base with tomato sauce, cheese, and toppings on top.', favorite: false},
        { name: 'Rice', desc: 'Rice is a type of grain that people like to eat.', favorite: false},
        { name: 'Fish', desc: 'Fish is an animal that lives in water.', favorite: true},
        { name: 'Cake', desc: 'Cake is something sweet that tastes good.', favorite: false}
      ]

const receiveEmit=(foodName)=>{
    alert("Hello shiva Today menu"+foodName)
}

</script>
