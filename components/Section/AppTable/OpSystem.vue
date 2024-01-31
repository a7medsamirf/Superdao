<script setup>
const OpSystemData = ref([
  {
    title: "OpSystem.Ownership",
    subtitle: "OpSystem.promises",
    image: "Icon_ownership",
  },
  {
    title: "OpSystem.Access",
    subtitle: "OpSystem.execution",
    image: "Icon_access",
  },

]);
</script>

<template>

        <div class="section-title inline-flex items-center text-center ">
          <img
            src="/img/svg/Icon_wing.svg"
            class="img-gradient w-10 lg:w-[30px]  "
            alt=""
          />
        <h3 class="flex justify-center items-center text-lg font-semibold text-gray-800 dark:text-primary-color px-4"> 
            {{ $t("OpSystem.SectionTitle") }}
        </h3>
    
        </div>


        <div class="flex flex-col justify-center">
        <div class="grid sm:grid-cols-2 xl:grid-cols-2  gap-4">
          <!-- Creators - start -->
          <div
            v-for="(OpSystem, index) in OpSystemData"
            :key="index"
            class="rounded-lg relative "
          >
          <div class="bg-white border border-gray-200 rounded-lg p-10 dark:bg-dark dark:border-dark-border text-center flex flex-col justify-center">
            <div
              class="text-center mb-4 w-10 h-10 lg:h-12 lg:w-12 flex flex-col justify-center self-center"
            >
            <img :src="`/img/Apps/${OpSystem.image}.svg`"/>
            </div>

            <div class=" text-center">
              <h3 class="text-lg font-semibold text-gray-800 dark:text-primary-color">
                {{ $t(OpSystem.title) }}
              </h3>
              <p
                class="mt-2 text-base font-normal text-gray-700 dark:text-gray-400 w-[250px]"
              >
                {{ $t(OpSystem.subtitle) }}
              </p>
            </div>
          </div>
        </div>
          <!-- Creators - end -->
        </div>
      </div>

</template>
