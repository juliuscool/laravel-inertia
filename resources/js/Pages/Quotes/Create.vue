<script setup>
    import GuestLayout from '@/Layouts/GuestLayout.vue';
    import { ref } from 'vue';

    const quote = ref('');

    const clear = ()=> {
        let quoteValue = quote.value;

        if(quoteValue){
            alert(quoteValue);
        }
    }
</script>

<template>
    <GuestLayout>
        <h1 class="mb-2">Create Quote</h1>
        <div class="form">
            <input v-model="quote" type="text" class="w-full" placeholder="Enter Quote">
            <input type="date" class="w-full" placeholder="Enter Year">
            <button v-on:click="clear" type="button" class="w-full">Save</button>
        </div>
    </GuestLayout>
</template>

<style scoped>
    h1{
        text-align: center;
        font-weight: bolder;
    }

    div.form input {
        margin-bottom: 12px;;
    }
</style>