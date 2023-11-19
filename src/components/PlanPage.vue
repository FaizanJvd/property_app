<template>
    <div class="container mx-auto p-4">
        <div class="mb-8">
          <h1 class="text-xl font-bold mb-2 bg-slate-800 p-2 rounded-md text-white"><span class="text-blue-500">{{"Launch PP "}} </span>{{"(Applicable on Launch + 2 Days) "}}<span class="text-white text-sm">Contact for more details</span></h1>
    
          <table class="min-w-full bg-white border border-gray-300 mt-4">
            <thead class="bg-slate-800 text-white ">
              <tr>
                <th class="py-2 px-4 border-b">MileStones</th>
                <th class="py-2 px-4 border-b">Percentage</th>
              </tr>
            </thead>
            <tbody class="bg-emerald-900 text-white text-lg text-center">
              <tr v-for="(data, i) in plan" :key="i">
                <td class="border-grey-light border hover:bg-emerald-500 p-3">{{ data.milestone }}</td>
                <td class="border-grey-light border hover:bg-emerald-500 p-3">{{ data.percentage }}</td>
              </tr>
            </tbody>
          </table>
          <h1 class="text-xl font-bold mb-2 bg-slate-800 p-2 rounded-md text-white">{{"4% DLD will be charged in Initail Deposit."}}<span class="text-blue-500"> Completion Date March 2027</span></h1>
        </div>
      </div>
</template>
<script setup>
const plan = [
    {
        milestone:"Immediate",
        percentage:"20%"
    },
    {
        milestone:"Within 3 to 36 Months of Sale Date",
        percentage:"1%"
    },
    {
        milestone:"On 70% Completion",
        percentage:"2%"
    },
    {
        milestone:"On 80% Completion",
        percentage:"2%"
    },
    {
        milestone:"On 90% Completion",
        percentage:"2%"
    },
    {
        milestone:"On Completion",
        percentage:"40%"
    },
]
</script>