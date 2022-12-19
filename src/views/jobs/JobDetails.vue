<template>
    <div v-if="job">
        <h1>Job details page</h1>
        <p> {{ $route.params.id }}</p>
        <p> Job id: {{ id }}</p>
        <p> Book name: {{ job.title }} by: {{ job.author }}</p>
    </div>
    <div v-else>
        <h2>Loading data</h2>
    </div>

</template>

<script>
export default {
    data(){
        return{
            id: this.$route.params.id,
            job: null,
        }
    },
    mounted(){
        fetch('http://localhost:3000/jobs/' + this.id)
        .then(res => res.json())
        .then(data => this.job = data)
        .catch(err => console.log(err.message))
    }
}
</script>

<style>

</style>