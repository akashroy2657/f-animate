# f-animate
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>login form</title>
    <style>
       @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap');
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins',sans-serif; 
}
body{
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background:black;

}
.box{
    position: relative;
  width: 380px;
  height: 420px;
  background: black; 
  border-radius:8px ;
  overflow: hidden; 
}
.box::before{
     content:'';
     position: absolute;
     top:-50%;
     left:-50%;
     width:380px ;
     height: 420px;
     background: linear-gradient(0deg,transparent,#fa51fd,#fa51fd);
     transform-origin: bottom right;
     animation:animate 6s linear infinite;

}
.box::after{
    content:'';
    position: absolute;
    left: -50%;
    top:-50%;
    width: 380px;
    height: 420px;
    background: linear-gradient(0deg,transparent,#45f3ff,#45f3ff);
    transform-origin: bottom right;
    animation:animate 6s linear infinite;
    animation-delay: -3s;
  }
  @keyframes animate{
    0%{
        transform: rotate(0deg);
    }
    100%{
        transform: rotate(360deg);
    }
}
.form{
    position: absolute;
    inset: 3px;
    border-radius: 8px;
    background:black;
    z-index: 10;
    padding: 10px;
}
.txt{
    font-size: 25px;
    font-weight: bold;
    color:#16deec;
    width: 100%;
    text-align: center;

}
input{
    text-align: center;
    width:250px;
    height: 30px;
    border-radius: 5px;
    background-color: #16deec;
    margin-top: 20px;
}
.font{
    color:#fa51fd;
}
.btn{
    background-color: #16deec;
    padding: 5px;
    border-radius: 5px;
    text-align: end;
    margin-left: 80px;
    cursor: pointer;
}
.bn{
    width: 100%;
    margin-top: 20px;
    background-color: #16deec;
    border-radius: 15px;
    height: 30px;
    cursor: pointer;
}
.fn{
    color: #fa51fd;
    cursor: pointer;  
}
.pass{
    width: 100%;
    display: grid;
    grid-template-columns: 6fr 6fr;
    margin-top: 20px;
}
img{
    width: 300px;
    height: 160px;
    margin-left: 20px;
}
button:active{
    background-color:#20b8c3;
}
    </style>
</head>
<body>
    <div class="box">
        <div class="form">
            <div class="txt">
                Sign in
            </div>
            <input type="text"placeholder="Enter your Email"><span class="font"> :User Name</span>
            <input type="password"placeholder="Password"><span class="font"> :password</span>
            <button class="bn">Log In</button>
            <div class="pass">
                <div class="fn">Forgot Password?</div>
                <div>
                    <button class="btn">Sign Up</button>
                </div>
            </div>
            <div class="pic">
                <img src="hkr.jfif" alt="">
            </div>
        </div>
    </div>
</body>
</html>
