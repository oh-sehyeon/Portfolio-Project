<template>
    <section id="skillset_section">
        <h4 class="skill_text">
            Knowledge and Skillset to create any Application
        </h4>
        <div class="skillset_container">
            <div class="skill"><img src="../assets/skills/vue.png" alt="Vue Image"></div>
            <div class="skill"><img src="../assets/skills/react.png" alt="React Image"></div>
            <div class="skill"><img src="../assets/skills/node.png" alt="NodeJS Image"></div>
            <div class="skill"><img src="../assets/skills/swift.png" alt="Swift Image" class="resize"></div>
            <div class="skill"><img src="../assets/skills/java.png" alt="JAVA image"></div>
            <div class="skill"><img src="../assets/skills/mongoDB.png" alt="MongoDB Image" class="resize"></div>
            <div class="skill"><img src="../assets/skills/firebase.png" alt="Firebase Image"></div>
            <div class="skill"><img src="../assets/skills/sql.png" alt="SQL Image" class="resize"></div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'SkillSet',
}
</script>

<style scoped>

#skillset_section {
    background-color: #08090D;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 1rem 5% 5rem;
}

#skillset_section > .skill_text{
    text-align: center;
    font-size: 2.25rem;
    color: white;
    margin: 3rem 0 3rem;
    text-shadow: #DADADA 1px 0 12px;
    animation: glow 3s ease-in-out infinite alternate;
}

@keyframes glow {
    from {
        text-shadow: #DADADA 1px 0 5px;
    }
    to {
        text-shadow: #DADADA 1px 0 80px;
    }
}

#skillset_section > .skillset_container {
    background-color: #FAFAFA;
    display: grid;
    grid-template-columns: repeat(4, 1fr); /* 4 columns */
    grid-template-rows: repeat(2, 1fr); /* 2 rows */
    box-shadow: inset 0 0 8px black;
}

#skillset_section > .skillset_container > .skill {
    display: flex;
    justify-content: center;
    align-items: center;
    border: .5px solid grey;
}
#skillset_section > .skillset_container > .skill .resize {
    transform: scale(0.6);
}

#skillset_section > .skillset_container > .skill img {
    max-width: 100%;
    max-height: 100%;
    display: block;
}

@media screen and (min-width: 769px) {
    #skillset_section {
        padding: 5rem 0 10rem;
    }

    #skillset_section > .skill_text{
        font-size: 3rem;
        padding-bottom: 5rem;
        text-shadow: #DADADA 1px 0 40px;
    }

    #skillset_section > .skillset_container {
        margin: 0 5%;
        box-shadow: inset 0 0 10px black;
    }

    #skillset_section > .skillset_container > .skill {
        border: 1px dotted grey;
    }
}

</style>