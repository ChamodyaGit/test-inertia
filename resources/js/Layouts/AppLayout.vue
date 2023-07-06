<template>
    <div>

        <Head :title="title ? title : 'Home'">
            <link rel="icon" type="image/png" href="{{ asset('assets/img/favicon.png') }}">
        </Head>

        <body onload="info_noti()">
            <!--wrapper-->
            <div class="wrapper">

                <SideBar />

                <NavBar />

                <slot name="content" />

                <Footer />
            </div>

        </body>
    </div>
</template>

<script>
import { Head } from '@inertiajs/vue3'
import NavBar from '@/Components/Main/NavBar.vue'
import SideBar from '@/Components/Main/SideBar.vue'
import Footer from '@/Components/Main/Footer.vue'

export default {
    components: {
        NavBar,
        SideBar,
        Footer,
    },
    props: {
        title: String,
    },
}
</script>

<style lang="css" scoped></style>
