<script>
export default {
    props: {
        project: Object,
    },
    data() {
        return {
            baseUrl: 'http://127.0.0.1:8000',
        }
    }
}

</script>

<template>
    <div class="card">
        <div class="card-body">
            <h5>{{ project.title }}</h5>
        </div>
    </div>
</template>

<style></style>