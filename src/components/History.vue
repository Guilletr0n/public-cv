<script setup lang="ts">
import { ref } from 'vue'
import companies from "./companies.json";

const word = (<any>companies).name;
const role = (<any>companies).role

</script>
<template>
  <div id="history">
    <ul>
      <li v-for="company in companies" :key="company.id">
        <h5>{{company.name}}</h5>
        <p>{{company.role.en}}</p>
      </li>
    </ul>
  </div>
</template>