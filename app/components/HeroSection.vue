<script setup lang="ts">
import type { ButtonProps } from "@nuxt/ui";

const links = ref<ButtonProps[]>([
  {
    label: "Contactez nous",
    to: "/docs/getting-started",
    icon: "i-lucide-square-play",
  },
  {
    label: "Learn more",
    to: "/docs/getting-started/theme/design-system",
    color: "neutral",
    variant: "subtle",
    trailingIcon: "i-lucide-arrow-right",
  },
]);

const items1 = [
  "https://cdn.prod.website-files.com/5b5729421aca332c60585f78/63f5fa23da820b87c87958be_61ba503872080311dde1ea56_long-form-landing-page-examples.png",
  "https://53.fs1.hubspotusercontent-na1.net/hub/53/hubfs/media/LandingpageSproutSocial.jpeg?width=612&height=329&name=LandingpageSproutSocial.jpeg",

  "https://img.freepik.com/free-vector/family-moving-packing-things-landing-page_74855-17269.jpg?semt=ais_hybrid&w=740&q=80",

  "https://img.freepik.com/free-vector/woman-modeling-3d-office-buildings-table-landing-page-template_74855-18090.jpg?semt=ais_hybrid&w=740&q=80",

  "https://img.freepik.com/free-vector/new-landing-page-luxury-background-template_125964-4374.jpg?semt=ais_user_personalization&w=740&q=80",
];

const items2 = [
  "https://cdn.prod.website-files.com/5b5729421aca332c60585f78/63f5fa23da820b87c87958be_61ba503872080311dde1ea56_long-form-landing-page-examples.png",
  "https://53.fs1.hubspotusercontent-na1.net/hub/53/hubfs/media/LandingpageSproutSocial.jpeg?width=612&height=329&name=LandingpageSproutSocial.jpeg",

  "https://img.freepik.com/free-vector/family-moving-packing-things-landing-page_74855-17269.jpg?semt=ais_hybrid&w=740&q=80",

  "https://img.freepik.com/free-vector/woman-modeling-3d-office-buildings-table-landing-page-template_74855-18090.jpg?semt=ais_hybrid&w=740&q=80",

  "https://img.freepik.com/free-vector/new-landing-page-luxury-background-template_125964-4374.jpg?semt=ais_user_personalization&w=740&q=80",
];
</script>

<template>
  <UPageHero
    description="A Nuxt/Vue-integrated UI library providing a rich set of fully-styled, accessible and highly customizable components for building modern web applications."
    headline="Freelance"
    orientation="horizontal"
    class="dark:bg-gradient-to-b from-neutral-900 to-neutral-950"
    :links="links"
    :ui="{ container: 'sm:py-0 lg:py-0' }"
  >
    <template #top>
      <HeroBackground class="z-10" />
    </template>

    <template #title> Développeur Web </template>

    <template #footer>
      <USeparator icon="i-simple-icons-nuxtdotjs" />
      <UPageFeature
        title="Sites vitrines & landings"
        description="Compréhensible, rapide et agréable pour vos visiteurs."
        icon="i-lucide-swatch-book"
        class="my-4"
      />
      <UPageFeature
        title="Interfaces d’applications"
        description="Un site rapide, bien optimisé et parfaitement adapté à tous les écrans"
        icon="i-lucide-swatch-book"
        class="my-4"
      />
      <UPageFeature
        title="Optimisation & SEO"
        description="On avance ensemble, avec des retours courts et une communication simple"
        icon="i-lucide-swatch-book"
        class="my-4"
      />
    </template>
    <template #default>
      <div>
        <div
          class="z-0 h-[344px] lg:h-full lg:relative w-full lg:min-h-[calc(100vh-var(--ui-header-height)-1px)] overflow-hidden"
        >
          <UMarquee
            :repeat="8"
            pause-on-hover
            class="z-10"
            :overlay="false"
            :ui="{
              root: '[--gap:--spacing(4)] [--duration:20s] border-default absolute w-full left-0 border-y lg:border-x lg:border-y-0 lg:w-[calc(50%-6px)] 2xl:w-[320px] lg:flex-col',
              content:
                'lg:w-auto lg:flex-col lg:animate-[marquee-vertical_var(--duration)_linear_infinite] lg:rtl:animate-[marquee-vertical-rtl_var(--duration)_linear_infinite] lg:h-[fit-content]',
            }"
          >
            <div v-for="item in items1">
              <div
                class="relative group/link aspect-video border-default w-[290px] xl:w-[330px] 2xl:w-[320px] 2xl:p-2 2xl:border-y"
              >
                <NuxtImg
                  width="300px"
                  :src="item"
                  alt="Carousel image"
                  class="hover:scale-105 lg:hover:scale-110 transition-transform aspect-video w-full border-x lg:border-x-0 lg:border-y border-default 2xl:border-y-0"
                />
              </div>
            </div>
          </UMarquee>

          <UMarquee
            :repeat="8"
            pause-on-hover
            class="z-10"
            :overlay="false"
            :ui="{
              root: '[--gap:--spacing(4)] [--duration:20s] border-default absolute w-full mt-[180px] left-0 border-y lg:mt-auto lg:left-auto lg:border-y-0 lg:border-x lg:w-[calc(50%-6px)] 2xl:w-[320px] lg:right-0 lg:flex-col',
              content:
                'lg:w-auto lg:flex-col lg:animate-[marquee-vertical_var(--duration)_linear_infinite] lg:rtl:animate-[marquee-vertical-rtl_var(--duration)_linear_infinite] lg:h-[fit-content] lg:[animation-direction:reverse]',
            }"
          >
            <div v-for="item in items2">
              <div
                class="relative group/link aspect-video border-default w-[290px] xl:w-[330px] 2xl:w-[320px] 2xl:p-2 2xl:border-y"
              >
                <NuxtImg
                  width="300px"
                  :src="item"
                  alt="Carousel image"
                  class="hover:scale-105 lg:hover:scale-110 transition-transform aspect-video w-full border-x lg:border-x-0 lg:border-y border-default 2xl:border-y-0"
                />
              </div>
            </div>
          </UMarquee>
        </div>
      </div>
    </template>
  </UPageHero>
</template>
