<template>
    <div class="employeebox">

        <div><img class="profile" src="../assets/profile.jpeg" alt=""></div>

        <div class="text"> {{ employee.displayname }}</div>
        <div> <button type="button" @click="$emit('xyz', employee.id)" class="btn2">
                <div class="btn2text">View</div>
            </button>
        </div>


    </div>
</template>

<script>
export default {
    emits: ['xyz'],
    name: "EmployeeBox",
    props: {
        employee: ''
    }


}
</script>

<style scoped>
.employeebox{
    display: flex;
     justify-content: space-evenly;
      margin-bottom: 30px;
}

.profile {
    width: 62.390438079833984px;
    height: 58px;
    top: 741px;
    left: 902px;
    border-radius: 50px;

}

.text {
    width: 112.94820404052734px;
    height: 22px;
    top: 759px;
    left: 993.4342651367188px;
    font-family: Roboto;
    font-size: 19px;
    font-weight: 700;
    line-height: 50px;
    letter-spacing: 0.03em;
    text-align: center;
    color: #212121;
    margin-left: -40px;



}

.btn2 {
    cursor: pointer;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 167.8087615966797px;
    height: 47px;
    top: 746px;
    left: 1190.2868347167969px;
    border-radius: 9px;
    background: #702F61;
    margin-left: 20px;

}

.btn2text {
    width: 46.254981994628906px;
    height: 22px;
    top: 376px;
    left: 1249.4501953125px;
    font-family: Roboto;
    font-size: 19px;
    font-weight: 400;
    line-height: 22px;
    letter-spacing: 0.03em;
    text-align: left;
    color: #FFFFFF;


}

@media only screen and (max-width: 600px) {

    .employeebox{
    
      margin-bottom: 10px;
}
    .profile {
        width: 60px;
        height: 50px;
    }

    .text {
        width: 80;
        height: 16;
        font-size: 15;
        line-height: 30px;
    }

    .btn2 {
        width: 80px;
        height: 25px;
    }

    .btn2text {
        width: 30px;
        height: 15px;
        font-size: 15px;
        line-height: 15px;
    }
}</style>