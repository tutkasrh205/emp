<template>
    <div class="header">
        <div class="headercontent">Employee Master</div>
        <button class="headercontent switchbtn" @click="toggle"> Switch Themes</button>
    </div>
</template>

<script>
export default {
    name: 'Header',
    methods: {
        // siwtch theme toggle function
        toggle() {
            var element = document.body;
            element.classList.toggle("dark-mode");
        }
    }

}
</script>

<style >
.header {
    display: flex;
    justify-content: space-between;
    width: 73rem;
    height: 10rem;
    top: 36px;
    left: 227px;
    border-radius: 8px;
    border: 1px;

}

.headercontent {
    width: 289px;
    height: 41px;
    top: 42px;
    left: 227px;
    font-family: 'Roboto';
    font-size: 35px;
    font-weight: 700;
    line-height: 41px;
    letter-spacing: 0.03em;
    text-align: left;
    color: #4A4A4A;
    margin-top: 40px;
    margin-left: 40px;



}

.switchbtn {
    cursor: pointer;
    width: auto;
    height: 22px;
    top: 51px;
    left: 1198px;
    font-family: Roboto;
    font-size: 19px;
    font-weight: 500;
    line-height: 22px;
    letter-spacing: 0.02em;
    text-align: left;
    color: #000000;
    border: none;



}

.dark-mode {
    .outerbox {
        background: #0C060E;

    }

    .sidebaar {
        background: #702F6145;

    }

    .userinfo {
        background: #110D15;

    }

    .view {
        background: #110D15;

    }

    .headercontent {
        color: #F1F1F1;

    }

    .employeeinfo {
        color: #FFFFFF;

    }

    .editbtn {
        color: #FFFFFF;

    }

    .status {
        color: #FFFFFF;

    }

    .text {
        color: #FFFFFF;
    }

    .btn2text {
        color: #FFFFFF;
    }

    .viewemployeebox {
        color: #F8F8F8;

    }

    .editbtntext {
        color: #FFFFFF;

    }

    .switchbtn {
        color: #FFFFFF;
        background-color: #0C060E;

    }
}

@media only screen and (max-width: 600px) {
    .header {
        width: 350px;
        height: 120px;
        flex-direction: column;
        justify-content: start;

    }

    .headercontent {
        width: 350px;
        height: 35px;
        font-size: 30px;
        letter-spacing: 0.0em;
        line-height: 0px;
        display: flex;
        align-items: center;
        margin-left: 80px;
    }

    .switchbtn {
        width: 350px;
        height: 4px;

    }

}
</style>