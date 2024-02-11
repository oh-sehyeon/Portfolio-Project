<template>
    <section id="aboutme_section">
        <div class="picture_container">
            <img src="../assets/profile_pic.jpg" alt="Se Hyeon's Profile Picture">
        </div>
        <div class="aboutme_content">
            <h3>&emsp;As a lifelong technology enthusiast, my journey has been marked by continuous exploration and learning in the ever-evolving world of technology. Since embarking on my IT career in 2017, my primary passions have centered around Front-End and Web Development. My academic achievements include a Bachelor's degree in System Information from São Paulo University (USP, Brazil) and a Postgraduate Diploma in Web & Mobile Development from Langara College in Vancouver, BC.</h3>
        </div>
    </section>
</template>

<script>
export default {
    name: 'AboutMe',
}
</script>

<style scoped>

#aboutme_section {
    background-color: #030303;
    width: 100%;
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 3rem 5% 2rem;
}

#aboutme_section > .picture_container {
    width: 80%;
}

#aboutme_section > .picture_container > img {
    width: 100%;
    border-radius: 50%;
}

#aboutme_section > .aboutme_content {
    padding: 1rem 0 0 0;
}

#aboutme_section > .aboutme_content > h3 {
    color: #B5B6B7;
    font-weight: lighter;
    font-size: 1rem;
    letter-spacing: .3px;
}

@media screen and (min-width: 769px) {
    #aboutme_section {
        flex-direction: row;
        padding: 5rem 5%;
    }

    #aboutme_section > .picture_container {
        width: 100%;
    }

    #aboutme_section > .picture_container > img {
        width: 100%;
    }

    #aboutme_section > .aboutme_content {
        padding: 0 0 0 5%;
    }

    #aboutme_section > .aboutme_content > h3 {
        font-size: 1.2rem;
    }
}

</style>