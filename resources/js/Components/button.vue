<script setup>
import Layout from '@/Layouts/Layout.vue';
import { Head } from '@inertiajs/vue3';

import { ref, inject } from "vue";
const Color = inject('color');
</script>


<template>

        <button class="rounded-sm p-2" :class="{
            'bg-red-600' : Color == 'red',
            'bg-blue-600' : Color == 'blue',
            'bg-green-600' : Color == 'green',
         }">
            Click Me!
        </button>

</template>

<script>

    </script>
