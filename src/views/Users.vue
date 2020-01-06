<template>
    <div>
        <h3>Users</h3>
        <router-link to="/users/1">ユーザー1</router-link>
        <router-link to="/users/2">ユーザー2</router-link>
        <hr>
         <!-- $route 今の情報が入ってる感じ -->
        <!-- <h1>User  No.{{$route.params.id}}</h1> -->
        <h1>User  No.{{id}}</h1>  <!-- このやり方の方がrouter関係なく疎結合で再利用性が高くてよい -->
        <router-view></router-view>
    </div>
</template>

<script>
export default {
    props:[
        "id"
    ],
    watch:{
        $route(to,from){
            console.log(to);
            console.log(from);
            console.log("$route changed!");
        }
    },
    created : function() {
        console.log("created!");
    }
}
</script>