<template>
    <div class="container">
        <div v-if="loading" class="loading">
            loading...
        </div>
        <div v-else class="row">
            <div v-for="project in projects" v-bind:key="project.name" class="col-lg-6 col-sm-12">
                <Card v-bind:project="project" />
            </div>
        </div>
        <br>
    </div>
</template>

<script>
import Card from './Card'

export default {
    name: 'Projects',
    data() {
        return {
            loading: true,
            projects: []
        }
    },
    components: {
        Card
    },
    created() {
        this.fetchData()
    },
    methods: {
        fetchData () {
            return fetch('https://cors-anywhere.herokuapp.com/https://raw.githubusercontent.com/AdithyaBhat17/portfolio-db/master/data.json', {
                method: 'GET',
                headers: {
                    'Content-Type': 'application/json'
                }
            })
            .then(response => response.json())
            .then(projects => {
                this.projects = projects
                this.loading = false
            })
            .catch(error => console.error(error))
        }
    } 
}

</script>

<style scoped>
    .container {
        margin-top: 40px;
    }
</style>



