<script>
export default {
    name: 'HomePage'
}
</script>

<template>
    <div class="row pt-5">
        <div class="text col-6">
            <p>
                L'azienda Buzzi s.n.c. ha sede ad Ardea in provincia di Roma e da anni con professionalità e serietà si
                occupa
                di
                trivellazioni, realizzazioni di pozzi artesiani e perforazioni. L'azienda che si avvale della collaborazione
                di
                un
                team esperto e qualificato, garantisce massima serietà e professionalità nella realizzazioni delle proprie
                opere.
            </p>
        </div>
        <div class="img col-6">
            <img src="../img/1.JPG" alt="">
        </div>
    </div>
</template>

<style lang="scss">
.row {
    display: flex;
    justify-content: space-around;

    .text {
        p {
            font-size: 2em;
        }
    }

    .img {
        img {
            width: 400px;
        }
    }
}
</style>