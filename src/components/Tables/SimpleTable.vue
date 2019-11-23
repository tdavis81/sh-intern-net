<template>
  <div>
    <md-table v-model="users" :table-header-color="tableHeaderColor">
      <md-table-row slot="md-table-row" slot-scope="{ item }">
        <md-table-cell md-label="Week" style="text-align:center">{{item.city}}</md-table-cell>
        <md-table-cell md-label="Date" style="text-align:left">{{ item.country }}</md-table-cell>
        <md-table-cell style="text-align:center" md-label="Sun">
          <md-field :md-counter="false" style="width:100%;text-align:center">
            <label>Sun</label>
            <md-input oninput="javascript: if (this.value.length > this.maxLength) this.value = this.value.slice(0, this.maxLength);"
            type = "number"
            maxlength = "2" style="width:100%"></md-input>
          </md-field>
        </md-table-cell>
        <md-table-cell style="text-align:center" md-label="Mon">
          <md-field :md-counter="false"  style="width:100%">
            <label>Mon</label>
            <md-input oninput="javascript: if (this.value.length > this.maxLength) this.value = this.value.slice(0, this.maxLength);"
            type = "number"
            maxlength = "2" style="width:100%"></md-input>
          </md-field>
        </md-table-cell>
        <md-table-cell  md-label="Tue">
          <md-field :md-counter="false" style="width:100%">
            <label>Tue</label>
            <md-input oninput="javascript: if (this.value.length > this.maxLength) this.value = this.value.slice(0, this.maxLength);"
            type = "number"
            maxlength = "2" style="width:100%"></md-input>
          </md-field>         
        </md-table-cell>
        <md-table-cell  md-label="Wed">
          <md-field :md-counter="false" style="width:100%">
            <label>Wed</label>
            <md-input oninput="javascript: if (this.value.length > this.maxLength) this.value = this.value.slice(0, this.maxLength);"
            type = "number"
            maxlength = "2" style="width:100%"></md-input>
          </md-field>          
        </md-table-cell>
        <md-table-cell md-label="Thu">
          <md-field :md-counter="false" style="width:100%" >
            <label>Thu</label>
            <md-input oninput="javascript: if (this.value.length > this.maxLength) this.value = this.value.slice(0, this.maxLength);"
            type = "number"
            maxlength = "2" style="width:100%"></md-input>
          </md-field>          
        </md-table-cell>
        <md-table-cell md-label="Fri">
          <md-field :md-counter="false" style="width:100%" class="hourInput">
            <label>Fri</label>
            <md-input oninput="javascript: if (this.value.length > this.maxLength) this.value = this.value.slice(0, this.maxLength);"
            type = "number"
            maxlength = "2" style="width:100%"></md-input>
          </md-field>          
        </md-table-cell>
        <md-table-cell md-label="Sat">
          <md-field :md-counter="false" style="width:100%" class="hourInput">
            <label>Sat</label>
            <md-input oninput="javascript: if (this.value.length > this.maxLength) this.value = this.value.slice(0, this.maxLength);"
            type = "number"
            maxlength = "2" style="width:100%"></md-input>
          </md-field>          
        </md-table-cell>
        <md-table-cell md-label="Actions">
          <i style="color:green;cursor:pointer;" class="material-icons">
            check_box
            <md-tooltip md-direction="top">Submit Hours</md-tooltip>
          </i>
          <i style="color:red;cursor:pointer;" class="material-icons">
            refresh
            <md-tooltip md-direction="top">Reset Hours</md-tooltip>
          </i>
        </md-table-cell>
      </md-table-row>
    </md-table>
  </div>
</template>

<script>
export default {
  name: "simple-table",
  props: {
    tableHeaderColor: {
      type: String,
      default: ""
    }
  },
  data() {
    return {
      selected: [],
      users: [
        {
          name: "Dakota Rice",
          salary: "$36,738",
          country: "8/11/2019",
          city: "1"
        },
        {
          name: "Minerva Hooper",
          salary: "$23,738",
          country: "12/11/2019",
          city: "2"
        },
        {
          name: "Sage Rodriguez",
          salary: "$56,142",
          country: "8/11/2019",
          city: "3"
        },
        {
          name: "Philip Chaney",
          salary: "$38,735",
          country: "8/11/2019",
          city: "4"
        },
        {
          name: "Doris Greene",
          salary: "$63,542",
          country: "8/11/2019",
          city: "5"
        },
        {
          name: "Mason Porter",
          salary: "$78,615",
          country: "8/11/2019",
          city: "6"
        },
        {
          name: "Mason Porter",
          salary: "$78,615",
          country: "8/11/2019",
          city: "7"
        },
        {
          name: "Mason Porter",
          salary: "$78,615",
          country: "8/11/2019",
          city: "8"
        },
        {
          name: "Mason Porter",
          salary: "$78,615",
          country: "8/11/2019",
          city: "9"
        },
        {
          name: "Mason Porter",
          salary: "$78,615",
          country: "8/11/2019",
          city: "10"
        },
        {
          name: "Mason Porter",
          salary: "$78,615",
          country: "8/11/2019",
          city: "11"
        },
        {
          name: "Mason Porter",
          salary: "$78,615",
          country: "8/11/2019",
          city: "12"
        }
      ]
    };
  }
};
</script>


<style>
.hourInput {
  width:50%
}
</style>