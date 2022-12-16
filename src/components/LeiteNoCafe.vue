<template>
    <div id="leiteCafe">
        <h1> Bem vindo ao Leite No Cafe: {{ leiteCafe }} </h1>
        <button type="button" @click="retirarCafe"> Clique para jogar o cafe fora</button>
        <hr>

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
        leiteCafe: ''
    },
    methods: {
        retirarCafe(){
            this.leiteCafe = "Cafe foi jogado fora!"
            this.$emit('jogarForaOcafe', this.leiteCafe)
        }
    }
    
}
</script>

<style scoped>

</style>