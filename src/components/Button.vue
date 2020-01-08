<template>
    <button @click="clicked">Add User</button>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
    name: "Button",
    methods: {
        clicked: function() {
            this.$emit("button-clicked");
        }
    }
});
</script>
