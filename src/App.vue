<template>
  <div>
    <info
      @step-changed="onStepChanged"
      ></info>
    <stepper 
      :steps="steps"
    ></stepper>
  </div>
</template>

<script>
import Stepper from "./components/Stepper.vue";
import Quiz from "./components/Quiz.vue";
import Results from "./components/Results.vue";
import Info from "./components/Info.vue";
export default {
  components: {
    Info,
    Stepper,
    Quiz,
    Results,
  },
  data(){
    return {
      steps : [
        {
          name : 'INFO',
          icon : '<i class="bi bi-info-circle-fill"></i>',
          active: true
        },
        {
          name : 'QUIZ',
          icon : '<i class="bi bi-question-circle-fill"></i>',
          active: false
        },
        {
          name : 'RESULTS',
          icon : '<i class="bi bi-check-circle-fill"></i>',
          active: false
        },
        
      ],
    }
  },
  methods:{
    onStepChanged(step) {
      this.step = step;
      this.steps.forEach(s => {
        s.active = s.name === this.step;
      });
    },
  }

}
</script>

<style>

</style>