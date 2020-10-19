<template>
  <div class="container">
    <header class="header">
      <div class="header__logo"><img src="" alt="logo"><h3>Boldseams Couture</h3></div>
      <div>
        <div class="header__nav">
          <div class="header__nav-img">
          <img src="~@/assets/images/notification.svg" alt="">
          <p>5</p>
          </div>
          <div class="header__nav-item">
            <p>Seun James</p>
            <a href="http://">Logout</a>
          </div>
        </div>
      </div>
    </header>

    <aside class="aside">
      <div class="aside__footer">
      <div class="aside__footer-item">
          <img src="" alt="logo">
        <h5>mzuri</h5>
      </div>
        <p>...Powering sustainable growth</p>
      </div>
    </aside>

    <main class="main">
      <div class="main__nav">
        <div class="main__nav-item">
          <p class="settings">Settings</p>
          <p class="user">User and Business Profiles</p>
        </div>
        <img src="~@/assets/images/information.svg" alt="">
      </div>
      <section class="profile">
        <div class="profile__title">
          <img src="" alt="logo">
          <h3>Boldseams Couture</h3>
        </div>
        <div class="profile__info">
          <div class="profile__info-title">
            <h5>My Profile</h5>
            <div>
              <button @click="passwordForm=true">Change Password</button>
              <button @click="showProfileForm=true">Edit</button>
            </div>
          </div>
          <div class="profile__info-form">
            <div>
            <h6>Name</h6>
            <p>Fariq</p>
          </div>
          <div>
            <h6>Email</h6>
            <p>abc@gmail.com</p>
          </div>
          <div>
            <h6>Phone Number</h6>
            <p>+234 222 333 443</p>
          </div>
          </div>
        </div>
      </section>
      <section class="business">
          <div class="business__info">
          <div class="business__info-title">
            <h5>Businesses</h5>
            <div class="business__info-button">
              <img src="~@/assets/images/add.svg" alt="icon">
              <button @click="showBusinessForm = true">Add Business</button>
            </div>
          </div>
          <div class="business__info-form">
            <div>
            <h6>Boldseams Stitches</h6>
            <p>RC-123456</p>
          </div>
          <div>
            <h6>East-West Farmers</h6>
            <p>BN-1234589</p>
          </div>
          <div>
            <h6>Mizzle Pharmaceuticals</h6>
            <p>RC-323902</p>
          </div>
          <div>
            <h6>Wigan Automobiles</h6>
            <p>BN-212994</p>
          </div>
          </div>
        </div>
      </section>
    </main>

      <modal v-if="showBusinessForm" @close="showBusinessForm = false">
        <div slot="header" class="modal__header">
          <h3>Add Business</h3>
          <img src="~@/assets/images/close.svg" alt="" @click="showBusinessForm = false">
        </div>
        <div slot="body">
          <form action="" class="form">
            <div class="form__title">
              <img src="" alt="logo">
              <h3>Boldseams Couture</h3>
            </div>
            <div class="form__input">
              <label for="name" >
                Business Name
              </label>
              <input type="text" name="" id="">
            </div>
            <div class="form__sides">
              <div class="form__input">
                <label for="number" >
                  Phone Number
                </label>
                <input type="text" name="" id="">
              </div>
              <div class="form__input">
                <label for="type" >
                  Business Type
                </label>
                <input type="text" name="" id="">
              </div>
            </div>
             <div class="form__sides">
              <div class="form__input">
                <label for="email" >
                  Email
                </label>
                <input type="email" name="" id="">
              </div>
              <div class="form__input">
                <label for="industry" >
                  Industry
                </label>
                <input type="text" name="" id="">
              </div>
            </div>
             <div class="form__sides">
              <div class="form__input">
                <label for="country" >
                  Country
                </label>
                <input type="text" name="" id="">
              </div>
              <div class="form__input">
                <label for="rcnumber" >
                  RC Number
                </label>
                <input type="text" name="" id="">
              </div>
            </div>
             <div class="form__sides">
              <div class="form__input">
                <label for="state" >
                  State
                </label>
                <input type="text" name="" id="">
              </div>
              <div class="form__input">
                <label for="local" >
                  Local Council
                </label>
                <input type="text" name="" id="">
              </div>
            </div>
            <div class="form__input">
                <label for="address" >
                  Business Address
                </label>
                <input type="text" name="" id="">
              </div>
              <button>Save</button>
          </form>
        </div>
      </modal>

      <modal v-if="showProfileForm" @close="showProfileForm = false">
        <div slot="header" class="modal__header">
          <h3>Edit Profile Details</h3>
          <img src="~@/assets/images/close.svg" alt="logo" @click="showProfileForm = false">
        </div>
        <div slot="body">
          <form action="" class="form">
            <div class="form__input">
              <label for="name" >
                First Name
              </label>
              <input type="text" name="" id="">
            </div>
            <div class="form__input">
              <label for="name" >
                Last Name
              </label>
              <input type="text" name="" id="">
            </div>
            <div class="form__input">
              <label for="email" >
                Email
              </label>
              <input type="email" name="" id="">
            </div>
             <div class="form__input">
              <label for="number" >
                Phone Number
              </label>
              <input type="text" name="" id="">
            </div>
              <button>Save</button>
          </form>
        </div>
      </modal>

      <modal v-if="passwordForm" @close="passwordForm = false">
        <div slot="header" class="modal__header">
          <h3>Change Password</h3>
          <img src="~@/assets/images/close.svg" alt="logo" @click="passwordForm = false">
        </div>
        <div slot="body">
          <form action="" class="form">
            <div class="form__input">
             
              <input type="text" name="" id="" placeholder="Old Password">
            </div>
            <div class="form__input">
              
              <input type="text" name="" id="" placeholder="New Password">
            </div>
          
             <div class="form__input">
              
              <input type="text" name="" id="" placeholder="Confirm Password">
            </div>
              <button @click.prevent="confirmPassword">Save</button>
          </form>
        </div>
      </modal>

       <modal v-if="otpVerification" @close="otpVerification = false">
        <div slot="header" class="modal__header">
          <h3>OTP Verification</h3>
          <img src="~@/assets/images/close.svg" alt="logo" @click="otpVerification = false">
        </div>
        <div slot="body">
          <form action="" class="form">
            <div class="form__otp">
              <p>An OTP code was sent to your phone and email, <br/> kindly input the code below</p>
              <div class="form__otp-code">
                <input type="text" name="" id="" maxlength="1">
                <input type="text" name="" id="" maxlength="1">
                <input type="text" name="" id="" maxlength="1">
                <input type="text" name="" id="" maxlength="1">
              </div>
            </div>
              <button @click.prevent="submitOtp">Submit</button>
          </form>
        </div>
      </modal>

       <modal v-if="successModal" @close="successModal = false">
        <div slot="header" class="modal__header">
          <h3>Success</h3>
          <img src="~@/assets/images/close.svg" alt="logo" @click="successModal = false">
        </div>
        <div slot="body">
          <form action="" class="form">
            <div class="form__success">
              <img src="" alt="logo">
              <h3>Congratulations!</h3>
              <p>Your password has been changed successfully</p>
            </div>
              <button @click="successModal = false">Continue</button>
          </form>
        </div>
      </modal>

  </div>
</template>

<script>
export default {
  name: 'HomePage',
  components: {
    Modal: () => import("@/components/Modal.vue"),
  },
  data(){
  return{
    showBusinessForm:false,
    showProfileForm:false,
    passwordForm:false,
    otpVerification:false,
    successModal:false
  }
},
  methods:{
    confirmPassword(){
      this.passwordForm=false
      this.otpVerification=true
    },
    submitOtp(){
      this.otpVerification=false
      this.successModal=true

    }
}
}
</script>

<style lang="scss">
@import "@/assets/scss/main.scss";
.container {
  display: grid;
  grid-template-areas:
    "header header"
    "nav main"
    "nav main";
  grid-template-rows: 60px auto;
  grid-template-columns: 10% 1fr;
  height: 100vh;
  margin: 0;

  .header {
  padding: $gap;
  grid-area: header;
  background: white;
  border-bottom: 0.5px solid #dadada;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #2c2c2c;
img{
  width: 25px;
  height: auto;
}
  &__logo{
    display: flex;
    img{
  font-size: 8px;
}
    h3{
      margin-left: $gap*2;
      font-size: 16px;
    }
  }
  &__nav{
    display: flex;
    justify-content: space-between;
    &-img{
      position: relative;
      img{
      }
      p{
        text-align: center;
        position: absolute;
        padding: $gap - .5;
        border-radius: 50%;
        background: red;
        width: 15px;
        height: 15px;
        top: -5px;
        right: 0;
        color: white;
        font-size: 10px;
        font-weight: 500;
      }
    }
    &-item{
      text-align: right;
      margin-left: $gap *3;
      p{
      color: #2c2c2c;
      font-size: 14px;

      }
      a{
      border-bottom: .5px solid rgb(25, 85, 197);
  font-size: 12px;
  color: rgb(25, 85, 197);

      }
    }
  }

  }
  .aside {
  grid-area: nav;
  background: rgb(25, 134, 197);
  position: relative;

  &__footer{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background: white;
    bottom: 0;
    position: absolute;
    width: 100%;
&-item{
  display: flex;
  justify-content: center;
  align-items: center;
img{
  font-size: 8px;
}
}
    p{
      font-size: 6px;
      color: #949393;
      margin-bottom: $gap - .2;
    }
    h5{
color: rgb(25, 134, 197);
font-size: 20px;

    }
}

  }

  .main {
  grid-area: main;
  background: rgb(246, 246, 246);
  &__nav{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: $gap - .7;
    margin-right: $gap;
    &-item{
        display: flex;
    justify-content: space-between;
    align-items: center;
      background: #f1eeee;
  width: 35%;
  border-radius: 6px;
  .settings{
clip-path: polygon(75% 0%, 85% 50%, 75% 100%, 0% 100%, 0 51%, 0% 0%);
    background: white;
      color: #949393;
  padding:  $gap $gap $gap $gap*5;
flex: 0 0 45%;
  }
  .user{
    flex-basis: 60%;
        text-align: center;
  padding: $gap;
          color: #949393;

  }
    }
  }
img{
  width: 25px;
  height: auto;
}
  .profile{
  padding: $gap*2;
margin-top: $gap*4;
    display: flex;
    flex-direction: column; 
    &__title{
      align-self: center;
      color: rgb(25, 134, 197);
      h3{
      font-weight: normal;
      font-size: 20px;
      padding: $gap*2 0;
      }
    }
    &__info{
      border: 1px solid #dadada;
      background: white;
      padding: $gap*2 $gap*5;
      margin: $gap*2 0;
      border-radius: 5px;
      &-title{
        display: flex;
        justify-content: space-between;
        margin-bottom: $gap;
        h5{
          color: #949393;
          font-size: 16px;
        }
        button{
  text-decoration: underline;
  margin-left: $gap*2;
}
      }
      &-form{
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;

        > * {
          flex: 0 0 45%;
          padding: $gap 0;
          h6{
            font-size: 14px;
          color: #949393;
          font-weight: normal;
          padding-bottom: $gap;
          }
          p{
          border-bottom: 1px solid #dadada;    
          font-size: 14px;
          color: #2c2c2c;
          padding-bottom: 2px;
           }
        }
      }
      button{
        outline: none;
        border: none;
        background: transparent;
        color: rgb(25, 134, 197);
        cursor: pointer;
      }
    }

  }

  .business{
  padding: $gap*2;

    &__title{
      align-self: center;
      color: rgb(25, 134, 197);
      h3{
      font-weight: normal;
      font-size: 20px;
      padding: $gap*2 0;
      }
    }
    &__info{
      border: 1px solid #dadada;
      background: white;
      padding: $gap*2 $gap*5;
      margin: $gap*2 0;
      border-radius: 5px;
      &-title{
        display: flex;
        justify-content: space-between;
        margin-bottom: $gap;
        h5{
          color:  rgb(25, 134, 197);
          font-size: 16px;
        }
        button{
        margin-left: $gap;
      }
      }
      &-button{
        display: flex;
        justify-content: space-between;
        align-items: center;
        img{
          width: 20px;
        }
      }
      &-form{
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;

        > * {
          flex: 0 0 45%;
          padding: $gap - .2 $gap;
          border: 1px solid #dadada;
          margin: $gap 0;
          border-radius: 2px;

          h6{
            font-size: 14px;
          color: rgb(25, 134, 197);
          font-weight: 500;
          padding-bottom: $gap - .2;
          }
          p{
          font-size: 14px;
          color: #949393;
           }
        }
      }
      button{
        outline: none;
        border: none;
        background: transparent;
        color: rgb(25, 134, 197);
        cursor: pointer;
      }
    }
  }
  }

  .form{
      max-width: 600px;
      margin: 0 auto;
      padding: 0 1rem;
      display: flex;
      flex-direction: column;
      &__title{
        align-self: center;
        color: rgb(25, 134, 197);
        margin-bottom: $gap*2;
        h3{
        font-weight: normal;
        font-size: 20px;
        padding: $gap*2 0;
        }
      }
      &__sides{
        display: flex;
        justify-content: space-between;
        align-items: center;
        > * {
          flex: 0 0 48%;
        }
      }
    &__input{
      position: relative;
      margin-bottom: $gap *2;
      label{
        color: #949393;
        font-size: 12px;
        display: block;
        margin: 0 $gap;
        padding: 0 2px;
        background: white;
        z-index: 2;
        width: fit-content;
        position: absolute;
        top: -8px;
      }
      input{
        display: block;
        padding: .5rem $gap;
        background: transparent;
        vertical-align: middle;
        width: 100%;
        max-width: 100%;
        border: 1px solid #cdcdcd;
        border-radius: 4px;
        font-size: 14px;
        color: #2c2c2c;

        &:focus{
          outline: none;
        border: 1px solid rgb(25, 134, 197);
        }
      }
    }

    &__otp{
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      p{
        font-size: 14px;
        color: #2c2c2c;
        text-align: center;
      }
      &-code{
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: nowrap;
        width: 50%;
        margin: $gap * 2 0;
        input{
          width: 3rem;
          height: 3rem;
          font-size: 18px;
          padding: $gap;
        color: #2c2c2c;
        border: 0.5px solid #dadada;
        border-radius: 2px;
        &:focus{
          outline: none;
        border: 0.5px solid #dadada;

        }

        }
      }
    }

    &__success{
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      color: #2c2c2c;

      img{
        margin-top: $gap *2 ;

      }
      h3{
        font-size: 20px;
        margin: $gap *2 0;
        font-weight: 500;
      }
      p{
        font-size: 14px;
      color: #474747;
margin-bottom: $gap*2;
      }
    }
    button{
      margin: $gap*2 0;
      padding: $gap $gap*5;
      border: none;
      outline: none;
      color: white;
      // width: 10%;
      align-self: center;
      background: rgb(25, 134, 197);
      border-radius: 5px;

    }
  }
  .modal{
    &__header{
      display: flex;
      justify-content: space-between;
      align-items: center;
      img{
        font: 6px;
        cursor: pointer;
        width: 12px;
        height: auto;
      filter: invert(1);
        
      }
    }
  }
}
</style>