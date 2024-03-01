<script>
  import ProductCard from "./ProductCard.svelte";
  import SectionWrapper from "./SectionWrapper.svelte";
  let productFeatures = [
    {
      featureList: [
        "Unlimited access to the gym",
        "Free personal training",
        "Access to all classes",
        "Free access to the pool",
      ],
      description:
        "Get unlimited access to the gym and all its amenities. You also get free personal training and access to all classes and the pool.",
      imgUrl: "assets/selection.png",
    },
    {
      featureList: [
        "Unlimited access to the gym",
        "Free personal training",
        "Access to all classes",
        "Free access to the pool",
      ],
      description:
        "Get unlimited access to the gym and all its amenities. You also get free personal training and access to all classes and the pool.",
      imgUrl: "assets/training.png",
    },
    {
      featureList: [
        "Unlimited access to the gym",
        "Free personal training",
        "Access to all classes",
        "Free access to the pool",
      ],
      description:
        "Get unlimited access to the gym and all its amenities. You also get free personal training and access to all classes and the pool.",
      imgUrl: "assets/goal.png",
    },
  ];
</script>

<SectionWrapper id="project">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24
  flex-1 items-center justify-center pb-10 md:pb-14"
  >
    <div class="flex flex-col gap-2">
      <p
        class="opacity-60 text-base sm:text-lg
      md:text-xl text-center"
      >
        Start your lifetime <span class="text-indigo-400"> gym streak </span> today
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl
      max-w-[1000px] mx-auto w-full font-semibold
      text-center"
      >
        Features for everyone
      </h3>
    </div>

    {#each productFeatures as productFeature, index}
      <ProductCard {productFeature} {index}>
        {#if index === 0}
          Experience the best of the gym <span
            class="text-indigo-400 font-medium"
          >
            world
          </span>
        {:else if index === 1}
          Get the best of the gym <span class="text-indigo-400 font-medium">
            world
          </span>
        {:else}
          Workout specific to your <span class="text-indigo-400 font-medium"
            >environment</span
          >
        {/if}
      </ProductCard>
    {/each}
  </div>
</SectionWrapper>
