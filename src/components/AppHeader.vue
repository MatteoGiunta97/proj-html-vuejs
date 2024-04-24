<script>
import Links from './Links.vue';

export default {
    name: 'AppHeader',
    components: {
        Links
    },
    data() {
        return {
            links: [
                {
                    'label': "HOME",
                    'path': "#"
                },
                {
                    'label': "ABOUT",
                    'path': "#"
                },
                {
                    'label': "SERVICES",
                    'path': "#"
                },
                {
                    'label': "SHOWCASE",
                    'path': "#"
                },
                {
                    'label': "BLOG",
                    'path': "#"
                },
                {
                    'label': "CONTACT",
                    'path': "#"
                }
            ]
        };
    }
}
</script>

<template>

    <header>
        <div class="ms-cover">
            <div class="ms-header-top container">
                <div>(001) 88451234 88455438</div>
                <div>
                    <a href="#"><i class="fa-brands fa-facebook-f p-2"></i></a>
                    <a href="#"><i class="fa-brands fa-x-twitter p-2"></i></a>
                    <a href="#"><i class="fa-brands fa-pinterest-p p-2"></i></a>
                </div>
            </div>
        </div>
        <nav class="navbar">
            <div class="container">
                <a class="navbar-brand" href="#">
                    <img src="../assets/img/logo.png" height="50" alt="logo">
                </a>
                <nav class="nav">

                    <Links v-for="link in links" :linkInfo="link"></Links>
               
                </nav>
                <nav class="navbar">
                    <form class="container-fluid justify-content-start">
                        <button class="btn me-2" type="button">PURCHASE</button>
                        <a href="#"><i class="fa-solid fa-magnifying-glass"></i></a>
                    </form>
                </nav>
            </div>
        </nav>
    </header>

</template>

<style scoped lang="scss">

    .ms-cover {
        background-color: #3d3d3d;

        .ms-header-top {
            color: white;
            display: flex;
            justify-content: space-between;
            align-items: center;

            a {
                color: inherit;
            }
        }
    }

    button {
        background: linear-gradient(to right, #7cf10ed6, #1bceb6);
        color: white;
        border-radius: 20px;
        padding: 7px 28px;
    }
    .fa-magnifying-glass {
        color: #1bceb6;
    }

</style>