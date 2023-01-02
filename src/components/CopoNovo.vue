<template>
    <div id="novoCopo">
        <h2> Deseja adicionar um novo copo? {{ contagemCopo }} Copos </h2>
        <button type="button" @click="adicionarCopo"> Clique para adicionar um copo </button>
        <button type="button" @click="reiniciarNm"> Reiniciar Numero</button>

    </div>
</template>

<script>
export default {
     /* eslint-disable */
    data(){
        return {

        }
    },
    props: {
        contagemCopo: 0,
        reiniciarNm: Function
    },
    methods: {
        adicionarCopo(){
            this.contagemCopo++
            this.$emit('adicionandoMaisUmCopo', this.contagemCopo)
        }
    }
    
}
</script>

<style scoped>

</style>