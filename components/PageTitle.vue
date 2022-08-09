<template>
    <div>
        <section id="header" class="col-md-12 text-center mb-4 mt-5">
            <h1 class="fw-bold">
                {{ title }}
            </h1>

            <img :src="image" class="mb-3 mt-5">
        </section>
    </div>
</template>

<script>
    export default {
        props: {
            title: String,
            image: String
        }
    }
</script>