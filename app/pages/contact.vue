<template>
    <div class="max-w-2xl mx-auto px-6 py-12 mx-auto text-center">
      <UPageHeader
        title="Have Questions? Contact me!"
        class="text-center"
      />
        <Form class=""/>
      <div class="max-w-2xl mx-auto px-6 py-12">
        <h2 class="text-xl font-semibold text-neutral-800 mb-6">Frequently asked questions</h2>
        <UAccordion :items="faqs" />
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  const faqs = [
    {
      label: 'How long was the trip?',
      content: 'About 8 days total, covering over 3,000 miles from Seattle down the coast and back up through Utah and Idaho.',
    },
    {
      label: 'How many people went?',
      content: 'Just my roomate and I.',
    },
    {
      label: 'What would you do differently?',
      content: 'We needed more time to explore. We spend probably 75% of our daylight driving, not including Zion.',
    },
  ]
  </script>