<template>
    <div class="col-md-6">
        <div class="card mb-3 mx-auto" style="max-width: 540px;">
            <div class="row g-0">
                <div class="col-md-4">
                    <img :src="image" class="img-fluid rounded-start" :alt="name">
                </div>
                <div class="col-md-8">
                    <div class="card-body">
                    <h5 class="card-title">{{name}}</h5>
                    <p class="card-text">
                        <b>Genêro:</b> {{gender}}
                        <br>
                        <b>Espécie:</b> {{species}}
                    </p>
                    <p class="card-text">
                        <span :class="`status-${status}`"></span>
                        <small class="text-muted">
                            {{status}}
                        </small>
                    </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            image: String,
            name: String,
            gender: String,
            species: String,
            status: String
        }
    }
</script>