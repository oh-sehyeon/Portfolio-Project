<template>
    <section id="career_section">
        <div class="job">
            <img src="../assets/job_logos/valtech_logo.png" alt="Valtech Logo">
            <div class="job_details">
                <span class="job_title">Frontend Developer</span>
                <span class="job_period">2021 - 2022</span>
                <span class="tech_used">Vue, Node JS, Sass, GIT, Bitbucket, JIRA, Fractal, Unicorn</span>
            </div>
        </div>
        <div class="job">
            <img src="../assets/job_logos/lg-cns-logo.png" alt="LG CNS Logo">
            <div class="job_details">
                <span class="job_title">Junior System Analyst</span>
                <span class="job_period">2019 - 2021</span>
                <span class="tech_used">PHP, Java, HTML, CSS, JavaScript, PLSQL, JIRA, TortoiseSVN</span>
            </div>
        </div>
        <div class="job">
            <img src="../assets/job_logos/lg-cns-logo.png" alt="LG CNS Logo">
            <div class="job_details">
                <span class="job_title">Support and Infra Assistant</span>
                <span class="job_period">2017 - 2019</span>
                <span class="tech_used">VPN managenment, Hardware issue troubleshooting, N/W issue management, OS image creation, User support</span>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'ProCareer',
}
</script>

<style scoped>

#career_section {
    box-sizing: border-box;
    background-color: #FAFAFA;
    width: 100%;
    padding: 2rem 5%;
    box-shadow: inset 0 0 8px black;
}

#career_section > .job {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: center;
    border-bottom: 1px solid black;
    padding: 1rem 1rem 1rem 0;
}

#career_section > .job:last-child {
    border-bottom: none;
}

#career_section > .job > img {
    width: 25%;
}

#career_section > .job > .job_details {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    margin-left: 1rem;
}

#career_section > .job > .job_details >
.job_title,
.job_period {
    margin-bottom: 0.2rem;
}
#career_section > .job > .job_details > .job_title {
    font-weight: bold;
    font-size: .9rem;
}

#career_section > .job > .job_details >
.job_period,
.tech_used {
    font-size: .7rem;
}

#career_section > .job > .job_details > .tech_used {
    font-style: italic;
}

@media screen and (min-width: 769px) {
    #career_section {
        padding: 5rem 5%;
        box-shadow: inset 0 0 10px black;
    }

    #career_section > .job {
        padding: 1rem;
    }
    #career_section > .job > img {
        width: 15%;
    }

    #career_section > .job > .job_details {
        margin-left: 3rem;
    }

    #career_section > .job > .job_details >
    .job_title,
    .job_period {
        margin-bottom: .25rem;
    }
    #career_section > .job > .job_details > .job_title {
        font-size: 1.25rem;
    }

    #career_section > .job > .job_details >
    .job_period,
    .tech_used {
        font-size: 1rem;
    }
}

</style>