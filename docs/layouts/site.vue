<template>
    <div class="bd-home">
        <a id="skippy" class="sr-only sr-only-focusable" href="#content">
            <div class="container">
                <span class="skiplink-text">Skip to main content</span>
            </div>
        </a>

        <m-nav></m-nav>

        <slot></slot>

        <m-footer></m-footer>
    </div>
</template>

<script>
    import mNav from '../includes/nav.vue';
    import mFooter from '../includes/footer.vue';

    export default {
        components: {mNav, mFooter},
        mounted(){
            // this.$ga.page(window.location.pathname);
            window.ga('send', 'pageview');
        }
    }
</script>