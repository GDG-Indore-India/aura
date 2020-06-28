<template>
  <v-container fluid class="py-0 my-0">
    <v-row align="center" justify="center" class="py-0 my-0">
      <v-col cols="12" md="12" lg="12" sm="12" class="py-0 my-0">
        <h3 class="google-font team-heading">Organizing Team Members</h3>
      </v-col>
    </v-row>
    <v-row align="center" justify="center" class="py-0 my-0">
      <v-col cols="12" md="12" lg="12" sm="12" class="py-0 my-0">
        <v-row class="py-0 my-0">
          <v-col md="6" lg="3" sm="12" cols="12" class="pa-1 team-card" v-for="(item,i) in data" :key="i">
            <organizingTeamList :data="item" />
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "OrganizingTeam",
  inject: ['theme'],
  props: ["data"],
  components: {
    organizingTeamList:()=>import('@/components/team/OrganizingTeamList')
  },
  data: () => ({}),
  methods: {},
    filters:{
        summery: (val,num)=>{
            return val.substring(0,num)+".."
        }
    }
};
</script>
