<template>
  <div>
    <ul>
      <li v-for="person in people" :key="person.Id">
        {{ person.Name }} {{ person.Surname }} - Age: {{ person.Age }}, Country:
        {{ person.Country }}
      </li>
    </ul>
    <button @click="generateRandomNumber">generate</button>
    <ul>
      <li v-for="num in arr" :key="num">{{ num }}</li>
    </ul>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const arr = ref([1])
const generateRandomNumber = () => {
  const randomNumber = Math.floor(Math.random() * 100) + 1
  arr.value.push(randomNumber)
}
const people = [
  {
    Id: 1,
    Name: 'John',
    Surname: 'Doe',
    Age: 30,
    Mail: 'john.doe@example.com',
    Country: 'USA'
  },
  {
    Id: 2,
    Name: 'Alice',
    Surname: 'Smith',
    Age: 25,
    Mail: 'alice.smith@example.com',
    Country: 'Canada'
  },
  {
    Id: 3,
    Name: 'Mohammed',
    Surname: 'Abdullah',
    Age: 40,
    Mail: 'mohammed.abdullah@example.com',
    Country: 'UAE'
  }
]
</script>

<style scoped></style>
