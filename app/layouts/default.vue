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
                <UButton
                    icon="i-simple-icons-linkedin"
                    variant="outline"
                    color="neutral"
                    size="sm"
                    to="https://www.linkedin.com/in/james-rody-17b2712ba/"

                />
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
            label:"About Page",
            to:"/about"
        },
        {
            label:"Portfolio",
            to:"/portfolio"
        },
        {
            label:"Contact",
            to:"/contact"
        },
        
    ];

</script>