<template>
    <b-container fluid>
        <b-row class="footer-row" align-h="between" aligh-v="center">
            <b-col lg="4" md="5" sm="10">
                <img class="map-img" :src="require(`@/assets/${map}`)" />
            </b-col>
            <b-col lg="6" md="6" sm="10">
                <b-form @submit="onSubmit">
                    <b-form-row>
                        <b-form-input required placeholder="example@mail.com"></b-form-input>
                    </b-form-row>
                    <b-form-row>
                        <b-textarea rows="4" required placeholder="comments..."></b-textarea>
                    </b-form-row>
                    <b-form-row>
                        <b-button type="submit" block variant="success">Contactar</b-button>
                    </b-form-row>
                </b-form>
            </b-col>
        </b-row>
    </b-container>
</template>

<script>
    export default {
        name: 'footer-component',
        data: function () {
            return {
                map: 'map.png'
            }
        }
    }
</script>

<style scoped>
    .container-fluid {
        margin-top: 6em;
        padding: 1.5em;
        background-color: #303841;
    }

    .col-map {
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .map-img {
        width: 100%;
        height: auto;
    }

    .form-row {
        margin-bottom: 1em;
    }

    .form-control {
        padding: 1em;
    }
    .col-sm-10 {
        margin-bottom: 1em;
    }
</style>