<template>
  <div class="container">
    <div class="row">
      <div class="col-lg-12">
        <h1>AktivBo List</h1>

        <input v-model="search" class="form-control" placeholder="Filter by survey type">

        <table class="table table-striped">
          <thead>
            <tr>
              <th v-for="(value, column) in columns" v-bind:key="column">
                <a href="#" @click="changeSort(column)">
                  {{ value }}
                </a>
              </th>
            </tr>
          </thead>

          <tbody>
            <tr v-for="data in orderedList" v-bind:key="data.project_id">
              <td>{{ data.project_status }}</td>
              <td>{{ data.survey_type }}</td>
              <td>{{ data.project_name }}</td>
              <td>{{ data.respondent_count }}</td>
              <td>{{ data.date_start }}</td>
              <td>{{ data.date_end }}</td>
              <td>{{ data.integration }}</td>
              <td>{{ data.answer_rate_latest }}</td>
              <td>&#11088;</td>
            </tr>
          </tbody>

        </table>

      </div>
    </div>
  </div>
</template>

<script>
import json from '../json/aktivbo.json'
import _ from 'lodash'

export default {
  name: 'Container',

  computed: {
    orderedList: function () {
      var search = this.search
      var filteredList =  _.filter(this.jsonData, function(o) {
        if(o.survey_type.toLowerCase().includes(search.toLowerCase())){
          return o.survey_type
        }
      })
      return _.orderBy(filteredList, this.sortBy, this.descAsc)
    }
  },

  data: function() {
    return {
      sortBy:"",
      descAsc: 'asc',
      order: true,
      search: '',
      columns: {
          project_status : 'Project Status',
          survey_type : "Survey Type",
          project_name : "Project Name",
          respondent_count : "Respondent Count",
          date_start : "Start Date",
          date_end : "End Date",
          integration : "Integration",
          answer_rate_latest : "Answer Rate"
      },
      jsonData: json.data.listSurveys

    };
  },

  methods: {
    changeSort: function(newSort) {
      this.sortBy = newSort
      this.order = !this.order;
      this.descAsc = this.order ? 'desc' : 'asc';
    },
    addFavorite: function() {

    }
  }
}
</script>

<style scoped>
a {
  color: #42b983;
}
td {
  text-align: left;
}
</style>
