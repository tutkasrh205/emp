<template>
    <div class="view">

        <div style="display: flex; justify-content: space-evenly;">
            <div class="viewemployeebox">
                View Employee ({{ Employee.length }})

            </div>



            <input class="searchbox" type="search" placeholder="Search" v-model="search" aria-label="Search">





        </div>
        <div v-for="employee in employeelist" :key="employee.id">
            <EmployeeBox :employee="employee" @xyz="abc" />

        </div>
    </div>
</template>

<script>
import EmployeeBox from './EmployeeBox.vue';

export default {

    emits: ["view",],
    components: {
        EmployeeBox,
        EmployeeBox
    },
    data() {
        return {
            search: ''

        }
    },
    props: {
        id: '',
        displayname: '',
        Employee: ''

    },
    methods: {
        abc(id) {
            this.$emit('view', id)
        }

    },
    computed: {

        employeelist() {
            if (this.search.trim().length > 0) {
                return this.Employee.filter((res) => res.displayname.includes(this.search.trim()))

            }
            return this.Employee
        }

    }



}
</script>

<style scoped >
.view {
    display: flex;
    flex-direction: column;


    width: 33.75rem;
    height: 39.625rem;
    top: 211px;
    left: 860px;
    border-radius: 29px;
    border: 1px;
    background: white;
    border: 1px solid #E1E1E1;
    box-shadow: 0px 2px 9px 1px #00000014;
    overflow: auto;
    margin-left: 30px
}

.viewemployeebox {
    width: 305.49798583984375px;
    height: 35px;
    top: 265px;
    left: 900.8764953613281px;
    font-family: Roboto;
    font-size: 30px;
    font-weight: 700;
    line-height: 35px;
    letter-spacing: 0.03em;
    text-align: left;
    color: #4A4A4A;
    margin-bottom: 40px;

    margin-top: 40px;


}

.searchbox {
    width: 151px;
    height: 46px;
    top: 261px;
    left: 1216px;
    border-radius: 8px;

    border: 1px solid #0c0c0c;
    margin-bottom: 40px;

    margin-top: 40px;

}

@media only screen and (max-width: 600px) {
    .view {


        margin-left: 0px;
        margin-top: 10px;
        width: 300px;
        height: 20rem;
        margin-top: 10px;
        margin-left: 30px;

    }

    .viewemployeebox {
        width: 200px;
        height: 10px;
        font-size: 20px;
      

    }

    .searchbox {
        width: 70px;
        height: 30px;
    }


}
</style>