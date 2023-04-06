<template>
    <h1>Calculadora</h1>
    <main>
        <Display 
            :valor=display
        />
        <Numbers
            @digitar="digitar"
        />
        <Actions 
            @opc="opc"
        />
    </main>
</template>

<style scoped>
    main{
        padding: 20px;
        width: 500px;
        height: 650px;
        background: #000;
        color: #fff;
    }

</style>
<script>

    export default{
        data(){
            return {
                equal:false,
                x:"",
                operation:"",
                display: ""
            }
        },
        methods: {
            digitar(valor){
               if(!this.equal){
                    this.display = this.display + valor;
               }else{
                    this.display = ''
                    this.operation = 0
                    this.x = 0
                    this.equal = false
                    this.display = this.display + valor;
               }
            },
            opc(opc){
                switch (opc) {
                    case 'C':
                        this.display = ''                        
                        break;
                    case '=':
                            switch (this.operation){
                                case '+':
                                    this.display = parseInt(this.x) + parseInt(this.display)
                                    this.x = ''
                                    this.equal = true
                                break;
                                case '-':
                                    this.display = parseInt(this.x) - parseInt(this.display)
                                    this.x = ''
                                    this.equal = true
                                break;
                                case '/':
                                    this.display = parseInt(this.x) / parseInt(this.display)
                                    this.x = ''
                                    this.equal = true
                                break;
                                case '*':
                                    this.display = parseInt(this.x) * parseInt(this.display)
                                    this.x = ''
                                    this.equal = true
                                break;
                            }
                        break;
                    default:
                        this.operation = opc
                        this.x = this.display
                        this.display = ''
                        break;
                }
            }
        }
    }
</script>
