<script>
export default {
    name: "AppFooter"
}
</script>

<template>
    <footer>
        <div class="logo">
            <img src="../img/30.JPG" alt="">
        </div>
        <h3>Per avere un preventivo gratuito contattaci:</h3>
        <ul>
            <li>
                <i class="fa-solid fa-phone"></i>
                347 479 5593
            </li>
            <li>
                <i class="fa-solid fa-phone"></i>
                389 664 3102
            </li>
        </ul>
    </footer>
</template>

<style lang="scss">
footer {
    display: flex;
    align-items: center;
    justify-content: space-around;
    background-color: rgb(11 113 184);
    color: white;

    .logo {
        img {
            padding: 2em;
            width: 200px;
        }
    }

    ul {
        list-style: none;
    }
}
</style>