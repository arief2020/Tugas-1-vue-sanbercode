<template>
    <div>
        <nav>
            <div class="container-fluid">
                <a href="#" class="navbar-brand">My Vue</a>
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li v-for="(page, index) in pages" class="nav-item" :key="index">
                    <a 
                    class="nav-link"
                    :class="{active: activePage == index}"
                    aria-current="page"
                    :href="page.link.url"
                    :title="`This link goes to the ${page.link.text} page`"
                    @click="navLinkClick(index)"
                    >{{ page.link.text }}</a>
                    </li>
                </ul>
                <form class="d-flex">
                    <button
                    class="btn btn-primary"
                    @click.prevent="changeTheme()"
                    >
                        Toogle
                    </button>
                </form>
            </div>
        </nav>
    </div>
</template>

<script>
export default{
    props: ['pages', 'activePage', 'navLinkClick'],
    data() {
        return {
            theme: 'light'
        }
    },
    methods: {
        changeTheme(){
            let theme = 'light';
            if (this.theme == 'light') {
                theme = 'dark';
            }
            this.theme= theme
        }
    }
}
</script>