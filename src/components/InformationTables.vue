<template>
  <div class="container mx-auto p-4">
    <div v-for="(property, index) in data" :key="index" class="mb-8">
      <h1 class="text-xl font-bold mb-2 bg-slate-800 p-2 rounded-md text-white"><span class="text-blue-500">{{"PROJECT_"+(index+1)+": "}} </span>{{ property.title }}</h1>

      <div
        class="flex flex-col items-center w-full bg-slate-100 border border-gray-200 rounded-lg shadow md:flex-row hover:bg-gray-100">
        <video src="../assets/videos/d2.mp4" controls autoplay muted class="h-1/2 w-1/2 rounded-md"/>
        <div class="flex flex-col justify-between p-4 leading-normal">
          <div class="mb-2">
            <p class="text-lg"><strong>Location:</strong> {{ property.Location }}</p>
            <h3 class="text-lg font-bold mb-1">Payment Plan</h3>
            <ul  class="list-disc px-5 text-lg">
              <li  v-for="(payment, i) in property['Payment Plan']" :key="i">{{ payment }}</li>
            </ul>
          </div>
          <div class="mb-2">
            <h3 class="text-lg font-bold mb-1">Features</h3>
            <ul class="list-disc px-5 text-lg">
              <li v-for="(feature, i) in property.Features" :key="i">{{ feature }}</li>
            </ul>
            <p class="text-lg"><strong>Completion Date:</strong> {{ property['Completion Date'] }}</p>
          </div>
        </div>
      </div>

      <table class="min-w-full bg-white border border-gray-300 mt-4">
        <thead class="bg-slate-800 text-white ">
          <tr>
            <th class="py-2 px-4 border-b">Category</th>
            <th class="py-2 px-4 border-b">Starting Price (AED)</th>
            <th class="py-2 px-4 border-b">Starting Area (sqft)</th>
          </tr>
        </thead>
        <tbody class="bg-slate-100 text-center">
          <tr v-for="(detail, i) in property.details" :key="i">
            <td class="border-grey-light border hover:bg-gray-100 p-3">{{ detail.Category }}</td>
            <td class="border-grey-light border hover:bg-gray-100 p-3">{{ detail['Starting Price(AED)'] }}</td>
            <td class="border-grey-light border hover:bg-gray-100 p-3">{{ detail['Starting Area (sqft)'] }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
<script setup>
import { onMounted } from "vue";
import { data } from "../assets/data/data.js"
onMounted(() => {
  console.log(data)
})
</script>
<style>
html,
body {
  height: 100%;
}

@media (min-width: 640px) {
  table {
    display: inline-table !important;
  }

  thead tr:not(:first-child) {
    display: none;
  }
}

td:not(:last-child) {
  border-bottom: 0;
}

th:not(:last-child) {
  border-bottom: 2px solid rgba(0, 0, 0, .1);
}</style>