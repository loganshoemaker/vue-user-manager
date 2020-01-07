<template>
    <div>
        <h1>These are your users</h1>
        <h3 v-for="(user, index) in users" v-bind:key="index">
            {{ user }}
        </h3>
        <button>Add User</button>
    </div>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
    name: "Users",
    props: {
        users: {
            type: Array,
            default: () => []
        }
    }
});
</script>
