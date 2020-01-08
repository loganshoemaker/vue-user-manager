<templat>
    <button>Add User</button>
</template>


<script lang="ts">
import Vue from "vue";
export default Vue.extend({
    name: "Button",
    props: {
        handleOnClick: () => any,
        text: string,
    }
});
</script>