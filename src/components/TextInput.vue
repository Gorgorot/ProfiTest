<template>
    <div class="text-input">
        <input type="text" :placeholder="placeholder"/>
        <div class="text-input__marker"></div>
    </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
    name: 'TextInput',
    props: {
        placeholder: String,
    },
});
</script>

<style scoped lang="scss">
    .text-input {
        position: relative;
        margin-bottom: 16px;

        &__marker {
            position: absolute;
            width: 12px;
            height: 12px;
            background: #0D0F5A;
            border-radius: 2px;
            transform: matrix(0.71, 0.69, -0.73, 0.71, 0, 0);
            left: 12px;
            bottom: -5px;
        }
        input {
            display: inline-block;
            width: 100%;
            font-size: 16px;
            border: 1px solid #EAEAEA;
            border-radius: 2px;
            outline: 0;
            padding: 20px 16px;

            &:focus {
                border: 1px solid rgba(251, 177, 67, 0.5);
                box-shadow: 0px 0px 20px rgba(251, 177, 67, 0.2);
            }
        }

        @media (min-width: 320px) {
            max-width: 320px;
        }
    }
</style>
