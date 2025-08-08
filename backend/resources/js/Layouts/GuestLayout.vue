<script setup>
import ApplicationLogo from '@/Components/ApplicationLogo.vue';
import { Link } from '@inertiajs/vue3';
</script>

<template>
    <div
        class="flex min-h-screen flex-col items-center bg-gray-100 pt-6 sm:justify-center sm:pt-0 bg-guest-layout"
    >
        <div>
            <Link href="/">
                <ApplicationLogo />
            </Link>
        </div>

        <div
            class="mt-6 w-full overflow-hidden bg-[rgba(255,255,255, 0.3)] px-6 py-4 sm:max-w-md sm:rounded-lg"
        >
            <slot />
        </div>
    </div>
</template>

<style scoped>

.bg-guest-layout {
    background-image: url('../../images/botanical-herbs-bg.jpg');
    background-size: 100% 100%;
}

</style>
