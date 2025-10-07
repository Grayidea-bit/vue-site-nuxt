<script setup lang="ts">
    const { isAnimate } = usePageTransition();
</script>

<template>
    <div class="w-full min-h-screen flex flex-col scroll-smooth">
        <div v-if="isAnimate" 
            :class="['fixed inset-0 top-25 z-50',{'animate-page-transition': isAnimate}]">
        </div>        
        <AppHeader />
            <div class="flex-1 w-full">
                <slot />
            </div>
        <AppFooter />
    </div>
</template>