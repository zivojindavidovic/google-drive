<template>
    <MenuItem v-slot="{ active }">
        <a href="#" class="text-gray-700 text-sm px-4 py-2 block relative">
            Upload Files

            <input @change="onChange" type="file"
                   class="absolute left-0 top-0 bottom-0 right-0 cursor-pointer opacity-0" multiple>
        </a>
    </MenuItem>
</template>

<script setup>

import {MenuItem} from "@headlessui/vue";
import {emitter, FILE_UPLOAD_STARTED} from "@/event-bus.js";

function onChange(e) {
    emitter.emit(FILE_UPLOAD_STARTED, e.target.files)
}
</script>

<style scoped>

</style>
