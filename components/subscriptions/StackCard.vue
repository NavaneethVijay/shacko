<template>
  <v-expansion-panel>
    <v-expansion-panel-header
      hide-actions
      :class="[bgcolor]"
      class="focus:outline-none cursor-default"
    >
      <div
        :class="[bgcolor]"
        class="w-full stack-card text-white text-left rounded-lg select-none flex justify-between items-center"
      >
        <div class="flex justify-start items-start">
          <div class="w-7 h-7">
            <img class="w-full h-full rounded" :src="logo" alt srcset />
          </div>
          <div class="ml-4">
            <h4 class="font-medium text-md">{{name}}</h4>
            <p class="text-xs text-light capitalize">{{ type }}</p>
          </div>
        </div>
        <div>
          <p>{{price}}</p>
        </div>
      </div>
    </v-expansion-panel-header>
    <v-expansion-panel-content style="color: #fff" :class="bgcolor">
      <div class="flex justify-between">
        <div>
          <h4 class="font-medium text-md">Purchased On</h4>
          <p class="text-xs text-light capitalize">23, Jun 2020</p>
        </div>
        <div>
          <h4 class="font-medium text-md">Next renewal</h4>
          <p class="text-xs text-light text-right capitalize">23, Jun 2020</p>
        </div>
      </div>
      <div class="flex justify-between mt-5">
        <button class>View</button>
        <button class="bg-red-100 px-4 py-1 font-semibold text-sm text-red-700 rounded-lg">Cancel</button>
      </div>
    </v-expansion-panel-content>
  </v-expansion-panel>
</template>
<script>
export default {
  name: 'StackCard',
  props: {
    logo: {
      type: String,
      default: '/subscriptions/netflix.png'
    },
    bgcolor: {
      type: String,
      default: 'bg-black'
    },
     name: {
      type: String,
      default: 'Netflix'
    },
     type: {
      type: String,
      default: 'pro'
    },
    price: {
      type: String,
      default: '$199/m'
    }
  },
}
</script>

