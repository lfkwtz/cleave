# Vue Input Mask

```html
<template>
    <vue-input-mask :options="{
            creditCard: true,
            onCreditCardTypeChanged: onCreditCardTypeChanged
        }"
        v-model="number"
        id="ccnumber"
        name="ccnumber"
        autocomplete="cc-number"
        type="tel"
    ></vue-input-mask>
</template>

<script>
import vueInputMask from 'vue2-input-mask';

export default {
    components: {
        VueInputMask,
    },
    data() {
        return {
            number: '',
        }
    },
    methods: {
        onCreditCardTypeChanged: (type) => {
            this.type = type;
        }
    }
</script>
```