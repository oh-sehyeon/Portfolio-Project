<template>
    <section id="contactme_section">
        <p class="contactme_text">Contact Me</p>
        <p class="contact_email">eden.cchord@gmail.com</p>
        <div class="sns_links">
            <a href="https://github.com/oh-sehyeon" id="github_link" target="_blank"><img src="../assets/sns_images/github.png" alt="Github Image"></a>
            <a href="https://www.linkedin.com/in/se-hyeon-oh/" id="linkedin_link" target="_blank"><img src="../assets/sns_images/linkedin.png" alt="Linkedin Image"></a>
        </div>
    </section>
</template>

<script>

export default {
    name: 'ContactMe',
}
</script>

<style scoped>

#contactme_section {
    position: relative;
    box-sizing: border-box;
    background-color: #FAFAFA;
    width: 100%;
    padding: 5rem 5%;
    box-shadow: inset 0 0 8px black;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

#contactme_section > .contactme_text {
    font-weight: bold;
    font-size: 2rem;
}

#contactme_section > .contact_email {
    font-size: 1.5rem;
    padding-top: 1rem;
}

#contactme_section > .sns_links {
    display: flex;
    flex-direction: row;
    margin-top: 1rem;
}

#github_link > img,
#linkedin_link > img {
    width: 5rem;
    height: 5rem;
    margin: 1rem;
}

@media screen and (min-width: 769px) {
    #contactme_section {
        box-sizing: border-box;
        background-color: #FAFAFA;
        width: 100%;
        padding: 5rem 5%;
        box-shadow: inset 0 0 8px black;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    #contactme_section > .contactme_text {
        font-weight: bold;
        font-size: 3rem;
    }

    #contactme_section > .contact_email {
        font-size: 2rem;
        padding-top: 1rem;
    }

    #contactme_section > .sns_links {
        display: flex;
        flex-direction: row;
        margin-top: 1rem;
    }

    #github_link > img,
    #linkedin_link > img {
        width: 8rem;
        height: 8rem;
        margin: 2rem;
    }
}

</style>