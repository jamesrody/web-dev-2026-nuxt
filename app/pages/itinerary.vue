<template>
  <div>
    <UPageHeader
      title="The Itinerary"
      description="The beauty of the west coast"
    />

    <UPageBody class="-mt-35">
      <UPageSection>
        <div class="mt-6 space-y-4">
          <div
            v-for="day in itinerary"
            :key="day.label"
            class="flex gap-6 p-5 rounded-2xl bg-white border border-neutral-200 transition-transform duration-300 hover:scale-101"
          >
            <img :src="day.image" :alt="day.title" class="w-40 h-40 rounded-xl object-cover shrink-0" />
            <div>
              <div class="text-xs font-semibold text-primary uppercase tracking-widest mb-1">{{ day.label }}</div>
              <h3 class="text-base font-semibold text-neutral-800 mb-1">{{ day.title }}</h3>
              <p class="text-sm text-neutral-500 leading-relaxed">{{ day.description }}</p>
            </div>
          </div>
        </div>
      </UPageSection>
    </UPageBody>
  </div>
</template>

<script setup lang="ts">
const itinerary = [
  {
    image: '/images/IMG_3732.jpeg',
    label: 'Day 1',
    title: 'Seattle -> Oregon Coast -> California',
    description: 'Left Seattle and drove towards highway 101, hitting the Oregon coast around noon. First glimpse of the Pacific and the start of Highway 101. Ended the day at the very tip of California',
  },
  {
    image: '/images/IMG_3764.JPG',
    label: 'Day 2',
    title: 'Redwoods -> Point Reyes',
    description: 'From 101 through the redwoods and NorCal to 1 along the coast down to Point Reyes National Seashore. The most fun driving day by far, at least for me.',
  },
  {
    image: '/images/IMG_3809.jpeg',
    label: 'Day 3',
    title: 'Point Reyes -> San Fransisco -> Big Sur',
    description: 'Drove into and spent a few hours around Pier 49 before driving down highway 1 through Big Sur.',
  },
  {
    image: '/images/IMG_3819.jpeg',
    label: 'Day 4',
    title: 'Big Sur -> Zion',
    description: 'Drove all the way from Big Sur to Zion. Lots of desert and straight roads without the proper car to make use of it.',
  },
  {
    image: '/images/IMG_3862.jpeg',
    label: 'Day 5',
    title: 'The big hike',
    description: 'Hiked from The Grotto up to the West Rim to campsite 2. Would not do again until I have significantly improved my cardio.',
  },
  {
    image: '/images/IMG_3925.jpeg',
    label: 'Day 6',
    title: 'West Rim -> Salt Flats -> Idaho City',
    description: 'Hiked down after spending the night up top, was SIGNIFICANTLY easier and didn\'t feel like dying afterward. Then drove 11 hours through the salt flats and up to Idaho.',
  },
  {
    image: '/images/IMG_3931.jpeg',
    label: 'Day 7',
    title: 'Idaho - Friends and resting',
    description: 'A slow day(finally) catching up with friends before the final drive home.',
  },
  {
    image: '/images/IMG_3937.jpeg',
    label: 'Day 8',
    title: 'Idaho → Seattle',
    description: 'Final drive home. Narrowly avoided putting chains on through Snoqualmie pass thank God.',
  },
]
</script>