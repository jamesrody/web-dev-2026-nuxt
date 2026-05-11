<template>
    <UContainer>
        <UHeader title="James Rody">
            <UNavigationMenu :items="items" variant="link"/>
        </UHeader>
        <slot/>
        <UFooter>
            <template #left>
                <p class="text-muted text-sm">Copyright James Rody © {{ new Date().getFullYear() }}</p>
            </template>

            <UNavigationMenu :items="items" variant="link"/>

            <template #right>
            </template>

        </UFooter>
    </UContainer>
</template>
<script setup>
    const items = [
        {
            label:"Home Page",
            to:"/"
        },
        {
            label:"Itinerary Page",
            to:"/itinerary"
        },
        {
            label:"Gallery",
            to:"/gallery"
        },
        {
            label:"Contact",
            to:"/contact"
        },
        
    ];

</script>