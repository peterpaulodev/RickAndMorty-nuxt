<template>
    <div>
        <head>
            <meta charset="utf-8" />
            <meta http-equiv="X-UA-Compatible" content="IE=edge" />
            <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no" />

            <title>Ricky and Morty</title>

            <!-- Font family - Didact Gothic -->
            <link href='https://fonts.googleapis.com/css?family=Didact Gothic' rel='stylesheet'>

            <!-- Bootstrap CSS 5.2.0 -->
            <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css"
            integrity="sha384-gH2yIJqKdNHPEq0n4Mqa/HGKIhSkIHeL5AyhkYV8i59U5AR6csBvApHHNl/vI1Bx" crossorigin="anonymous">

            <!-- Font Awesome 6.1.2 -->
            <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.2/css/all.min.css"
            integrity="sha512-1sCRPdkRXhBV2PBLUdRb4tMg1w2YPf37qatUFeS7zlBy7jJI8Lf4VHwWfZZfpXtYSLy85pkm9GaYVYMfw5BC1A=="
            crossorigin="anonymous" referrerpolicy="no-referrer" />
        </head>

        <nav class="navbar navbar-expand-lg bg-light">
            <div class="container-fluid">
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                    aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse justify-content-l" id="navbarNav">
                    <ul class="navbar-nav">
                        <li class="nav-item mx-4">
                            <NuxtLink class="nav-link active fs-4" aria-current="page" to="/">
                                Personagens
                            </NuxtLink>
                        </li>
                        <li class="nav-item mx-4">
                            <NuxtLink  class="nav-link fs-4" to="/about">
                                Sobre
                            </NuxtLink>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>

        <section id="header" class="col-md-12 text-center mb-4 mt-5">
            <h1 class="fw-bold">
                Rick and Morty JQuery API
            </h1>
            <img src="~/static/img/dancing-rick.gif" class="mb-3 mt-5">
        </section>
    </div>
</template>