<template>
    <section class="acoes">
            <button @click="($e) => $emit('opc','+')">+</button>
            <button @click="($e) => $emit('opc','-')">-</button>
            <button @click="($e) => $emit('opc','*')">*</button>
            <button @click="($e) => $emit('opc','/')">/</button>
            <button @click="($e) => $emit('opc','=')">=</button>
            <button @click="($e) => $emit('opc','C')">c</button>
    </section>
</template>
<style scoped>
    section{
        display: flex;
        justify-content: space-around;
        width:100%;
        height: 25%;
    }
    button{
        transition: 200ms;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
        color: white;
        background: #000;
        border: 1px solid white;
        border-radius: 10px;
        padding: 25px;
        margin:  10px;
        font-size: 25px;
    }
    button:hover{
        text-shadow: 0 0 10px white;
        box-shadow: inset 0 0 5px white;
    }
</style>