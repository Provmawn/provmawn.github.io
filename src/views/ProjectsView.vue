<template>
    <div class="container">
        <div class="row mt-3 mx-auto">
            <div v-for="project in projects" :key="project.id" class="col-md-4 mb-3 mt-3">
                <div class="card project-card">
                    <div class="card-body">
                        <h2 class="project-heading">{{ project.name }}</h2>
                        <p class="description">
                            <span class="section description">description: </span>
                            {{ project.description }}
                        </p>
                        <p class="non-essential">
                            <div v-if="project.demo">
                                <span class="section non-essential">demo link: </span>
                                <a class="non-essential" target="_blank" :href="project.demo">here</a>
                            </div>
                        </p>
                        <a v-if="project.code.length > 0" class="non-essential" :href="project.code">source-code</a>
                        <img class="img-fluid mt-3" :src="project.image"/>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "ProjectView",
    component: {
    },
    data() {
        return {
            projects: [
                { id: 0, name: 'NEURO Game Framework', description:'3D Game framework implemented in C++.', code: 'https://github.com/Provmawn/Neuro', demo: '', image: require('@/assets/game-framework.png') },
                { id: 1, name: 'Pet Bot', description:'Discord bot pokemon like game written in python.', code: 'https://github.com/ant-codez/PetBot', demo: '', image: require('@/assets/petbot.png')},
                { id: 2, name: 'Minesweeper Replica', description:'Minesweeper recreated from in java.', code: 'https://github.com/Provmawn/java_minesweeper', demo: '', image: ''},
                { id: 3, name: 'Gun Man\'s Nightmare', description:'2D web game made with javascript and canvas.', code: 'https://github.com/Provmawn/gunmans-nightmare', demo: 'https://www.youtube.com/watch?v=9pqFwmkh7r8', image: require('@/assets/gunmans-nightmare.png')},
                { id: 4, name: 'Asteroids', description:'2D asteroids game written in C++ with SDL', code: 'https://github.com/Provmawn/asteroids', demo: '', image: ''},
                { id: 5, name: 'full-type', description:'typing app that uses 100% of your keyboard', code: '', demo: 'http://full-type.com', image: ''},
            ]
        }
    }
}
</script>

<style>
img {
    transition:transform 0.25s ease;
}

img:hover {
    -webkit-transform:scale(1.5); /* or some other value */
    transform:scale(1.5);
}

.project-card {
    width: 18rem;
    background: #000;
    border:1px dotted red;
}

p {
    text-align: left;
}

.description {
    font-size: 17px;
}

.non-essential {
    font-size: 17px;
}

.section {
    color: red;
}

.project-heading {
    height: 20%;
    border-bottom: 1px dotted red;
    font-size:23px;
    font-weight: bold;
}
</style>
