<template>
    <section id="career_section">
        <div v-for="(job, index) in jobs" :key="index" class="job">
            <img :src="job.logo" :alt="job.companyName + ' Logo'">
            <div class="job_details">
                <span class="job_title">{{ job.title }}</span>
                <span class="job_period">{{ job.period }}</span>
                <span class="tech_used">{{ job.techUsed }}</span>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'ProCareer',
    data() {
        return {
            jobs: [
                {
                    companyName: 'Valtech',
                    logo: require('../assets/job_logos/valtech_logo.png'),
                    title: 'Frontend Developer',
                    period: '2021 - 2022',
                    techUsed: 'Vue, Node JS, Sass, GIT, Bitbucket, JIRA, Fractal, Unicorn'
                },
                {
                    companyName: 'LG CNS',
                    logo: require('../assets/job_logos/lg-cns-logo.png'),
                    title: 'Junior System Analyst',
                    period: '2019 - 2021',
                    techUsed: 'PHP, Java, HTML, CSS, JavaScript, PLSQL, JIRA, TortoiseSVN'
                },
                {
                    companyName: 'LG CNS',
                    logo: require('../assets/job_logos/lg-cns-logo.png'),
                    title: 'Support and Infra Assistant',
                    period: '2017 - 2019',
                    techUsed: 'VPN management, Hardware issue troubleshooting, N/W issue management, OS image creation, User support'
                }
            ]
        };
    }
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
    box-sizing: border-box;
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
    line-height: 150%;
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