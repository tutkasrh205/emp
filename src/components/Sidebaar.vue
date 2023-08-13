<template>
    <div class="sidebaar">

        <div class="box">
            <div class="icon"> <i class="fa-solid fa-gauge fa-2xl"></i></div>
            <div class="icontext">Dashboard</div>
        </div>

        <div class="box">
            <div class="icon"> <i class="fa-brands fa-product-hunt text-white fa-2xl"></i></div>
            <div class="icontext">Products & Modules</div>
        </div>

        <div class="box">
            <div class="icon"> <i class="fa-regular fa-user fa-2xl"></i></div>
            <div class="icontext">User</div>
        </div>
        
        <div class="box">
            <div class="icon"><i class="fa-solid fa-address-card text-white fa-2xl"></i></div>
            <div class="icontext">Registrations</div>
        </div>
        
        <div class="box">
            <div class="icon"><i class="fa-solid fa-file-invoice text-white fa-2xl"></i></div>
            <div class="icontext">Invoice</div>
        </div>

        <div class="box">
            <div class="icon"><i class="fa-solid fa-credit-card text-white fa-2xl"></i></div>
            <div class="icontext">Payments</div>
        </div>

        <div class="box">
            <div class="icon"><i class="fa-regular fa-thumbs-up text-white fa-2xl"></i></div>
            <div class="icontext">Approve</div>
        </div>

    </div>
</template>
<Script>
     
</Script>
<style>
.sidebaar {
    width: 186px;
    height: 1024px;
    border-radius: 0px 25px 25px 0px;
    background: #702F61;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.box {
    display: flex;
    flex-direction: column;
    margin-bottom: 50px;
}

.icon {
    height: 29px;
    top: 212px;
    left: 78px;
    border-radius: 6px;
    color: #FFFFFF;
    text-align: center;
}
.icontext {
    width: auto;
    height: auto;
    top: 252px;
    left: 54px;
    font-family: 'Roboto';
    font-size: 16px;
    font-weight: 400;
    line-height: 19px;
    letter-spacing: 0em;
    text-align: center;
    color: #FFFFFF;
}

@media only screen and (max-width: 600px) {
    .sidebaar {
        width: 390px;
        height: 50px;
        flex-direction: row;
        justify-content: start;
    }

    .icon {
        line-height: 70px;
        margin-left: 20px;
    }
    .icontext {
        display: none;
    }
}
</style>