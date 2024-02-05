<script>
import { store } from "../store";
export default {
    props: {
        project: Object,
    },
    data() {
        return {
            store
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