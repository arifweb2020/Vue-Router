<template>
<div>
    <h1>User page</h1>
    <h2>User id is {{userId}}</h2>
    </div>
</template>

<script>
export default {
    name : 'User',
    data(){

        return{ userId:this.$route.params.id}
    }
}
</script>