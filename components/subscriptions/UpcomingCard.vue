<template>
  <div
    :class="bgcolor"
    class="w-full rounded-lg select-none flex justify-between items-center py-2 px-4 shadow-inner"
  >
    <div class="flex justify-start items-start">
      <div class="w-7 h-7 mt-1">
        <img class="w-full h-full rounded" :src="logo" alt srcset />
      </div>
      <div class="ml-4">
        <h4 class="font-medium text-md">{{name}}</h4>
        <p class="text-xs text-light capitalize">23, June</p>
      </div>
    </div>
    <div>
      <p class="text-lg font-medium">{{price}}</p>
    </div>
  </div>
</template>
<script>
export default {
  name: 'UpcomingCard',
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
  }
}
</script>
