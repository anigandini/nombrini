<script setup>
import { Head, Link } from '@inertiajs/vue3';
import About from './About.vue'
import ApplicationLogo from '../Components/ApplicationLogo.vue';

defineProps({
    canLogin: {
        type: Boolean,
    },
    canRegister: {
        type: Boolean,
    },
    laravelVersion: {
        type: String,
        required: true,
    },
    phpVersion: {
        type: String,
        required: true,
    },
});

function handleImageError() {
    document.getElementById('screenshot-container')?.classList.add('!hidden');
    document.getElementById('docs-card')?.classList.add('!row-span-1');
    document.getElementById('docs-card-content')?.classList.add('!flex-row');
    document.getElementById('background')?.classList.add('!hidden');
}
</script>

<template>
    <Head title="Welcome" />
    <div class="bg-gray-50 text-black/50 dark:bg-black dark:text-white/50 w-full h-full home-bg">
        <div>
            <header
                class="grid grid-cols-2 items-center gap-2 lg:grid-cols-3"
            >
                <nav v-if="canLogin" class="w-screen flex justify-between p-4">
                    <ApplicationLogo class="text-white"/>
                    <div>
                        <Link
                            v-if="$page.props.auth.user"
                            :href="route('dashboard')"
                            class="rounded-md px-3 py-2 text-white ring-1 ring-transparent transition hover:text-black/70 focus:outline-none focus-visible:ring-[#FF2D20] dark:text-white dark:hover:text-white/80 dark:focus-visible:ring-white"
                        >
                            Dashboard
                        </Link>

                        <template v-else>
                            <Link
                                :href="route('login')"
                                class="rounded-md px-3 py-2 text-white ring-1 ring-transparent transition hover:text-black/70 focus:outline-none focus-visible:ring-[#FF2D20] dark:text-white dark:hover:text-white/80 dark:focus-visible:ring-white"
                            >
                                Log in
                            </Link>

                            <Link
                                v-if="canRegister"
                                :href="route('register')"
                                class="rounded-md px-3 py-2 text-white ring-1 ring-transparent transition hover:text-black/70 focus:outline-none focus-visible:ring-[#FF2D20] dark:text-white dark:hover:text-white/80 dark:focus-visible:ring-white"
                            >
                                Register
                            </Link>
                        </template>
                    </div>
                </nav>
            </header>
        </div>
        <main class="w-screen h-screen  flex flex-col justify-center md:justify-start items-center gap-2 md:gap-7">
            <h2 class="h2 relative text-[#49180B] mb-[2rem] mt-[2rem] pr-6 text-2xl md:text-4xl">
                Nombres con sentido.<br />
                Listas con amor.
            </h2>
            <div class="text-[#49180B] text-highlighted">
                Encuentra inspiración, explora significados y guarda tus nombres favoritos en listas compartibles.
            </div>
            <div>
                <Link
                    :href="route('search')"
                    class="px-3 py-2 text-white underline  hover:text-[#49180B]/70 focus:outline-none focus-visible:ring-[#FF2D20] dark:text-white dark:hover:text-white/80 dark:focus-visible:ring-white"
                >
                    Buscar nombres
                </Link>
                <Link
                    :href="route('new-list')"
                    class="px-3 py-2 text-white underline hover:text-[#49180B]/70 focus:outline-none focus-visible:ring-[#FF2D20] dark:text-white dark:hover:text-white/80 dark:focus-visible:ring-white"
                >
                    Crear lista
                </Link>
            </div>
        </main>
    </div>
    <About></About>
</template>
