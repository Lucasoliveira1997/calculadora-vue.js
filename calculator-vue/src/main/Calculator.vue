<template>
    <div class="calculator">
        <Display value="1260"/>
        <Button label="AC" triple @onClickCalcButton="clearMemory"/>
        <Button label="/" operation @onClickCalcButton="setOperation"/>
        <Button label="7" @onClickCalcButton="addDigit"/>
        <Button label="8" @onClickCalcButton="addDigit"/>
        <Button label="9" @onClickCalcButton="addDigit"/>
        <Button label="*" operation @onClickCalcButton="setOperation"/>
        <Button label="4" @onClickCalcButton="addDigit"/>
        <Button label="5" @onClickCalcButton="addDigit"/>
        <Button label="6" @onClickCalcButton="addDigit"/>
        <Button label="-" operation @onClickCalcButton="setOperation"/>
        <Button label="1" @onClickCalcButton="addDigit"/>
        <Button label="2" @onClickCalcButton="addDigit"/>
        <Button label="3" @onClickCalcButton="addDigit"/>
        <Button label="+" operation @onClickCalcButton="setOperation"/>
        <Button label="0" double @onClickCalcButton="addDigit"/>
        <Button label="." @onClickCalcButton="addDigit"/>
        <Button label="=" operation @onClickCalcButton="setOperation"/>
    </div>
</template>

<script>
import Button from '../components/Button'
import Display from '../components/Display'

export default {
    components: { Button, Display },

    methods: {
        clearMemory() {
            console.log('AC')            
        },
        setOperation(operation) {
            console.log(operation)            
        },
        addDigit(n) {
            console.log(n)            
        }
    },
}
</script>

<style>
    .calculator {
        height: 320px;
        width: 235px;
        border-radius: 5px;
        overflow: hidden;

        display: grid;
        grid-template-columns: repeat(4, 25%);
        grid-template-rows: 1fr 48px 48px 48px 48px 48px;
    }
</style>