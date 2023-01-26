<template>

<div class="container" @click.self="closeModal">
    <div class="center" >

      <div>
        <form method="post">
          <div class="txt-field">
            <input type="text" id="username" required>
            <span></span>
            <label for="username">Username</label>
          </div>
  
          <div class="txt-field">
            <input type="text" id="message" required>
            <span></span>
            <label for="message">Message</label>
          </div>
  

          <input type="submit" value="Send">
        </form>    
      </div>
    </div>
</div>
</template>

<script>
export default {

}
</script>

<style>
body {
  margin: 0;
  padding: 0;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  height: 100vh;
}
.container {
  position: fixed;
  top: 0;
  left: 0;
  background-color: rgba(0, 0, 0, 0.3);
  width: 100vw;
  height: 100vh;
  opacity: 1;
  justify-content: center;
  align-items: center;
  display: flex;
  overflow: hidden;
}

.show {
  display: flex;
  background: #f6f9fc;
  border-top-right-radius: 5px;
  border-top-left-radius: 5px;
  height: 70px;
  border-bottom: 1px solid #e2e9f0;
  align-items: center;
}
.close-window {
  position: absolute;
  left: 475px;
  top: 5px;
}
.close-window i {
  font-size: 20px;
  color: #555;
  cursor: pointer;
}
#close-window {
  display: none;
}
.show-login {
  flex: 50%;
}
.show p {
  padding: 14px 25px;
  border-radius: 5px;
  border: none;
  outline: none;
  color: #4b566b;
  background: transparent;
  cursor: pointer;
  font-size: 18px;
  margin-top: 5px;
  margin-left: 50px;
  transition: .5s;
}
.show p:hover {
  color: #fe696a;
}
.clicked {
  color: #fe696a;
  border-bottom: 2px solid black;
}
.clicked p {
    color: #fe696a;

}
.show-signup {
  flex: 50%;
}
.center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 500px;
  background: white;
  border-radius: 10px;
  box-shadow: 1px 5px 3px rgba(0, 0, 0, 0.3);
}
      
.bar {
  background-color: #666666;
  width: 100%;
  height: 50px;
}
.center h1 {
  text-align: center;
  padding: 0 0 20px 0;
  border-bottom: 1px solid silver;
}
.center form {
  padding: 0 40px;
  box-sizing: border-box;
}

form .txt-field {
  position: relative;
  border-bottom: 2px solid #adadad;
  margin: 30px 0;
}

.txt-field input {
  width: 100%;
  padding: 0 5px;
  height: 40px;
  font-size: 16px;
  border: none;
  background: none;
  outline: none;
}
.txt-field label {
  position: absolute;
  top: 50%;
  left: 5px;
  color: #adadad;
  transform: translateY(-50%);
  font-size: 16px;
  pointer-events: none;
  transition: .5s;
}
.txt-field span::before {
  content: '';
  position: absolute;
  top: 40px;
  left: 0;
  width: 0%;
  height: 2px;
  background: #fe696a;
  transition: .5s;
}
.txt-field input:focus ~ label,
.txt-field input:valid ~ label {
  top: -5px;
  color: #fe696a;
}

.txt-field input:focus ~ span::before,
.txt-field input:valid ~ span::before {
  width: 100%;
}

.pass {
  margin: -5px 0 20px 5px;
  color: #4b566b;
  cursor: pointer;
  text-align: center;
}
.pass:hover {
  text-decoration: underline;

}
      input[type='submit'] {
  width: 100%;
  height: 50px;
  border: 1px solid;
  background: #fe696a;
  border-radius: 10px;
  font-size: 18px;
  color: #e9f4fb;
  font-weight: 700;
  cursor: pointer;
  outline: none;
  margin-bottom: 30px;
}
      input[type='submit']:hover {
  border-color: #fe696a;
  transition: .5s;
}
.signup-link {
  margin: 30px 0;
  text-align: center;
  font-size: 18px;
  color: #666666;
}
.signup-link a {
  color: #fe696a;
  text-decoration: none;
}
</style>