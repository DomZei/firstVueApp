<script setup>
import {reactive, ref} from 'vue';

const person = reactive({
  firstName: "Dominik",
  lastName: "Zeise",
})

function updatePerson(){
  person.firstName = "Elon";
  person.lastName = "Musk";
}

const people = reactive(["Elon Musk", "Marc Zuckerberg"]);

const count = ref(0);

console.log(person)
console.log(count)
function incrementCount(){
  count.value++;
}
</script>

<template>
  <p>Person: {{ person }}</p>
  <button @click="updatePerson">Update Person</button>
  <hr />
  <p>People: {{ people }}</p>
  <hr />
  <p>Count: {{ count }}</p>
  <button @click="incrementCount">Count</button>
</template>

<style scoped>

</style>
