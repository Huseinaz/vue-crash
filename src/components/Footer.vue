<template>
    <footer>
        <p>Copyright &copy; 2023</p>
        <router-link to="/about" v-show="homePage">About</router-link>
    </footer>
</template>

<script>
    export default {
        computed: {
            homePage() {
                if(this.$route.path === '/') {
                    return true
                }
                else {
                    return false
                }
            }
        }
    }
</script>

<style scoped>
a {
    color: #333;
}
footer {
    margin-top: 30px;
    text-align: center;
}
</style>