<template>
  <link
    href="https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css" rel="stylesheet">
  <title>Login</title>
  <main class="body">
  <div class="wrapper">
        <span class="animate"></span>

        <div class="form-box login">
            <h2 class="animation">Login</h2>
            <form action="">
                <div class="input-box animation">
                    <input type="text" required>
                    <label>Username</label>
                    <i class='bx bxs-user'></i>
                </div>

                <div class="input-box animation">
                    <input type="password" required>
                    <label>Password</label>
                    <i class='bx bxs-lock-alt' ></i>
                </div>
                <button type="submit" class="btn animation">Login</button>

                <div class="logreg-link animation">
                    <p>Vous n'avez pas de compte ? <a href="#/SignUp" class="register-link">Sign Up</a></p>
                </div>
            </form>
        </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}

.body{
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: #242423f1;
}

.wrapper{
    position: relative;
    width: 750px;
    height: 450px;
    background: transparent;
    border: 2px solid rgb(243, 243, 247);
    overflow: hidden;
    box-shadow: 0 0 25px rgb(73, 73, 73);
}

.wrapper .form-box{
    position: absolute;
    top: 0;
    width: 50%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.wrapper .form-box.login{
    left: 0;
    padding: 0 60px 0 40px;
}

.wrapper .form-box.login .animation{
    transform: translateX(0);
    transition: .7s ease;
}

.wrapper.active .form-box.login .animation{
    transform: translateX(-120%);
}


.form-box h2{
    font-size: 32px;
    color: #fff;
    text-align: center;
}

.form-box .input-box{
    position: relative;
    width: 100%;
    height: 50px;
    margin: 25px 0;
}

.input-box input{
    width: 100%;
    height: 100%;
    background: transparent;
    border: none;
    outline: none;
    border-bottom: 2px solid #fff;
    font-size: 16px;
    color: #fff;
    font-weight: 500;
    padding-right: 30px;
    transition: .5s;
}

.input-box input:focus,
.input-box input:valid{
    border-bottom-color: rgb(243, 243, 247);
}


.input-box label{
    position: absolute;
    top: 50%;
    left: 0;
    transform: translateY(-50%);
    font-size: 16px;
    color: #fff;
    pointer-events: none;
    transition: .5s;
}

.input-box input:focus~label,
.input-box input:valid~label{
    color: rgb(73, 73, 73);
    top: -1px;
}

.input-box i{
    position: absolute;
    top: 50%;
    right: 0;
    transform: translateY(-50%);
    font-size: 18px;
    color: #fff;
}

.input-box input:focus~i,
.input-box input:valid~i{
    color: rgb(73, 73, 73);
}

.btn{
    position: relative;
    width: 100%;
    height: 45px;
    background: transparent;
    border: 2px solid #ffffff;
    outline: none;
    border-radius: 40px;
    cursor: pointer;
    font-size: 16px;
    color: #fff;
    font-weight: 600;
    z-index: 1;
    overflow: hidden;
}
.btn::before{
    content: '';
    position: absolute;
    top: -100%;
    left: 0;
    width: 100%;
    height: 300%;
    z-index: -1;
    background: linear-gradient(#081b29, #ffffff, #081b29, #ffffff);
    transition: .5s;
}

.btn:hover::before{
    top: 0;
}

.form-box .logreg-link{
    font-size: 15px;
    color: #fff;
    text-align: center;
    margin: 20px 0 10px;
}

.logreg-link p a{
    color: #fff;
    text-decoration: none;
    font-weight: 600;
    font-size: 17px;
}

.logreg-link p a:hover{
    text-decoration: underline;
}

.wrapper .animate{
    position: absolute;
    top: -4px;
    right: 0;
    width: 850px;
    height: 600px;
    background: #C8AD7F;
    border-bottom: 3px solid #fff;
    transform-origin: bottom right;
    transform: rotate(10deg) skewY(40deg);
    /* transform: rotate(0) skewY(0); */
}
</style>
