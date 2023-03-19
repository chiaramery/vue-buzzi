<script>
export default {
    name: 'HomePage'
}
</script>

<template>
    <div id="home">
        <div class="row pt-5">
            <div class="text col-6">
                <p>
                    L'azienda Buzzi s.n.c. ha sede ad Ardea in provincia di Roma e da anni con professionalità e serietà si
                    occupa
                    di
                    trivellazioni, realizzazioni di pozzi artesiani e perforazioni.
                </p>
                <p>

                    L'azienda si avvale della collaborazione
                    di
                    un
                    team esperto e qualificato, garantendo massima serietà e professionalità nella realizzazioni delle
                    proprie
                    opere.
                </p>
            </div>
        </div>

    </div>
</template>

<style lang="scss">
#home {
    height: 100vh;
    background-image: url(../img/33.JPG);
    background-repeat: no-repeat;
    background-size: cover;

    .row {
        display: flex;
        justify-content: space-around;

        .text {
            background-color: rgb(11 113 184);
            color: white;

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
}
</style>