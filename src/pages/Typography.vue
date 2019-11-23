<template>
  <div class="content">
    <div class="md-layout">
      <div class="md-layout-item">
        <md-card>
          <md-card-header data-background-color="green">
            <h4 class="title">Summaries</h4>
            <p class="category">Here is where you enter your summaries.</p>
          </md-card-header>
          <md-card-content>
            <md-field>
              <label>What major objectives/goals did you or your supervisor set for the week? (You should set a new goal every week for something to learn, progress in your
              job search, ideas to proposed, etc.) Did you successfully accomplish these goals?: </label>
              <md-textarea></md-textarea>
            </md-field>

            <md-field>
              <label>
                What additional accomplishments and tasks were performed this week? This could include routine tasks, project/assignment completion, a new skill
                learned, time spent observing, etc.:
              </label>
              <md-textarea></md-textarea>
            </md-field>

            <md-field>
              <label>
                What tasks would you like to perform but have not been assigned?:
              </label>
              <md-textarea></md-textarea>
            </md-field>

            <md-field>
              <label>
                What activity do you feel you handled especially well this week?:Have your supervisor and/or co-workers been helpful? Discuss any human relations
problems or issues you have witnessed or been involved with.: 
              </label>
              <md-textarea></md-textarea>
            </md-field>

            <md-field>
              <label>
                Explain any problems you faced this week and how you solved them or plan to solve them.: 
              </label>
              <md-textarea></md-textarea>
            </md-field>

            <md-field>
              <label>
                Explain one thing you learned this week, whether it is a new task, a human relations revelation, workplace/career information, or anything at all pertaining
to your career/internship.: 
              </label>
              <md-textarea></md-textarea>   
            </md-field>
            <div class="md-layout-item md-size-100 text-right">
              <md-button class="md-raised md-success">Submit Summary</md-button>
            </div>
          </md-card-content>
        </md-card>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    dataBackgroundColor: {
      type: String,
      default: ""
    }
  }
};
</script>
