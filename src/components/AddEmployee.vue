<template>
  <!-- addemployee box -->
  <div class="userinfo">

    <div style="display: flex; justify-content: space-around;   margin-bottom: 40px; margin-top: 40px;">
      <div class="employeeinfo">Employee Info</div>
    </div>

    <div style="display: flex; flex-direction: column; align-items: center;">

      <input class="pla" type="text" placeholder="Display Name" v-model="displayname">
      <input class="pla" type="email" placeholder="LoginId" v-model="loginid">
      <input class="pla" type="password" placeholder="Password" v-model="password">

      <div class="pla" style="display: flex; justify-content: space-between; border:none">
        <div class="status">Status</div>

        <label class="switch">
          <input type="checkbox" v-model="status">
          <span class="slider round"></span>
        </label>

        <div class="active">Active</div>
      </div>

    </div>
    <div style="display: flex; justify-content: center;">
      <button type="button" v-on:click="submitdata" class="btn">
        <div class="btntext">Save</div>
      </button>
    </div>





  </div>
</template>

<script>
export default {
  name: 'AddEmployee',
  emits: ["add-employee"],
  data() {
    return {
      displayname: '',
      loginid: '',
      password: '',
      status: 'true',

    }
  },
  methods: {
    submitdata() {

      this.$emit('add-employee', this.displayname, this.loginid, this.password, this.status)
      this.displayname = ''
      this.loginid = ''
      this.password = ''
      this.status = 'true'

    }

  }
}
</script >

<style scoped >
.userinfo {
  width: 37.3125rem;
  height: 39.625rem;
  top: 211px;
  left: 227px;
  border-radius: 29px;
  border: 1px;
  background: white;
  border: 1px solid #E1E1E1;
  box-shadow: 0px 2px 9px 1px #00000014;
}

.employeeinfo {
  width: 204px;
  height: 35px;
  top: 264px;
  left: 286px;
  font-family: Roboto;
  font-size: 30px;
  font-weight: 700;
  line-height: 35px;
  letter-spacing: 0.03em;
  text-align: left;
  color: #4A4A4A;
}
.pla {
  width: 476px;
  height: 64px;

  border-radius: 8px;
  border: 1px;
  border: 1px solid #E9E9E9;
  margin-bottom: 15px;

}
.status {
  width: 59px;
  height: 22px;
  top: 598px;
  left: 286px;
  font-family: Roboto;
  font-size: 19px;
  font-weight: 700;
  line-height: 22px;
  letter-spacing: 0.03em;
  text-align: left;
  color: #313333;
  margin-right: 250px;
}
.switch {
  position: relative;
  display: inline-block;
  width: 47px;
  height: 26px;
}

.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}

.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #ccc;
  -webkit-transition: .4s;
  transition: .4s;
}

.slider:before {
  position: absolute;
  content: "";
  height: 26px;
  width: 26px;

  background-color: #702F61;

  box-shadow: 1px 1px 4px 0px #0000006E;

  ;
  -webkit-transition: .4s;
  transition: .4s;
}

input:checked+.slider {
  background-color: #702F61;
  ;
}

input:focus+.slider {
  box-shadow: 0 0 1px #2196F3;
}

input:checked+.slider:before {
  -webkit-transform: translateX(26px);
  -ms-transform: translateX(26px);
  transform: translateX(26px);
}

/* Rounded sliders */
.slider.round {
  border-radius: 34px;
}

.slider.round:before {
  border-radius: 50%;
}

.active {
  width: 56px;
  height: 22px;
  top: 600px;
  left: 706px;
  font-family: Roboto;
  font-size: 19px;
  font-weight: 400;
  line-height: 22px;
  letter-spacing: 0.03em;
  text-align: left;
  color: #313333;

}

.btn {
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 229px;
  height: 67px;
  top: 694px;
  left: 417px;
  background: #702F61;
  border-radius: 40px;
}

.btntext {
  width: 57px;
  height: 26px;
  top: 714px;
  left: 503px;
  font-family: Roboto;
  font-size: 22px;
  font-weight: 700;
  line-height: 26px;
  letter-spacing: 0.03em;
  text-align: left;
  color: #FFFFFF;
}


@media only screen and (max-width: 600px) {

  .userinfo {
    width: 300px;
    height: 20rem;
    margin-top: 20px;
    margin-left: 30px;


  }

  .employeeinfo {
    width: 200px;
    height: 10px;
    font-size: 20px;
    line-height: 10px;

  }

  .pla {
    width: 250px;
    height: 30px;

  }

  .status {
    width: 20px;
    height: 10px;
    font-size: 15px;
    margin-right: 150px;
  }

  .switch {
    width: 20px;
    height: 15px;
  }

  .slider:before {
    width: 15px;
    height: 15px;
  }

  input:checked+.slider:before {
    -webkit-transform: translateX(10px);
    -ms-transform: translateX(10px);
    transform: translateX(10px);
  }

  .active {
    width: 20px;
    height: 10px;
    font-size: 15px;

  }

  .btn {
    width: 100px;
    height: 30px;
  }

  .btntext {
    width: 30px;
    height: 15px;
    font-size: 15px;
    line-height: 15px;

  }


}</style>