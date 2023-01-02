<template>
    <div id="Copo">
        <LeiteNoCafe :leiteCafe="leiteCafe" @jogarForaOcafe="leiteCafe = $event"/>
        <button type="button" @click="adicionarCafe"> Clique para adicionar o café </button>

        <CopoNovo :contagemCopo="contagemCopo" @adicionandoMaisUmCopo="contagemCopo = $event" :reiniciarNm="reiniciarNumero"/> <!-- Aqui eu to passando
         no reiniciarNm o uma function que eu clico no botão no CopoNovo que é o filho dele.cal-->
        <button type="button" @click="zerarCopos"> Clique para diminuir 1 copo</button>

    </div>
    
</template>

<script>
import LeiteNoCafe from './LeiteNoCafe.vue';
import CopoNovo from './CopoNovo.vue'
export default {
    components: {
        LeiteNoCafe,
        CopoNovo
    },
    data(){
        return {
            leiteCafe: '',
            contagemCopo: 0
        }
    },
    methods: {
        adicionarCafe(){
            this.leiteCafe = "Cafe adicionado"

        },
        zerarCopos(){
            this.contagemCopo--
        },
        reiniciarNumero(){
            this.contagemCopo = 0
        }


    }
    
}
</script>

<style scoped>

</style>