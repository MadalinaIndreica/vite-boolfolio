<script>
import axios from 'axios';
import AppCards from './AppCards.vue';
import { store } from "../store";
export default {
    data() {
        return {
            baseUrl: 'http://127.0.0.1:8000',
            projects: [],
            store

        }
    },
    created() {
        axios.get(`${this.store.baseUrl}/api/projects`).then((resp) => {
            // console.log(resp);
            this.projects = resp.data.results;
        })
    },
    components : {AppCards}
}

</script>

<template>
    <div class="container">
        <h2>Progetti disponibili</h2>
        <div class="row">
            <div class="col" v-for="project in projects" :key="project.id">
               <AppCards :project="project"/>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped ></style>