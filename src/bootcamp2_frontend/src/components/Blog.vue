<template>
    <div>
        <button @click="pobierzWpisy">refresh</button>
        siema blog!
        {{ wpisy }}
    </div>
</template>

<script>
import { bootcamp2_backend } from 'declarations/bootcamp2_backend/index';

export default {
    data() {
        return {
            wpisy: []
        }
    },
    methods: {
        async pobierzWpisy() {
            this.wpisy = await bootcamp2_backend.odczytaj_wpisy();
        }
    },
}
</script>