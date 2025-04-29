<template>
    <div class="mt-5 fs-4 container justify-content-center text-light d-flex ">
        <div class="text-light p-3 align-items-center">
            {{ operand1 }}
        </div> 
        <div class="text-light p-3">
            {{ operation }}
        </div> 
        <div class="text-light p-3">
            {{ operand2 }}
        </div> 

        <div class="py-3">=</div> 

        <div class="text-light p-3" v-if="!(operand1 == null || operand2 == null)">
            {{ getResult }}
        </div>
    </div>
</template>

<script>

    export default {
        props: [
            'operand1',
            'operand2',
            'operation'
        ],

        computed: {
            getResult() {
                return this.makeOperation();
            }
        },

        methods: {
            makeOperation() {
                switch(this.operation) {
                    case '+':
                        return (this.operand1 + this.operand2)
                    case '-':
                        return (this.operand1 - this.operand2);
                    case '*':
                        return (this.operand1 * this.operand2);
                    case '/':
                        return (this.operand1 / this.operand2);
                    
                    default: 
                        return null
                }
            }
        }
    }
</script>
