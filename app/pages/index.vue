<template>
    <div>
      <UPageHero
        title="Pacific Coast Spring Break"
        description="A very ambitious week long trip across the incredibly diverse west coast"
        :links="links"
      />
  
      <UPageSection
        title="Trip highlights"
        description="My personal favorite views of the trip"
      >
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-8">
          <div
            v-for="highlight in highlights"
            :key="highlight.title"
            class="rounded-2xl bg-white border border-neutral-200 overflow-hidden"
          >
            <div class="p-6">
              <h3 class="text-lg font-semibold text-neutral-800 mb-1">{{ highlight.title }}</h3>
            </div>
  
            <UMarquee :repeat="1" pause-on-hover>
              <img
                v-for="img in highlight.images"
                :key="img"
                :src="img"
                class="h-24 w-36 object-cover rounded-lg mx-1"
              />
            </UMarquee>
          </div>
        </div>
      </UPageSection>
  
      <UPageCTA
        title="See all the photos"
        description="Browse the full gallery from every stop on the trip."
        :links="ctaLinks"
      />
    </div>
  </template>
  
  <script setup lang="ts">
  const links = [
    { label: 'View photos', to: '/gallery' },
    { label: 'About the trip', to: '/itinerary' },
  ]
  
  const ctaLinks = [
    { label: 'Photo gallery', to: '/gallery' },
    { label: 'Questions?', to: '/contact' },
  ]
  
  const highlights = [
    {
      title: 'Oregon Coast',
      images: [
        '/images/IMG_3721.jpeg',
        '/images/IMG_3725.jpeg',
        '/images/IMG_3726.jpeg',
        '/images/IMG_3731.jpeg',
        '/images/IMG_3733.jpeg',
        '/images/IMG_3734.jpeg',
        '/images/IMG_3721.jpeg',
        '/images/IMG_3725.jpeg',
        '/images/IMG_3726.jpeg',
        '/images/IMG_3731.jpeg',
        '/images/IMG_3733.jpeg',
        '/images/IMG_3734.jpeg',
      ],
    },
    {
      title: 'Point Reyes/San Fransisco',
      images: [
        '/images/IMG_3787.jpeg',
        '/images/IMG_3786.jpeg',
        '/images/IMG_3785.jpeg',
        '/images/IMG_3809.jpeg',
        '/images/IMG_3819.jpeg',
        '/images/IMG_3820.jpeg', 
        '/images/IMG_3787.jpeg',
        '/images/IMG_3786.jpeg',
        '/images/IMG_3785.jpeg',
        '/images/IMG_3809.jpeg',
        '/images/IMG_3819.jpeg',
        '/images/IMG_3820.jpeg',    
      ],
    },
    {
      title: 'Zion National Park',
      images: [
        '/images/IMG_3846.jpeg',
        '/images/IMG_3854.jpeg',
        '/images/IMG_3857.jpeg',
        '/images/IMG_3862.jpeg',
        '/images/IMG_3865.jpeg',
        '/images/IMG_3876.jpeg',
        '/images/IMG_3883.jpeg',
        '/images/61E111E7-577F-44AA-8464-C0AABC1F4FAA.jpg',
        '/images/IMG_3892.jpeg',
        '/images/IMG_3897.jpeg',
        '/images/IMG_3903.jpeg',
        '/images/IMG_3907.jpeg',
      ],
    },
  ]
  </script>