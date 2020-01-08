<template>
    <div>
        <Users v-bind:users="usersList" />
        <Input v-bind:value="userToAdd" @input-changed="handleChange" />
        <Button @button-clicked="handleClicked" />
    </div>
</template>

<script>
// @ is an alias to /src
import Users from "@/components/Users.vue";
import Button from "@/components/Button.vue";
import Input from "@/components/Input.vue";

export default {
    name: "home",
    components: {
        Users,
        Button,
        Input
    },
    data: function() {
        return {
            usersList: ["Ash", "Brittany", "Jack", "Logan"],
            userToAdd: ""
        };
    },
    methods: {
        handleClicked: function() {
            this.userToAdd && this.usersList.push(this.userToAdd);
            this.userToAdd = "";
        },
        handleChange: function(value) {
            this.userToAdd = value;
        }
    }
};
</script>
