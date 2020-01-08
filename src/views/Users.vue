<template>
    <div>
        <Users v-bind:users="usersList" />
        <Button @button-clicked="handleClicked" />
    </div>
</template>

<script>
// @ is an alias to /src
import Users from "@/components/Users.vue";
import Button from "@/components/Button.vue";

export default {
    name: "home",
    data: function() {
        return {
            usersList: ["Ash", "Brittany", "Jack", "Logan"]
        };
    },
    components: {
        Users,
        Button
    },
    methods: {
        handleClicked: function() {
            this.usersList.push("Some rando");
        }
    }
};
</script>
