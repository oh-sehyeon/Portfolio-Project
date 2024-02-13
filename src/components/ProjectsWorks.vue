<template>
    <section id="projectsWorks_section">
        <h4>Check out my latest Projects</h4>
        <div class="projects_container">
            <a v-for="(project, index) in projects" :key="index" :href="project.url" class="project" target="_blank">
                <div :id="project.id"></div>
                <div class="project_details">
                    <p class="project_name">{{ project.name }}</p>
                    <p class="project_info">{{ project.description }}</p>
                </div>
            </a>
        </div>
    </section>
</template>

<script>
export default {
    name: 'ProjectsWorks',
    data() {
        return {
            projects: [
                {
                    id: 'colourfit',
                    name: 'ColourFit',
                    url: 'https://github.com/ansonsow/rhealm',
                    description: 'Project made for Langara College\'s Capstone project. Worked as Full-Stack developer using ExpressJS, React Native and NodeJS combining with MongoDB and Firebase Storage.'
                },
                {
                    id: 'gallop',
                    name: 'Gallop',
                    url: 'https://github.com/mahzinhaaugusto/gallop',
                    description: 'Term project made for Langara Collge\'s 3rd term. Worked as the main Front-End developer using ReactJS, Firebase Storage and NodeJS.'
                },
                {
                    id: 'peoplecars',
                    name: 'People & Cars',
                    url: 'https://github.com/oh-sehyeon/people-cars',
                    description: 'Web application made using React, Apollo and GraphQL. This application let user to add new User, add cars to users as well as it is posible to edit and delete both users and cars.'
                },
                {
                    id: 'moviesapp',
                    name: 'MoviesApp',
                    url: 'https://github.com/oh-sehyeon/moviesApp',
                    description: 'React Native App made to search for Movies and TV Shows through TMDB API.'
                },
                {
                    id: 'snakegame',
                    name: 'Snake Game',
                    url: 'https://oh-sehyeon.github.io/snake-game/',
                    description: 'Classic Snake game made with HTML, CSS and Vanilla JavaScript.'
                }
            ]
        };
    }
}
</script>

<style scoped>

#colourfit,
#gallop,
#peoplecars,
#moviesapp {
    display: none;
}

#projectsWorks_section {
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    padding-bottom: 3rem;
}

#projectsWorks_section > h4 {
    color: white;
    padding: 0 5%;
    font-size: 1.75rem;
    margin-bottom: 2rem;
    text-align: center;
}

#projectsWorks_section > .projects_container {
    background-color: #FAFAFA;
    margin: 0 5%;
    padding: 2rem 2rem;
    box-shadow: inset 0 0 8px black;
}

#projectsWorks_section > .projects_container > .project {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: center;
    width: 100%;
    padding: 1rem 0;
    border-bottom: .1px solid black;
}

#projectsWorks_section > .projects_container > .project:first-child {
    padding-top: 0;
}

#projectsWorks_section > .projects_container > .project:last-child {
    padding-bottom: 0;
    border-bottom: none;
}

#projectsWorks_section > .projects_container > .project > .project_details {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    width: 100%;
}

#projectsWorks_section > .projects_container > .project > .project_details > .project_name {
    font-weight: bold;
    font-size: 1.5rem;
    margin: 0;
}

#projectsWorks_section > .projects_container > .project > .project_details > .project_info {
    font-size: .75rem;
    margin-top: 1rem;
    line-height: 150%;
}

@media screen and (min-width: 769px) {
    #colourfit,
    #gallop,
    #peoplecars,
    #moviesapp {
        display:block;
    }

    #colourfit {
        background-image: url('../assets/projects_images/colourfit.png');
        background-size: cover;
        background-position: center;
    }

    #gallop {
        background-image: url('../assets/projects_images/gallop.png');
        background-size: cover;
        background-position:center;
    }

    #peoplecars {
        background-image: url('../assets/projects_images/people-cars.png');
        background-size: cover;
        background-position:center;
    }

    #moviesapp {
        background-image: url('../assets/projects_images/moviesApp.png');
        background-size: cover;
        background-position:center;
    }

    #snakegame {
        background-image: url('../assets/projects_images/snake-game.png');
        background-size: cover;
        background-position:center;
    }

    #projectsWorks_section {
        padding-bottom: 5rem;
    }

    #projectsWorks_section > h4 {
        color: white;
        font-size: 3rem;
        margin-bottom: 5rem;
    }

    #projectsWorks_section > .projects_container {
        padding: 2rem 3rem;
        box-shadow: inset 0 0 10px black;
    }

    #projectsWorks_section > .projects_container > .project {
        padding: 2rem 0;
        border-bottom: 1px solid black;
    }

    #projectsWorks_section > .projects_container > .project > div {
        width: 20%;
        height: 10rem;
    }

    #projectsWorks_section > .projects_container > .project > .project_details {
        width: 80%;
        padding-left: 2rem;
    }

    #projectsWorks_section > .projects_container > .project > .project_details > .project_name {
        font-size: 2rem;
    }

    #projectsWorks_section > .projects_container > .project > .project_details > .project_info {
        font-size: 1rem;
    }
}

</style>