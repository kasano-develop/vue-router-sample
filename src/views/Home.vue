<template>
    <div>
        <!-- router-viewタグはrouter-view内では使えない-->
        <h3>HOME</h3>
        <button @click="toUsers">to Users page</button>
    </div>
</template>

<script>
export default {
    methods : {
        toUsers() {
            this.$router.push({path:"/users"}); // $router 切り替え時に使うもの
        }
    }
}
</script>
