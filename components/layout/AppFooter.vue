<script setup>
const SocialData = ref([
  {
    image: "email",
    label: "email",
  },
  {
    image: "instagram",
    label: "instagram",
  },
  {
    image: "twitter",
    label: "twitter",
  },
  {
    image: "facebook",
    label: "facebook",
  },
  {
    image: "linkedin",
    label: "linkedin",
  },
]);
</script>

<template>
  <footer class="bg-gradient-to-r from-[#FFD600] to-[#FFB800]">
    <div class="py-[25px] px-0 border-t border-slate-400">
      <div class="container mx-auto relative">
        <div class="flex justify-around">
          <!-- Grid -->
          <div class="grid grid-cols-1 md:grid-cols-3 items-center gap-5 text-center">
            <div class="text-center flex justify-center md:justify-between">
              <img src="/Logo-Full-Black.png" class="flex-none" alt="" />
            </div>


            <p class="mb-0 text-sm font-semibold text-dark">
              © 2024 Superdao. Development with
              <i class="mdi mdi-heart text-red-600"></i> by
              <a class="text-reset" href="" target="_blank"
                >MedCoder</a
              >.
            </p>

            <!-- Social Brands -->
            <div class="md:text-end">
          
              <NuxtLink
              v-for="(social, index) in SocialData" :key="index"
                target="_blank"
                class="h-8 w-8 mx-1 cursor-pointer inline-flex items-center justify-center tracking-wide align-middle duration-500 text-[15px] text-center border border-gray-800 dark:border-slate-800 rounded-xl hover:border-[#f59e20] dark:hover:border-[#f59e20] hover:bg-[#f59e20] dark:hover:bg-[#f59e20] text-slate-300 hover:text-white"
              >
              <img class="opacity-70" :src="`/img/svg/${social.image}.svg`"/>
          <!--       <img class="opacity-70" :src="require(`/img/svg/${social.image}`)" /> -->
              </NuxtLink>
  
            <!-- End Social Brands -->
          </div>
          <!-- End Grid -->
        </div>
        </div>
      </div>
    </div>
  </footer>
</template>
