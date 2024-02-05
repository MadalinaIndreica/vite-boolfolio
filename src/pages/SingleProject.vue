<script>
import axios from "axios";
export default {
    data() {
        return {

            baseUrl: 'http://127.0.0.1:8000',
            project: null,
            loading: false
        }
    },
    created() {
        this.loading = true;
        axios.get(`${this.baseUrl}/api/projects/${this.$route.params.slug}`).then((resp) => {

            this.project = resp.data.results;

        }).finally(() => {
            this.loading = false;
        })

    }
}
</script>

<template>
    <div v-if="loading">
        <h3> loading…</h3>
    </div>
    <div v-else>
        <h1> {{ project.title }} </h1>
    </div>
</template>

<style lang="scss" scoped></style>