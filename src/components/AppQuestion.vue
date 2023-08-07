<script>
import axios from "axios";
import { store } from "../store";

export default {
    name: "AppQuestion",

    // data() {
    //     return {
    //         store,
    //         questions: [],
    //     };
    // },
    // mounted() {
    //     getQuestion()
    // },

    // methods: {
    //     getQuestion() {
    //         axios.get(this.store.apiUrl).then((resp)=> {
    //             this.questions = resp.data.request;
    //             console.log(resp.data.request);
    //         })
    //     }
    // }
}


</script>

<template>
    <div class="q_container">
        <h1 class="text-center">Question</h1>
        <main>
            <div class="ms_question">
                <p>Questa è la mia domanda</p>
            </div> 
            <div class="ms_answer my-4">
                <div> <span>A.</span> Risposta</div>
                <div> <span>B.</span> Risposta</div>
            </div>
            <div class="ms_answer">
                <div> <span>C.</span> Risposta</div>
                <div> <span>D.</span> Risposta</div>
            </div>
        </main>
    </div>
</template>

<style lang="scss" scoped>
.q_container {
    height: 55%;
    padding: 3rem 0;
}

main {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 1rem 0;

    
    .ms_question {
        width: 35%;
        border: 2px solid white;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 1rem 0;

        p {
            margin: 0;
            vertical-align: top;
        }
    }
    .ms_answer {
        display: flex;
        justify-content: space-around;
        width: 60%;

        div {
            border: 2px solid white;
            width: 45%;
            text-align: center;
            padding: .8rem 2rem;
        }
    }
}
</style>