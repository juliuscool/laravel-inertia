<script setup>
    import GuestLayout from '@/Layouts/GuestLayout.vue';

    defineProps({
        quotes: {
            type: Array
        },
        isAdmin: {
            type: Boolean
        }
    });
</script>

<template>
    <GuestLayout>
        <h1>Quotes <span v-if="isAdmin">&checkmark;</span></h1>
        <div>
            <ul>
                <li v-bind:key="quote" v-for="quote in quotes">{{ quote }}</li>
            </ul>
        </div>
    </GuestLayout>
</template>

<style scoped>
    h1{
        text-align: center;
    }
</style>