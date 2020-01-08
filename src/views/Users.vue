<template>
    <Users v-bind:users="usersList" />
</template>

<script>
// @ is an alias to /src
import Users from "@/components/Users.vue";

export default {
    name: "home",
    data: function() {
        return {
            usersList: ["Ash", "Brittany", "Jack", "Logan"]
        };
    },
    components: {
        Users
    }
};
</script>
