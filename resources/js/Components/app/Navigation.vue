<template>
    <nav class="min-w-[200px]">
        <Link :href="route('myFiles')" class="h-[80px] px-3 items-center gap-3">
            <ApplicationLogo
                class="inline-block mb-1 h-9 w-auto fill-current text-gray-800"
            />
            GoogleDrive
        </Link>
        <div class="px-3 mt-6">
            <CreateNewDropdown/>

            <div class="py-3">
                <NavLink :href="route('myFiles')" :active="$page.url === '/my-files'">My Files</NavLink>
                <NavLink href="/">Shared with me</NavLink>
                <NavLink href="/">Shared by me</NavLink>
                <NavLink href="/">Trash</NavLink>
            </div>
        </div>
    </nav>
</template>

<script setup>

import ApplicationLogo from "@/Components/ApplicationLogo.vue";
import {Link, router} from '@inertiajs/vue3';
import CreateNewDropdown from "@/Components/app/CreateNewDropdown.vue";
import NavLink from "@/Components/NavLink.vue";

</script>

<style scoped>

</style>
