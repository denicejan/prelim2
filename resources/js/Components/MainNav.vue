<script setup>
    import { Link } from '@inertiajs/vue3';
    import { defineProps } from 'vue';
    import { ref, inject } from "vue";
    const Color = inject('color')
    
    const {hidden} = defineProps (['hidden'])

    </script>
    
    <template>
    
        <div class="main-nav shadow-lg" style="text-align: start;">
            <Link :class="{
                'bg-red-600' : Color == 'red',
                'bg-blue-600' : Color == 'blue',
                'bg-green-600' : Color == 'green',
             }" :href="route('dashboard')" :active="route().current('dashboard')">
                <i class="fa-solid fa-house-chimney"></i> <span :hidden="hidden">Dashboard</span>
            </Link>
            <Link :class="{
                'bg-red-600' : Color == 'red',
                'bg-blue-600' : Color == 'blue',
                'bg-green-600' : Color == 'green',
             }" :href="route('clients')" :active="route().current('clients')">
                <i class="fa-solid fa-user"></i> <span :hidden="hidden">Clients</span>
            </Link>
    
    
        </div>
    
    </template>