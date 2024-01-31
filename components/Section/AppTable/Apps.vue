<script setup>
 const AppsData = ref([
  {
    title: "Apps.Voting",
    image: "Icon_1",
  },
  {
    title: "Apps.Payroll",
    image: "Icon_2",
  },
  {
    title: "Apps.Treasury",
    image: "Icon_3",
  },
  {
    title: "Apps.Grants",
    image: "Icon_4",
  },
  {
    title: "Apps.Chat",
    image: "Icon_5",
  },
  {
    title: "Apps.Member",
    image: "Icon_6",
  },
  {
    title: "Apps.More",
    image: "Icon_7",
  },
]); 
</script>

<template>
       <div class="section-title inline-flex  items-center text-center">
        <img
            src="/img/svg/Icon_wing.svg"
            class="img-gradient w-10 lg:w-[30px]  "
            alt=""
          />
        <h3 class="flex justify-center items-center text-lg font-semibold text-gray-800 dark:text-primary-color px-4"> 
            {{ $t("Apps.SectionTitle") }}
        </h3>

        </div>

        <div class="flex flex-col justify-center">
        <div class="grid grid-cols-2 md:grid-cols-2 xl:grid-cols-4 mt-10 gap-4">
            <div v-for="(Apps, index) in AppsData" :key="index" class="rounded-lg relative p-4 flex bg-white border border-gray-200  dark:bg-dark dark:border-dark-border">
          

                    <div class=" ">
                    <img class="opacity-70 w-[30px] flex-shrink-0" :src="`/img/Apps/color/${Apps.image}.svg`"/>
                    </div>

                    <div class="ms-3 flex items-center">
                    <h3 class="text-base font-normal text-gray-700 dark:text-gray-400 ">
                   {{ $t(Apps.title) }} 
                    </h3>
                    </div>
          
                </div>
        </div>
        </div>



  

</template>
