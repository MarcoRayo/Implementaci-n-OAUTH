<template>
    <div class="home">
        <h1>Login con OAuth</h1>
        <!-- Revisa la librería se encuentra cargando antes de mostrar los botones de acceso -->
        <div v-if="!$auth.loading">
            <!-- muestra el botón de login si no está autentificado -->
            <b-button variant="outline-primary" v-if="!$auth.isAuthenticated" @click="login">Iniciar Sesión</b-button>
            <!-- muestra el botón de Log out si está autentificado -->
            <b-button variant="outline-danger" v-if="$auth.isAuthenticated" @click="logout">Cerrar Sesión</b-button>
        </div>
    </div>
</template>

<script>
    export default {
        name: "home",
        methods: {
            login() {
                this.$auth.loginWithRedirect();
            },
            logout() {
                this.$auth.logout({
                    logoutParams: {
                        returnTo: window.location.origin,
                    },
                });
            },
        },
    };
</script>