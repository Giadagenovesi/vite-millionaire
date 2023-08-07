<script>
import AppHeader from "./components/AppHeader.vue";
import AppQuestion from "./components/AppQuestion.vue";
import AppFooter from "./components/AppFooter.vue";
import { store } from "./store";
import axios from "axios";




export default {
  components: { AppHeader, AppFooter, AppQuestion },

  data() {
        return {
            store,
            questions: [],
        };
    },
    mounted() {
        this.getQuestion()
    },

    methods: {
        getQuestion() {
            axios.get(this.store.apiUrl).then((resp)=> {
                this.questions = resp.data.results;
                console.log(resp.data.results);
            })
        }
    }
};
</script>

<template>
  <div class="ms_page_container">
    <AppHeader/>
    <AppQuestion/>
    <AppFooter/>

  </div>
</template>

<style lang="scss">
@use "./style/general.scss" as *;
.ms_page_container {
    background-color: #11093a;
    color: white;
    height: 100vh;
}

</style>