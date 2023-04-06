<template>
    <section class="botoes">
            <div>
                <button @click="($e) => $emit('digitar',1)">1</button>
                <button @click="($e) => $emit('digitar',2)">2</button>
                <button @click="($e) => $emit('digitar',3)">3</button>
            </div>
            <div>
                <button @click="($e) => $emit('digitar',4)">4</button>
                <button @click="($e) => $emit('digitar',5)">5</button>
                <button @click="($e) => $emit('digitar',6)">6</button>
            </div>
            <div>
                <button @click="($e) => $emit('digitar',7)">7</button>
                <button @click="($e) => $emit('digitar',8)">8</button>
                <button @click="($e) => $emit('digitar',9)">9</button>
            </div>
            <div>
                <button @click="($e) => $emit('digitar',0)">0</button>
            </div>
        </section>
</template>
<style scoped>
    section{
        height: 65%;
        border: 1px solid white;
    }
    div{
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