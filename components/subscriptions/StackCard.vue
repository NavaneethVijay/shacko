<template>
  <div
    :class="bgcolor"
    class="w-full rounded-t-lg select-none flex justify-between items-center pt-4 pb-5 px-4 -mt-3 shadow-inner"
  >
    <div class="flex justify-start items-start">
      <div class="w-8 h-8 bg-gray-100 rounded mt-1"></div>
      <div class="ml-4">
        <h4 class="font-medium text-md">{{name}}</h4>
        <p class="text-xs text-light capitalize">{{ type }}</p>
      </div>
    </div>
    <div>
      <p>{{price}}</p>
    </div>
  </div>
</template>
<script>
export default {
  name: 'StackCard',
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
