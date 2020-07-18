<template>
  <div
    :class="bgcolor"
    class="w-full rounded-lg select-none flex justify-between items-center py-2 px-4 shadow-inner"
  >
    <div class="flex justify-start items-start">
      <div class="w-6 h-6 bg-gray-100 rounded mt-1"></div>
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
