<template>
    <a target="_blank" rel="noopener noreferrer" :href="projectInfo.link">
        <div class="thumbnail">
            <img v-bind:src="projectInfo.image" :alt="projectInfo.name">
            <h2 class="name">{{ projectInfo.name }}</h2>
            <p class="desc">{{ projectInfo.description }}</p>
            <div class="tech-stack">
                <span :key="index" v-for="(tech, index) in projectInfo.tech">{{ tech }} </span>
            </div>
        </div>
    </a>
</template>

<script>
export default {
    name: 'Card',
    props: ['project'],
    data() {
        return {
            projectInfo: this.project
        }
    }
}
</script>

<style scoped>
    a {
        display: block;
        text-decoration: none;
        text-align: center;
        color: #444;
        margin-top: 55px;
    }
    h2 {
        font-weight: bold;
    }
    span {
        background-color: #ececec;
        padding: 5px 8px;
        margin: 0 2px;
        border-radius: 4px;
        box-shadow: 5px 5px 25px 0 rgba(0, 0, 0, 0.1);
    }
</style>


