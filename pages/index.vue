<template>
  <div class="max-w-md mx-auto px-4 pt-6">
    <header class="mb-6 flex justify-between items-center">
      <div class="flex items-center">
        <img src="/logo.svg" alt srcset />
        <span class="font-bold text-2xl ml-2">Shacko.</span>
      </div>

      <div>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="feather feather-search"
        >
          <circle cx="11" cy="11" r="8" />
          <line x1="21" y1="21" x2="16.65" y2="16.65" />
        </svg>
      </div>
    </header>
    <div class="mb-4">
      <h2 class="text-xl font-medium">Summary</h2>
      <div class="px-4 py-8 rounded-lg mt-4 bg-panel-gray shadow-md">
        <div class="flex">
          <div>
            <p class="text-xs">Monthly Spending</p>
            <h2 class="text-3xl font-semibold">$2,343</h2>
          </div>
        </div>
        <div class="pt-5">
          <client-only>
            <Bar />
          </client-only>
        </div>
      </div>
    </div>
    <div class="mt-8">
      <h2 class="text-xl font-medium">Upcoming payments</h2>
      <div class="py-4">
        <swiper class="swiper" :options="swiperOption">
          <swiper-slide>
            <UpcomingCard />
          </swiper-slide>
          <swiper-slide>
            <UpcomingCard bgcolor="bg-green-600" name="Spotify" type="pro" price="$199/m" />
          </swiper-slide>
        </swiper>
      </div>
    </div>

    <div class="mt-4">
      <h2 class="text-xl font-medium">Active Subscriptions</h2>
      <div class="py-4 mt-2">
        <StackCard />
        <StackCard bgcolor="bg-green-600" name="Spotify" type="pro" price="$199/m" />
        <StackCard bgcolor="bg-pink-600" name="Dribble" type="Professional" price="$119/m" />
        <StackCard bgcolor="bg-blue-900" name="Amazon Prime" type="pro" price="$99/m" />
        <StackCard bgcolor="bg-white text-black" name="Vercel" type="team" price="$1450/m" />
        <StackCard bgcolor="bg-red-900" name="Dribble" type="pro" price="$199/m" />
      </div>
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
export default {
   components: {
      Swiper,
      SwiperSlide
    },
    data() {
      return {
        swiperOption: {
          slidesPerView: 1.3,
          spaceBetween: 30,
        }
      }
    }
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
</style>
