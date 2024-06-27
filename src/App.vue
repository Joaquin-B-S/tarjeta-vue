<template>
    <form>
        <div>
            <label for="titulo">Título de la tarjeta: </label>
            <input id="titulo" type="text" v-model="titulo" />
        </div>

        <div>
            <label for="chip">Chip SRC: </label>
            <input id="chip" type="text" v-model="chip" />
        </div>

        <div>
            <label for="numero">Número: </label>
            <input id="numero" type="text" v-model="numero" />
        </div>

        <div>
            <label for="fechaExp">Fecha de expiración: </label>
            <input id="fechaExp" type="text" v-model="fechaExp" />
        </div>

        <div>
            <label for="propietario">Propietario: </label>
            <input id="propietario" type="text" v-model="propietario" />
        </div>

        <div>
            <label for="tipoTarjeta">Tipo de tarjeta SRC: </label>
            <input id="tipoTarjeta" type="text" v-model="tipoTarjeta" />
        </div>
    </form>

    <div class="carnet">
        <h3>{{ titulo }}</h3>
        <img width="40" :src="chip" alt="Chip" />
        <div>
            <h2>{{ numero }}</h2>
            <span
                >Fecha Exp: <b>{{ fechaExp }}</b></span
            >
        </div>
        <footer>
            <span>{{ propietario }}</span>
            <img :src="tipoTarjeta" width="60" alt="tipo de tarjeta" />
        </footer>
    </div>
</template>

<script>
export default {
    data() {
        return {
            titulo: "",
            chip: "",
            numero: "",
            fechaExp: "",
            propietario: "",
            tipoTarjeta: "",
        };
    },
};
</script>
