<template>
    <input :value="value" v-on:change="inputChanged" />
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
    name: "Input",
    props: {
        value: {
            type: String,
            default: ""
        }
    },
    methods: {
        inputChanged: function(e: any) {
            this.$emit("input-changed", e.target.value);
        }
    }
});
</script>
