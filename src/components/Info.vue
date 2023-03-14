<template>
    <div id="info">
        <h2 class="roles-h">ROLES</h2>
        <div>
            <h6>Read the instructions carefully before beginning the quiz to understand the rules and objectives.</h6>
            <h6>Answer all questions to the best of your ability before proceeding to the next question.</h6>
            <h6>You cannot go back to previous questions once you have answered them.</h6>
            <h6>The questions may be presented in a random order, so be prepared for any question to come up at any time.</h6>
            <h6>There may be a time limit for completing the quiz, so work efficiently and manage your time wisely.</h6>
            <h6>Once you have completed the quiz, you will be able to see your score and the correct answers to each question.</h6>
            <h6> Take note of any incorrect answers and learn from them for future quizzes.</h6>
        </div>
       <button @click="onStepChanged('QUIZ')">TAKE THE QUIZ</button> 
    </div> 
</template>

<script>
export default {
    data(){
        return {
            
        }
    },
    methods:{
        onStepChanged(step) {
            this.$emit('step-changed', step);
        },
    }
    
}
</script>

<style>
#info{
    height: 80vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 2em 0;
}
.roles-h{
    color: #00ba92;
}
#info h6{
    color: #00ba92;
    margin: .6em 0;
}
#info div{
    margin: 3em auto;
}
#info button{
    width: 200px;
    margin: auto;
}
</style>