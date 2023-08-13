<template>

<div class="outerbox">
  <div >    
  <Sidebaar/>
     </div>
  <div style="display: flex; flex-direction: column;"> 
    <div> <Header/> </div>
    <div class="employeediv">
      <div>  <AddEmployee v-show="view" @add-employee="addemployee"></AddEmployee></div>
      <Edit v-show="!view" :employee="employee"/>
      <div>  <ViewEmployee 
  
 
  :Employee="Employees"
  
  @view="viewemployee"

  
  ></ViewEmployee></div>

    </div>
  </div>
</div>

 
  



  

   
</template>

<script>

import AddEmployee from "./components/AddEmployee.vue";
import ViewEmployee from "./components/ViewEmployee.vue";
import Edit from "./components/Edit.vue"
import Sidebaar from "./components/Sidebaar.vue"
import Header from "./components/Header.vue"

export default {
  name: 'App',
  components: {
   
    AddEmployee,
    ViewEmployee,
    Edit,
    Sidebaar,
    Header
  },
  data(){
    return {
      Employees:[
        
      ],
      employee:{},

      view:true,
     
    }
  },
 
  methods:{
    addemployee(displayname,loginid, password, status){
     
      const newemployee={
        id:loginid,
        displayname:displayname,
        loginid:loginid,
        password:password,
        status:status
      }
      this.Employees.push(newemployee)
    
    },

    viewemployee(ID){
     this.employee= this.Employees.filter(
        (emp) => emp.id === ID)

        this.employee=this.employee[0]
        this.view=!this.view
        
    }
  }
}
</script>


<style>
 @import url('https://fonts.googleapis.com/css2?family=Roboto&family=Ubuntu:ital,wght@0,300;0,400;1,300;1,700&display=swap');
  .outerbox {
    width: 1440px;
height: 1024px;
top: -522px;
left: -730px;

            background: #F2F1FA;
            display: flex;

        }
        .employeediv {
            display: flex;
            justify-content: space-evenly;
            margin-left: 30px;
        }

        @media only screen and (max-width: 600px) {
            .outerbox {
                width: 600px;
                height: 1000px;
                flex-direction: column;
                
            }
            .employeediv {
         
                flex-direction: column;
                margin-left: 12px;
             

            }

          }
       

</style>
