<template>
    <UContainer>
        <slot/>
        <UFooter>
            <template #left>
                <p class="text-muted text-sm">Copyright James Rody © {{ new Date().getFullYear() }}</p>
            </template>

            <UNavigationMenu :items="items" variant="link"/>

            <template #right>
                <UButton
                    icon="i-simple-icons-linkedin"
                    variant="outline"
                    color="neutral"
                    size="sm"
                    to="https://www.linkedin.com/in/james-rody-17b2712ba/"
                    target="_blank"

                />
            </template>

        </UFooter>
    </UContainer>
</template>
<script setup>
    const items = [
        {
            label:"Home Page",
            to:"/",
            target:""

        },
        {
            label:"About Page",
            to:"/about",
            target:""

        },
        {
            label:"blank Page",
            to:"/",
            target:""

        },
        {
            label:"blank Page",
            to:"/",
            target:""

        },
        
    ];

</script>