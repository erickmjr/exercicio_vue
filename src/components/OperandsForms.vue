<template>

    <div class="mt-3">
        <form class="d-flex justify-content-around">
            <input class="form-control" type="number" placeholder="Operando 1" v-model="operand1">

            <select class="rounded" v-model="selectedOperation">
                <option value="?" disabled>?</option>
                <option value="+">+</option>
                <option value="-">-</option>
                <option value="/">/</option>
                <option value="*">*</option>
            </select>

            <input class="form-control" type="number" placeholder="Operando 2" v-model="operand2">
        </form>

        <Result
            :operand1="operand1"
            :operand2="operand2"
            :operation="selectedOperation"
        />
    </div>

</template>

<script>
    import Result from './Result.vue';

    export default {
        components: { Result },
        data() {
            return {
                operand1: null,
                operand2: null,
                selectedOperation: '?',
            }
        }
    }
</script>

<style scoped>
    select {
        max-width: fit-content;
        padding: 8px;
    }

    input {
        max-width: fit-content;
    }
</style>