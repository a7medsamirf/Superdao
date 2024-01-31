<script setup>
const FeatureData = [
  {
    title: "DeFi",
    subtitle: "Decentralize-governance",
    image: "Icon_defi",
  },
  {
    title: "Investment",
    subtitle: "Scout-and-pick-together",
    image: "Icon_invest",
  },
  {
    title: "Creators",
    subtitle: "Remove-middlemen",
    image: "Icon_creat",
  },
  {
    title: "Metaverse",
    subtitle: "Build-virtual",
    image: "Icon_meta",
  },
  {
    title: "Communities",
    subtitle: "Build-shared",
    image: "Icon_comm",
  },
  {
    title: "Startups",
    subtitle: "Reward-early",
    image: "Icon_startup",
  },
  {
    title: "Nonprofits",
    subtitle: "Raise-funds",
    image: "Icon_nonprof",
  },
  {
    title: "Professionals",
    subtitle: "Form-freelancer",
    image: "Icon_prof",
  },
  {
    title: "Corporations",
    subtitle: "Reinvent-loyalty",
    image: "Icon_Corpor",
  },
];
</script>

<template>
  <section
    id="Features"
    class="py-16 md:py-24 relative after:content-[url('img/Element/Element-3.png')] after:absolute after:z-n1 after:bottom-0 after:left-0"
  >
    <div class="container mx-auto relative">
      <div class="section-title grid grid-cols-1 pb-10 text-center">
        <!-- text - start -->
        <h3
          class="flex justify-center items-center text-2xl md:text-3xl lg:text-4xl font-extrabold text-gray-800 dark:text-white"
        >
          <img
            src="/img/gradient-Bg.png"
            class="img-gradient w-56 lg:w-[400px] absolute z-[-1] block top-7"
            alt=""
          />
          {{ $t("features.SectionTitle") }}
        </h3>
        <!-- text - end -->
      </div>
      <div class="flex justify-center">
        <div class="grid sm:grid-cols-2 xl:grid-cols-3 mt-10 gap-4">
          <!-- feature - start -->
          <div
            class="rounded-lg relative"
            v-for="(feature, index) in FeatureData"
            :key="index"
          >
            <FeatureCard
              :image="feature.image"
              :feature="feature"
              :title="feature.title"
              :subtitle="feature.subtitle"
            />
          </div>
          <!-- feature - end -->
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped></style>
~/public/imgAPI