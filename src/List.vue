
<template>
    <article v-for="p in props.data" :key="p.id" class="person">
        <img :src="p.image" :alt="p.name">
        <div>
            <h4>{{ p.name }}</h4>
            <p>{{ p.age }}</p>
        </div>
    </article>
</template>

<script lang="ts" setup>
import { defineProps } from "vue"

type Item = {
    id: number,
    name: string,
    age: number,
    image: string
}

const props = defineProps({
    data: {
        type: Array<Item>,
        required: true
    }
})

</script>