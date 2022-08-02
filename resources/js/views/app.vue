<template>
    <div>
        <h1>JS</h1>
    </div>
</template>

<script>

export default{
    name: 'App',
    data(){
        return {
            posts: []
        };
    },
    created(){
        axios.get('http://127.0.0.1:8000/api/posts')
            .then((respone)=>{
                console.log(respone.data);
            })
            .catch((e)=>{
                console.log(e);
            });
    },

}
</script>

<style>

</style>