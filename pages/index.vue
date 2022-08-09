<template>
    <div>
        <section id="characters" class="col-md-12 mt-5 background-pacific-blue">
            <h1 class="text-center fw-bold text-white mt-4">
                Personagens
            </h1>

            <div class="input-group mx-auto my-4 w-50 col-md-12">
                <input type="text" class="form-control" id="character-name" placeholder="Digite para procurar..."
                    aria-label="Digite para procurar..." aria-describedby="basic-addon2"
                    v-model="searchCharacterName" @keyup="getCharacters">

                <span class="input-group-text" id="basic-addon2">
                    <i class="fas fa-search" aria-hidden="true"></i>
                </span>
            </div>

            <div class="cards row mx-auto my-4">
                <CharacterCard v-for="(char, index) in characters"
                    :key="index"
                    :name="char.name"
                    :image="char.image"
                    :gender="char.gender"
                    :species="char.species"
                    :status="char.status"
                >
                </CharacterCard>
            </div>
        </section>
    </div>
</template>

<script>
    export default {
        name: "IndexPage",
        data() {
            return {
                characters: [],
                searchCharacterName: ''
            }
        },
        methods: {
            async getCharacters() {
                const url = "/character/?name=" + this.searchCharacterName;

                let characters = await this.$axios.$get(url);
                this.characters = characters.results;
            }
        },
        mounted() {
            this.getCharacters()
        }
    }
</script>

<style>
  :root {
    /* BACKGROUND */
    --default-background: #202329;

    /* CSS HEX */
    --black: #000000ff;
    --pacific-blue: #00B0C8ff;
    --black-2: #000000ff;
    --skobeloff: #10777Dff;
    --june-bud: #B1D34Bff;

    /* CSS Gradient */
    --gradient-top: linear-gradient(0deg, #000000ff, #00B0C8ff, #000000ff, #10777Dff, #B1D34Bff);
    --gradient-right: linear-gradient(90deg, #000000ff, #00B0C8ff, #000000ff, #10777Dff, #B1D34Bff);
    --gradient-bottom: linear-gradient(180deg, #000000ff, #00B0C8ff, #000000ff, #10777Dff, #B1D34Bff);
    --gradient-left: linear-gradient(270deg, #000000ff, #00B0C8ff, #000000ff, #10777Dff, #B1D34Bff);
    --gradient-top-right: linear-gradient(45deg, #000000ff, #00B0C8ff, #000000ff, #10777Dff, #B1D34Bff);
    --gradient-bottom-right: linear-gradient(135deg, #000000ff, #00B0C8ff, #000000ff, #10777Dff, #B1D34Bff);
    --gradient-top-left: linear-gradient(225deg, #000000ff, #00B0C8ff, #000000ff, #10777Dff, #B1D34Bff);
    --gradient-bottom-left: linear-gradient(315deg, #000000ff, #00B0C8ff, #000000ff, #10777Dff, #B1D34Bff);
    --gradient-radial: radial-gradient(#000000ff, #00B0C8ff, #000000ff, #10777Dff, #B1D34Bff);
  }

  * {
    font-family: 'Didact Gothic';
  }

  nav {
    background-color: white;
  }

  .header-section {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 330px;
    width: 100%;
  }

  .form-control:focus {
    border-color: var(--june-bud) !important;
    box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 8px var(--june-bud) !important;
  }

  .input-group-text {
    background-color: var(--june-bud) !important;
    border-color: var(--june-bud) !important;
    color: #fff !important;
  }

  .background-pacific-blue {
    background-color: var(--pacific-blue);
    padding: 0;
  }

  .wave-bg {
    background-image: url('~/static/img/wave.svg') !important;
    background-attachment: fixed !important;
    background-size: cover !important;
  }

  .status-Dead {
    height: 10px;
    width: 10px;
    background-color: #bbb;
    border-radius: 50%;
    display: inline-block;
    background: rgb(214, 61, 46);
    margin-right: 5px;
  }

  .status-Alive {
    height: 10px;
    width: 10px;
    background-color: #bbb;
    border-radius: 50%;
    display: inline-block;
    background: rgb(85, 204, 68);
    margin-right: 5px;
  }

</style>
