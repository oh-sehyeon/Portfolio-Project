<template>
    <section id="banner_section">
        <div class="typed_out">
            <h1>Looking for a <br>Developer?</h1>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MainBanner',
}
</script>

<style scoped>

#banner_section {
    display: flex;
    justify-content: center;
    align-items: center;
    background-image: url('../assets/background.jpg');
    background-size: cover;
    height: 25rem;
    width: 100%;
    opacity: .7;
    box-shadow: inset 0 0 160px black;
}

#banner_section > div > h1 {
    font-weight: bold;
    font-size: 3rem;
    color: #FFFFFF;
}

.typed_out {
    overflow: hidden;
    white-space: nowrap;
    animation: 
        typing 4s forwards;
    width: 0;
}
@keyframes typing {
    from { width: 0 }
    to { width: 80%;}
}

@media screen and (min-width: 769px) {
    #banner_section {
        height: 40rem;
        box-shadow: inset 0 0 350px black;
    }

    #banner_section > div > h1 {
        font-size: 6rem;
    }

    @keyframes typing {
        from { width: 0 }
        to { width: 90%;}
    }
}
</style>

