<template>
    <h1>Jobs</h1>
    <div v-for="job in jobs" :key="job.id">
        <router-link :to="{ name : 'JobDetails', params : { id: job.id }}">
        <h2>{{ job.title }} </h2>
        </router-link>
    </div>
</template>

<script>
export default {
    data(){
        return {
            jobs: [
                {title: 'New book1', id: 1 , author: 'Ivan lukyanov'},
                {title: 'Some new book', id: 2, author: 'Vasya Pupkin'}
            ]
        }
    }
}
</script>

<style>

</style>