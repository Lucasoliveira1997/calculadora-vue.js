<template>
    <button class="button" 
            :class="{triple, double, operation}"
            @click="$emit('onClickCalcButton', label)">
        {{ label }}
    </button>
</template>

<script>
export default {
    props: {
        label: {},
        operation: Boolean,
        triple: Boolean,
        double: Boolean
    }
}
</script>

<style>
    .button {
        font-size: 1.4em;
        border: none;
        outline: none;
        background-color: #f0f0f0;
        border: solid 1px #888;
        border-right:  #f0f0f0;
        border-bottom:  #f0f0f0;
    }

    .button:active {
        background-color: #ccc;
    }

    .button.double {
        grid-column: span 2;
    }

    .button.triple {
        grid-column: span 3;
    }

    .button.operation {
        background-color: #fa8231;
        color: #fff;
    }

    .button.operation:active {
        background-color: #fa8231cc;
    }
</style>