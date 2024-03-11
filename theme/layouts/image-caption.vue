<script setup>
const props = defineProps({
  name: {
    type: String,
    required: true
  },
  image: {
    type: String,
    required: true
  },
  imageCaption: {
    type: String,
    required: true
  }
})

</script>
<!-- 
<template>
  <div class="slidev-layout h-full grid image-x">
    <h1 class="text-4xl font-bold p-8">{{ title }}</h1>
    <div class="my-auto flex">
      <div class="w-1/2 flex flex-col justify-center">
        <slot />
      </div>
      <div class="w-1/2 flex justify-center items-center p-8 max-h-md object-cover">
        <img :src="image" class="border-image h-full object-cover" />
        <p class="text-center mt-2">{{ imageCaption }}</p>
      </div>
    </div>
  </div>
</template> -->


<template>
  <div class="slidev-layout grid image-caption">
    <div class="my-auto">
      <h1 class="text-4xl font-bold">{{ name }}</h1>
      <div class="flex flex-grow">
        <div class="w-1/2 flex flex-col justify-center">
          <slot />
        </div>
        <div class="w-1/2 flex flex-col justify-center items-center p-8">
          <img :src="image" border="rounded" class="border-image max-h-md object-cover mb-2" />
          <p class="text-center" v-html="imageCaption"></p>
        </div>
      </div>
    </div>
  </div>
</template>