<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    data() {
        return {
            logs: [
                {
                    photo: "src/assets/logo.svg",
                    name: "あいうえお",
                },
                {
                    photo: "src/assets/logo.svg",
                    name: "かきくけこ",
                },
            ],
        }
    }
})
</script>

<template>
    <!-- type checking and auto-completion enabled -->
    <div  v-for="(log, i) in logs" :key="i">
           <img :src="log.photo" width="50" height="50" />
           <div >{{ log.name }}</div>
    </div>
</template>