<script>
//import { store } from "../store";
export default {
    props: {
        project: Object,
    },
    data() {
        return {
            baseUrl:'http://.127.0.0.1:8000',
            // store
        }
    }
}

</script>

<template>
    <div class="card">
        <div class="card-body">
            <h5>{{ project.title }}</h5>
            <router-link :to="{name: 'single-project', params:{slug: project.slug}}">dettagli</router-link>
        </div>
    </div>
</template>

<style></style>