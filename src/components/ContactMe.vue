<template>
    <section id="contactme_section">
        <p class="contactme_text">Contact Me</p>
        <p class="contact_email">eden.cchord@gmail.com</p>
        <div class="sns_links">
            <a href="https://github.com/sehyeon-oh" id="github_link"><img src="../assets/sns_images/github.png" alt="Github Image"></a>
            <a href="https://www.linkedin.com/in/se-hyeon-oh/" id="linkedin_link"><img src="../assets/sns_images/linkedin.png" alt="Linkedin Image"></a>
        </div>

        <div class="animation-area">
            <ul class="box-area">
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
            </ul>
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

/* Bubble Animation Start */
.animation-area {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    margin: 0;
    padding: 0;
}

.box-area {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 100%;
    overflow: hidden;
    margin: 0;
}

.box-area li {
    position: absolute;
    display: block;
    list-style: none;
    width: 25px;
    height: 25px;
    background: rgba(248, 114, 114, 0.2);
    animation: animate 20s linear infinite;
    bottom: -150px;
    border-radius: 20%;
}

.box-area li:nth-child(1) {
    left: 86%;
    width: 80px;
    height: 80px;
    animation-delay: 0s;
}

.box-area li:nth-child(2) {
    left: 12%;
    width: 30px;
    height: 30px;
    animation-delay: 1.5s;
    animation-duration: 10s;
}

.box-area li:nth-child(3) {
    left: 70%;
    width: 100px;
    height: 100px;
    animation-delay: 5.5s;
}

.box-area li:nth-child(4) {
    left: 42%;
    width: 150px;
    height: 150px;
    animation-delay: 0s;
    animation-duration: 15s;
}

.box-area li:nth-child(5) {
    left: 65%;
    width: 40px;
    height: 40px;
    animation-delay: 0s;
}

.box-area li:nth-child(6) {
    left: 15%;
    width: 110px;
    height: 110px;
    animation-delay: 3.5s;
}

@keyframes animate {
    0% {
        transform: translateY(0) rotate(0deg);
        opacity: 1;
    }
    100% {
        transform: translateY(-1000px) rotate(360deg);
        opacity: 0;
    }
}
/* Bubble Animation End */

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