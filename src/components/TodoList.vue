<template>
    <div class="container">
        
        <input v-model="conteudoInput" type="text" class="entrada">
        <button id="inserir" @click="inserir()">ADD</button>
       
        <ul class="lista">
            <li v-for="(nota, index) in notas" :key="index"><span>{{nota.texto}}</span><button @click="apagar(index)">X</button></li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'TodoList',
        data(){
            return {
                conteudoInput: '',
                notas: [
                    {texto: "teste de texto 1"},
                ]
            }
        },
        methods:{
            apagar(index){
                this.notas.splice(index,1)
            },
            inserir(){
                console.log(this.conteudoInput)
                if(this.conteudoInput === '') return
                this.notas.push({texto: this.conteudoInput})

                this.conteudoInput = ''
            }

        }
    }
</script>

<style scoped>
</style>
