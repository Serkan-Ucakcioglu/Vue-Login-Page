<script lang="ts" setup></script>

<template>
  <div class="component--login">
    <div class="login-card">
      <header>
        <h5>Welcome Back !</h5>
        <p>Sign in to continue</p>
      </header>
      <div class="login-content">
        <div class="avatar">
          <img src="../assets/photo_2022-03-01_11-02-04.jpg" alt="" />
        </div>
        <form action="" @submit.prevent>
          <ul>
            <li>
              <label class="title" for="username">Username</label>
              <input type="text" id="username" placeholder="Enter username" />
            </li>
            <li>
              <label class="title" for="password">Password</label>
              <input
                type="password"
                id="password"
                placeholder="Enter password"
              />
            </li>
            <li>
              <label class="checkbox">
                <input type="checkbox" name="remember_me" value="1" />
                <span class="checkbox"></span>
                <span class="text">Remember me</span>
              </label>
            </li>
            <li>
              <button id="btn" type="submit">Log In</button>
              <a href="#" class="forgot-password">
                <img src="" alt="" />
                Forgot your password
              </a>
            </li>
          </ul>
        </form>
      </div>
    </div>
    <div class="login-text">
      <p>Don't have an account ? <a href="#">Signup now</a></p>
    </div>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;500&display=swap");

* {
  padding: 0;
  margin: 0;
  list-style: none;
  border: none;
  text-decoration: none;
  box-sizing: border-box;
  -webkit-overflow-scrolling: touch;
  font-family: "Poppins", sans-serif;

  &:focus {
    outline: 0;
  }
}

body {
  background: #f8f8fb;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  -webkit-font-smoothing: antialiased;
}

.component {
  &--login {
    $primary-color: #214247;
    width: 451px;
    margin: 0 15px;

    .login-card {
      border-radius: 4px;
      background: #fff;
      box-shadow: 0 12px 24px 0 rgba(#12263f, 0.05);
      overflow: hidden;
      margin-bottom: 36px;

      header {
        background: rgba($primary-color, 0.25) no-repeat right;
        height: 112px;
        padding: 24px;
        color: black;

        h5 {
          font-size: 16px;
          font-weight: 500;
          margin-bottom: 8px;
        }

        p {
          font-size: 13px;
        }
      }

      .login-content {
        padding: 0 28px 24px;

        .avatar {
          position: relative;
          top: -24px;
          margin-bottom: 8px;
          display: flex;
          justify-content: flex-start;

          img {
            border: 3px solid #f8f8fb;
            width: 72px;
            height: 72px;
            border-radius: 50%;
          }
        }

        ul {
          li {
            margin-bottom: 16px;

            &:last-child {
              margin-bottom: 0;
            }

            .title {
              display: block;
              color: #495057;
              font-size: 13px;
              font-weight: 500;
              margin-bottom: 8px;
              text-align: left;
            }

            input {
              width: 100%;
              height: 36px;
              border-radius: 4px;
              border: 1px solid #ced4da;
              padding: 0 12px;
              font-size: 13px;
              transition: 300ms border-color;

              &:focus {
                border-color: $primary-color;
                caret-color: $primary-color;
              }

              &::placeholder {
                color: #495057;
              }
            }

            > .checkbox {
              display: flex;
              align-items: center;
              cursor: pointer;

              .checkbox {
                width: 16px;
                height: 16px;
                border-radius: 4px;
                border: 1px solid #adb5bd;
                margin-right: 8px;
                display: flex;
                align-items: center;
                justify-content: center;
                transition: 300ms background-color, 300ms border-color;

                img {
                  height: 8px;
                }
              }

              .text {
                font-size: 13px;
                color: #495057;
                font-weight: 500;
              }

              input {
                display: none;

                &:checked + .checkbox {
                  background: $primary-color;
                  border-color: $primary-color;
                }
              }
            }

            button {
              height: 36px;
              border-radius: 4px;
              background:  #008CBA;
              color: #fff;
              width: 100%;
              cursor: pointer;
              font-size: 13px;
              transition: 300ms background-color;

              &:hover {
                background:  #05546e ;
              }
            }

            .forgot-password {
              display: flex;
              align-items: center;
              font-size: 13px;
              color: #74788d;
              justify-content: center;
              margin-top: 24px;
              transition: 300ms color;

              &:hover {
                color: darken(#74788d, 30%);
              }

              img {
                margin-right: 8px;
              }
            }
          }
        }
      }
    }

    .login-text {
      p {
        font-size: 13px;
        color: #495057;
        margin-bottom: 16px;
        text-align: center;

        a {
          color: $primary-color;
          font-weight: 500;

          &:hover {
            text-decoration: underline;
          }
        }

        &:last-child {
          margin-bottom: 0;
        }
      }
    }
  }
}
</style>
