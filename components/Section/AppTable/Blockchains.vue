<script setup>
 const BlockchainsData = ref([
  {
    title: "Blockchains.Ethereum",
    image: "Icon_ethereum",
  },
  {
    title: "Blockchains.Binance",
    image: "Icon_binance",
  },
  {
    title: "Blockchains.Solana",
    image: "Icon_solana",
  },
  {
    title: "Blockchains.Avalanche",
    image: "Icon_avalanche",
  },
  {
    title: "Blockchains.Terra",
    image: "Icon_Terra",
  },
  {
    title: "Blockchains.NEAR",
    image: "Icon_near",
  },
  {
    title: "Blockchains.Polygon",
    image: "Icon_polygon",
  },
  {
    title: "Blockchains.More",
    image: "Icon_more",
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
            {{ $t("Blockchains.SectionTitle") }}
        </h3>
    
        </div>


        <div class="flex flex-col justify-center">
        <div class="grid grid-cols-2 sm:grid-cols-3 xl:grid-cols-4 gap-4">
            <div v-for="(Blockchains, index) in BlockchainsData" :key="index" class="rounded-lg relative p-4 flex bg-white border border-gray-200 dark:bg-dark dark:border-dark-border">
          

                    <div class=" ">
                    <img class="opacity-70 w-[30px] flex-shrink-0" :src="`/img/Apps/${Blockchains.image}.svg`"/>
                    </div>

                    <div class="ms-3 flex items-center">
                      <h3 class="text-base font-normal text-gray-700 dark:text-gray-400 ">
                   {{ $t(Blockchains.title) }} 
                    </h3>
                    </div>
          
                </div>
        </div>
        </div>

</template>
