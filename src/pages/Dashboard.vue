<template>
  <div class="content">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <div class="md-layout">
      <div
        class="md-layout-item md-medium-size-50 md-xsmall-size-100 md-size-25"
      >
      
        <stats-card data-background-color="green">
          <template slot="header">
            <md-icon class="fa fa-clock-o"></md-icon>
          </template>

          <template slot="content">
            <p class="category">Total Submitted Hours</p>
            <h3 class="title">
              49 <small>Hours</small>
            </h3>
          </template>

          <template slot="footer">
            <div class="stats">
              <md-icon>access_time</md-icon>
              100% Completed
            </div>
          </template>
        </stats-card>
      </div>
      <div
        class="md-layout-item md-medium-size-50 md-xsmall-size-100 md-size-25"
      >
        <stats-card data-background-color="blue">
          <template slot="header">
            <md-icon class="fa fa-clock-o"></md-icon>
          </template>

          <template slot="content">
            <p class="category">Total Approved Hours</p>
            <h3 class="title">
              49
              <small>Hours</small>
            </h3>
          </template>

          <template slot="footer">
            <div class="stats">
              <md-icon>access_time</md-icon>
              100% Approved
            </div>
          </template>
        </stats-card>
      </div>
      <div
        class="md-layout-item md-medium-size-50 md-xsmall-size-100 md-size-25"
      >
        <stats-card data-background-color="orange">
          <template slot="header">
            <md-icon class="fa fa-clock-o"></md-icon>
          </template>

          <template slot="content">
            <p class="category">Total Hours Remaining</p>
            <h3 class="title">
              49
              <small>Hours</small>
            </h3>
          </template>

          <template slot="footer">
            <div class="stats">
              <md-icon>access_time</md-icon>
             100% Remaining
            </div>
          </template>
        </stats-card>
      </div>
      <div
        class="md-layout-item md-medium-size-50 md-xsmall-size-100 md-size-25"
      >
        <stats-card data-background-color="red">
          <template slot="header">
            <md-icon class="fa fa-clock-o"></md-icon>
          </template>

          <template slot="content">
            <p class="category">Required Hours</p>
            <h3 class="title">
              330
              <small>Hours</small>
            </h3>
          </template>

          <template slot="footer">
            <div class="stats">
              <md-icon>access_time</md-icon>
              Last Modified August 10th 2019 2:31 PM
            </div>
          </template>
        </stats-card>
      </div>
      <div
        class="md-layout-item md-medium-size-100 md-xsmall-size-100 md-size-33"
      >
        <chart-card
          :chart-data="dailySalesChart.data"
          :chart-options="dailySalesChart.options"
          :chart-type="'Line'"
          data-background-color="blue"
        >
          <template slot="content">
            <h4 class="title">Hours Submitted This Week</h4>
            <p class="category">
              
            </p>
          </template>

          <template slot="footer">
            <div class="stats">
              <md-icon>access_time</md-icon>
               Updated {{currentDate}}
            </div>
          </template>
        </chart-card>
      </div>
      <div
        class="md-layout-item md-medium-size-100 md-xsmall-size-100 md-size-33"
      >
        <chart-card
          :chart-data="emailsSubscriptionChart.data"
          :chart-options="emailsSubscriptionChart.options"
          :chart-responsive-options="emailsSubscriptionChart.responsiveOptions"
          :chart-type="'Bar'"
          data-background-color="red"
        >
          <template slot="content">
            <h4 class="title">Hours Submitted By Month</h4>
            <p class="category">
            </p>
          </template>

          <template slot="footer">
            <div class="stats">
              <md-icon>access_time</md-icon>
               Updated {{currentDate}}
            </div>
          </template>
        </chart-card>
      </div>
      <div
        class="md-layout-item md-medium-size-100 md-xsmall-size-100 md-size-33"
      >
        <chart-card
          :chart-data="dataCompletedTasksChart.data"
          :chart-options="dataCompletedTasksChart.options"
          :chart-type="'Line'"
          data-background-color="green"
        >
          <template slot="content">
            <h4 class="title">Total Hours By Week</h4>
            <p class="category">
              
            </p>
          </template>

          <template slot="footer">
            <div class="stats">
              <md-icon>access_time</md-icon>
               Updated {{currentDate}}
            </div>
          </template>
        </chart-card>
      </div>
      <div
        class="md-layout-item md-medium-size-100 md-xsmall-size-100 md-size-50"
      >
      </div>
    </div>
  </div>
</template>

<script>
import {
  StatsCard,
  ChartCard,
  NavTabsCard,
  NavTabsTable,
  OrderedTable
} from "@/components";

import moment from 'moment';

export default {
  components: {
    StatsCard,
    ChartCard,
    NavTabsCard,
    NavTabsTable,
    OrderedTable
  },
  data() {
    return {
      currentDate: moment().format('LLL'),
      dailySalesChart: {
        data: {
          labels: ["S","M", "T", "W", "T", "F", "S"],
          series: [[0, 8.5, 7.5, 9.5, 8.0, 8.5, 0]],
        },
        options: {
          lineSmooth: this.$Chartist.Interpolation.cardinal({
            tension: 0
          }),
          low: 0,
          high: 20, // creative tim: we recommend you to set the high sa the biggest value + something for a better look
          chartPadding: {
            top: 0,
            right: 0,
            bottom: 0,
            left: 0
          }
        }
      },
      dataCompletedTasksChart: {
        data: {
          labels: ["1","2","3","4","5","6","7","8","9","10","11","12"],
          series: [[40,40,40,24,39,32,23,25,6,23,33,23 ]]
        },

        options: {
          lineSmooth: this.$Chartist.Interpolation.cardinal({
            tension: 0
          }),
          low: 0,
          high: 60, // creative tim: we recommend you to set the high sa the biggest value + something for a better look
          chartPadding: {
            top: 0,
            right: 0,
            bottom: 0,
            left: 0
          }
        }
      },
      emailsSubscriptionChart: {
        data: {
          labels: [
            "Ja",
            "Fe",
            "Ma",
            "Ap",
            "Mai",
            "Ju",
            "Jul",
            "Au",
            "Se",
            "Oc",
            "No",
            "De"
          ],
          series: [[0, 0, 0, 0, 0, 160, 150, 140, 0, 0, 0, 0]]
        },
        options: {
          axisX: {
            showGrid: false
          },
          low: 0,
          high: 250,
          chartPadding: {
            top: 0,
            right: 5,
            bottom: 0,
            left: 0
          }
        },
        responsiveOptions: [
          [
            "screen and (max-width: 640px)",
            {
              seriesBarDistance: 5,
              axisX: {
                labelInterpolationFnc: function(value) {
                  return value[0];
                }
              }
            }
          ]
        ]
      }
    };
  }
};
</script>
