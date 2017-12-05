<template>
    <!-- Navbar Container -->
    <div id="navbar-container">
        <!-- Navbar -->
        <nav class="navbar is-fixed-top" role="navigation" aria-label="main navigation">
            <!-- Navbar Brand -->
            <div class="navbar-brand">
                <router-link :to="{ path: '/' }" class="navbar-item">
                    <h1 id="navbar-logo-custom" class="is-size-4 has-text-black">Vent</h1>
                    <!-- <h1 id="navbar-logo-custom-last" class="is-size-4 has-text-black">OUT</h1> -->
                </router-link>
            </div><!-- End of Navbar Brand -->
        </nav> <!-- End of Navbar -->
    </div> <!-- End of Navbar Container -->
</template>

<script>
export default {
  name: 'Navbar'
}
</script>

<style lang="scss" scoped>
    #navbar-logo-custom {
        letter-spacing: 5px;
        font-weight: 400;
        margin-left: 45%;
        margin-right: 45%;
    }
</style>
