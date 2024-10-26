<template>
    <div>
        <div class="spinner-border text-info" role="status">
            <span class="visually-hidden">Loading...</span>
        </div>{{ title }}...
    </div>
</template>

<script>
export default {
    name: "loading",
    props: {
        title: String
    }
}
</script>