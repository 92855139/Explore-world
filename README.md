<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Explore world </title><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" integrity="sha512-DTOQO9RWCH3ppGqcWaEA1BIZOC6xxalwEsw9c2QQeAIftl+Vegovlnee1c9QX4TctnWMn13TZye+giMm8e2LwA==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <style>
        *{
            margin: 0px;
            padding: 0px;
            background-image: url();
        }
    
        @keyframes backgroundZoom {
            0% { transform: scale(1); }
            100% { transform: scale(1.1); }
        }
        .login-container {
            background: rgba(255, 255, 255, 0.9);
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            width: 350px;
            transition: transform 0.3s;
            animation: fadeIn 1s ease-in-out;
            position: absolute;
            top:230px;
            left: 1000px;
            padding:25px;
            height: 300px;
        }
        .login-container h2{
            text-align: center;  
              }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .login-container:hover {
            transform: scale(1.05);
        }
        h2 {
            margin-bottom: 1rem;
            color: #333;
        }
        .input-field {
            position: relative;
            margin-bottom: 1.5rem;
        }
        .input-field input {
            width: 100%;
            padding: 10px;
            border: none;
            border-bottom: 2px solid #ccc;
            outline: none;
            font-size: 1rem;
            transition: border-bottom 0.3s, background0.3s;
            background: transparent;
        }
        .input-field input:focus {
            border-bottom: 2px solid #2575fc;
            background: rgba(37, 117, 252, 0.1);
        }
        .toggle-password {
            position: absolute;
            right: 10px;
            top: 50%;
            transform: translateY(-50%);
            cursor: pointer;
            font-size: 1rem;
            color: #2575fc;
        }
        .login-btn1 {
            background: #2575fc;
            color: white;
            border: none;
            padding: 10px;
            width: 100%;
            cursor: pointer;
            font-size: 1rem;
            border-radius: 5px;
            transition: all 0.3s;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }
        .login-btn1:hover {
            transform: scale(1.1);
            background: #6a11cb;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
        }
        .login-btn1:active {
            animation: bounce 0.3s;
        }
        @keyframes bounce {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
        .message {
            margin-top: 10px;
            font-size: 0.9rem;
            color: red;
            display: none;
            opacity: 0;
            transition: opacity 0.5s ease-in-out;
        }
        .shake {
            animation: shake 0.5s ease-in-out;
        }
        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-5px); }
            50% { transform: translateX(5px); }
            75% { transform: translateX(-5px); }
        }

        nav{
            width: 100%;
            height: 75px;
            line-height: 75px;
            padding: 0px 100px;
            position:fixed;
            background-image: linear-gradient(#033747,#012733);
            position: relative;
        }
        nav .logo p{
            font-size: 30px;
            font-weight: bold;
            float: left;
            color: white;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            cursor: pointer;
        }
        nav ul{
            float: right;
        }
        nav li{
            display: inline-block;
            list-style: none;
        }
        nav li a{
            font-size: 18px;
            text-transform: uppercase;
            padding: 0px 30px;
            color: white;
            text-decoration: none;
        }
        nav li a:hover{
            color: #ff8c69;
            transform: all 0.4s ease 0s;

        }
        .items img{
            width: 100%;
            height: 100vh;
            background-size: cover;
            background-position: center;
            position:absolute;
            
        }
        .text h2{
            position: relative;
            color: antiquewhite;
            padding-top: 200px;
            font-size: 60px;
            padding-left: 60px;
            width: 60%;
        }
        .text p{
            position: relative;
            color: antiquewhite;
            padding-top: 20px;
            padding-left: 50px;
            font-size: 30px;
            width: 60%;
        }  
        .login-btn {
            background: #2575fc;
            color: white;
            border: none;
            padding: 10px;
            width: 10%;
            margin-left: 250px;
            cursor: pointer;
            font-size: 1rem;
            border-radius: 5px;
            transition: all 0.3s;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            position: relative;
            border-radius: 20px;
            margin-top: 40px;
        }
        .login-btn:hover {
            transform: scale(1.1);
            background: #6a11cb;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
        } 
        .text2 p{
            position: absolute;
            top: 825px;
            font-size: 20px;
            left: 15px;
        }
        .text2 h1{
            position: absolute;
            top: 845px;
            font-size: 60px;
            left: 15px;
        }
        .login-btn2 {
            background: none;
            color: rgb(31, 25, 25);
            border: none;
            padding: 10px;
            width: 180px;
            margin-left: 1320px;
            cursor: pointer;
            font-size: 1rem;
            border-radius: 2px;
            transition: all 0.3s;
            box-shadow: 0 4px 10px rgba(1, 2, 1, 3.2);
            position: relative;
            border-radius: 20px;
            margin-top: 270px;
        }
        .login-btn2:hover {
            transform: scale(1.1);
            background: #6a11cb;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
        }
        .items1 img{
            width:460px;
            margin-left: 30px;
            position: absolute;
            top: 964px;
            height: 310px;
            border-radius: 30px;
        }
        .items2 img{
            width:460px;
         top: 964px;
           margin-left: 530px;
           position: absolute;
           height: 310px;
           border-radius: 30px;
        }
        .items3 img{
            width:460px;
           top: 964px;
           margin-left: 1020px;
           position: absolute;
           height: 310px;
           border-radius: 30px;
        }
        .image-text h3{
            position: absolute;
            top: 1300px;
           left: 200px;
           font-size: 40px;
        }
        .image-text2 h3{
            position: absolute;
            top: 1300px;
           left: 600px;
           font-size: 40px;
        }
        .image-text3 h3{
            position: absolute;
            top: 1300px;
           left: 1160px;
           font-size: 40px;
        }
        .items1 img:hover {
            transform: scale(1.1);
            background: #6a11cb;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
            transition:ease-in-out 0.2s ;
        }
        .items2 img:hover {
            transform: scale(1.1);
            background: #6a11cb;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
            transition:ease-in-out 0.2s ;
            
        }
        .items3 img:hover {
            transform: scale(1.1);
            background: #6a11cb;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
            transition:ease-in-out 0.2s ;
        }
        .text-box4{
            top: 1800;
            background-color: transparent;
            height: 350px;
            width: 1450px;
            border: #060606;
            box-shadow: 0 6px 15px rgba(2, 2, 2, 1.3);
            border-radius: 40px;
        }
        #text-id{
            background-image: url(https://wallpapersok.com/images/high/cappadocia-s-hot-air-balloons-full-screen-desktop-zhxe7yla0nm34ft1.webp);
            position: absolute;
            top: 1400px;
            left: 40px;
         background-repeat: no-repeat ;
         background-size: cover;
        border-radius: 40px;
        }  
        .login-btnx {
            background: red;
            color: rgb(31, 25, 25);
            border: none;
            padding: 10px;
            width: 170px;
            margin-left: 950px;
            cursor: pointer;
            font-size: 1rem;
            border-radius: 2px;
            transition: all 0.3s;
            box-shadow: 0 4px 10px rgba(1, 2, 1, 3.2);
            position: absolute;
            border-radius: 20px;
            margin-top: -112px;
        }
        .login-btnx:hover {
            transform: scale(1.1);
            background: #6a11cb;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
        } 
        .text-box4 input{
            top: 235px;
            position: relative;
            margin-left: 420px;
            width: 500px;
            border-radius: 50px;
            background-color: white;
            height: 50px;
            animation:forwards;
            font-size: 20px;


        }
        .text-box4 input:hover {
            transform: scale(0.1.00.1);
            background: #6fdedf;
            box-shadow: 5pc 6px 15px rgba(1, 2, 2, 0.3);
            animation: ease-in-out3s;
        }
        .p p{
            position: absolute;
            top: 290px;
            left: 540px;
        }
       .a a{
            position: absolute;
            top: 290px;
            left: 910px;
        }
        .p2 h3{
            margin-top:-230px;
            position: absolute;
            left: 250px;
            font-size: 30px;
            font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
        }
        .mail h1{
            margin-top:-350px;
            position: absolute;
            left: 650px;
            font-size: 80px;
            font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
            background-color: transparent ;

}
#box-image{
    position: relative;
            top: 880px;
        border-radius: 50px;
        height: 500px;
        background-color: #f3f0f0;
        background-image: url(https://images.unsplash.com/photo-1530789253388-582c481c54b0?fm=jpg&q=60&w=3000&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MzR8fHRyYXZlbHxlbnwwfHwwfHx8MA%3D%3D);
     background-size: contain;
     background-repeat: no-repeat;
     width: 100%;
    }
.text-h{
position: relative;
    left:780px;
    top:390px;
    color: #6a11cb;
    font-size:30px;
    width: 40%;
}
.text-h h2{
position: relative;
    left:10px;
    top:10px;
    color: black;
    font-size:25px;
    width: 120%
}
.text-h p{
position: relative;
    left:10px;
    top:20px;
    color: black;
    font-size:15px;
    width: 120;
}

.text-h-btn {
            background: rgb(66, 170, 211);
            color: white;
            border: none;
            padding: 10px;
            width: 190px;
            margin-left: 800px;
            cursor: pointer;
            font-size: 1rem;
            border-radius: 2px;
            transition: all 0.3s;
            box-shadow: 0 4px 10px rgba(1, 2, 1, 3.2);
            position: absolute;
            border-radius: 20px;
            margin-top: 450px;
        }
        .text-h-btn:hover {
            transform: scale(1.1);
            background: #ed75e1;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
        }
        #box-body{
            position: relative;
            top: 680px;
        border-radius: 50px;
        height: 600px;
        background-color: #f3f0f0;
        width: 100%;
        }
        #tbody{
            position: relative;
            top: +110px;
            left:-700px;

        }
        .hbody ul{
            float: right;
        }
        .hbody li{
            list-style: none;
            padding-top: 8px;
            
        }
        .hbody li a{
            font-size: 18px;
            text-transform:lowercase;
            padding: 0px 110px ;
            color: rgb(48, 44, 44);
            text-decoration: none;
        }
        .hbody li a:hover{
            color: #ff8c69;
            transform: all 0.4s ease 0s;

        }
        .hbody ul h1{
            font-size: 15px;
            top: 100px;
            margin-left: 100px;
        }
        .Abody li{
            list-style: none;
            padding-top: 10px;
            position: relative;
            margin-left: 780px;
            top: 110PX;
            width: 400px;
        }
        .Abody li a{
            font-size: 15px;
            text-transform:lowercase;
            padding: 0px 110px ;
            color: rgb(48, 44, 44);
            text-decoration: none;
        }
        .Abody li a:hover{
            color: #ff8c69;
            transform: all 0.4s ease 0s;

        }
        .Abody ul h1{
            font-size: 15px;
            top: 112px;
            margin-left: 890px;
            position: relative;
        }
        .shop li{
            list-style: none;
            padding-top: 10px;
            position: relative;
            margin-left: 1080px;
            top: -450PX;
            width: 500px;
        }
        .shop li a{
            font-size: 15px;
            text-transform:lowercase;
            padding: 0px 110px ;
            color: rgb(48, 44, 44);
            text-decoration: none;
        }
        .shop li a:hover{
            color: #ff8c69;
            transform: all 0.4s ease 0s;

        }
        .shop ul h1{
            font-size: 17px;
            top: -450px;
            margin-left: 1190px;
            position: relative;
        }
        .about li{
            list-style: none;
            padding-top: 10px;
            position: relative;
            margin-left: 1080px;
            top: -450PX;
            width: 500px;
        }
        .about li a{
            font-size: 14px;
            text-transform:lowercase;
            padding: 0px 110px ;
            color: rgb(48, 44, 44);
            text-decoration: none;
        }
        .about li a:hover{
            color: #ff8c69;
            transform: all 0.4s ease 0s;

        }
        .about ul h1{
            font-size: 15px;
            top: -450px;
            margin-left: 1190px;
            position: relative;
        }
        .web h1{
            font-size: 30px;
            bottom: 870px;
            left: 50px;
            position: relative;
            color: #6a11cb;

        }
        .webp{
            font-size: 15px;
            bottom: 860px;
            left: 50px;
            position: relative;

        }
        .follo{
            font-size: 25px;
            bottom: 820px;
            left: 50px;
            position: relative;
            color: #6a11cb;
        }
        .link{
            font-size: 30px;
            bottom: 805px;
            left: 50px;
            position: relative;
            letter-spacing: 11px;
            color: pink;


        }
        .link a i:hover{
            color: #ff8c69;
            transform: all 0.4s ease 0s;
        }
        .side-sharch input{
        bottom: 705px;
            position: relative;
            margin-left: 40px;
            width: 300px;
            border-radius: 50px;
            background-color: white;
            height: 30px;
            animation:forwards;
            font-size: 20px;


        }
        .side-sharch input:hover {
            transform: scale(0.1.00.1);
            background: #fdffff;
            box-shadow: 5pc 6px 15px rgba(1, 2, 2, 0.0);
            animation: ease-in-out3s;
            border-color: #2575fc;
        }
        .sub{
            bottom: 850px;
            color: #033747;
            position: relative;
            left: 50px;
        }
        .gift{
            bottom: 840px;
            color: #033747;
            position: relative;
            left: 45px;
            font-size: 35px;
        }
        .side-btnx {
            background: red;
            color: rgb(31, 25, 25);
            border: none;
            padding: 10px;
            width: 300px;
            margin-left: 40px;
            cursor: pointer;
            font-size: 1rem;
            border-radius: 2px;
            transition: all 0.3s;
            box-shadow: 0 4px 10px rgba(1, 2, 1, 3.2);
            position: relative;
            border-radius: 20px;
            bottom:680px ;
        }
        .side-btnx:hover {
            transform: scale(1.1);
            background: #6a11cb;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
        }
          .FT{
            background-color: #7f7a7a;
            top: -560px;
             width: 100%;
             position: relative;
        }

    </style>
    </head> 
    <body>
<nav>
<div class="logo">
    <p>
        EXPLORE
    </p>
</div>
<ul>
<li><a href="#">Destination</a></li>
<li><a href="#">Planning</a></li>
<li><a href="#">Inspiration</a></li>
<li><a href="#">Shop</a></li>
</ul>
</nav>
<div class="items">
    <img src="https://img.freepik.com/free-photo/misurina-sunset_181624-34793.jpg?t=st=1742966107~exp=1742969707~hmac=c58c517831056c6b922bf704bdfbf397a82c5eae6e4f9de4891f34bfd0686692&w=1380" alt="">
</div>
<div class="text">
<h2>Travel the whole world</h2>
<p>"Explore vibrant cultures, breathtaking landscapes, <br>and mesmerizing wonders. Collect unforgettable memories,<br> try new experiences, and discover the beauty of our<br> incredible planet, one adventure at a time."</p>
</div>
<div class="login-container" id="login-container">
    <h2>Login</h2>
    <div class="input-field">
        <input type="text" placeholder="Username" id="username">
    </div>
    <div class="input-field">
        <input type="password" placeholder="Password" id="password">
        <span class="toggle-password" onclick="togglePassword()">👁️</span>
    </div>
    <button class="login-btn1" onclick="login()">Login</button>
    <p class="message" id="error-message">Invalid credentials, please try again.</p>
</div>
<div>
<button class="login-btn" onclick="Shop()">Shop</button>
</div>
<div class="text2">
    <p>Plan your trip</p>
    <h1>Where to next?</h1>
</div>
<div>
    <button class="login-btn2" onclick="ViewallDestination()">View all Destination</button>
    </div>
    <div class="items1">
     <a href="#"> <img src="https://as2.ftcdn.net/v2/jpg/01/03/17/23/1000_F_103172390_8zOuwoHGzKfZRu2X4z10cyl9rrbdIq6H.jpg" alt=""></img></a>
    </div>
    <div class="items2">
        <a href="#"> <img src="https://navbharattimes.indiatimes.com/thumb/114889987/114889987.jpg?imgsize=98702&width=700&height=394&resizemode=75" alt=""></a>
    </div>
    <div class="items3">
        <a href="#"><img src="https://as2.ftcdn.net/v2/jpg/11/87/82/49/1000_F_1187824932_XuzdIfo4pT38tn10g2Tlpgm1y6SZyiyy.jpg" alt=""></a>
    </div>  
    <div class="image-text">
        <h3>Kashmir</h3>
    </div>
    <div class="image-text2">
        <h3>KEDARNATH Mandir</h3>
    </div>
    <div class="image-text3">
        <h3>Surya Mandir</h3>
    </div>
    <div id="text-id">
    <div class="text-box4">
    <input type="search"placeholder="Email address">
    </div>
    <div>
        <button class="login-btnx" onclick="Shop()">Subscrib Now</button>
        </div>
        <div class="p">
            <p>Subscribe to our newsletters and promotions. Read our</p>
        </div>
        <div class="a">
        <a href="#">privet policy</a>
        </div>
        <div class="p2">
            <H3>
                **Travel becomes more beautiful when new stories unfold on the way. <br> 
The destination is just an excuse; the real joy lies in the journey.** ✈️🌍
            </H3>
        </div>
        <div class="mail">
            <h1>
                📩
            </h1>
        </div>
    </div>

<div id="box-image">

</div>
<div class="text-h">
    <h1>Your dream itinerary, 
        <br>crafted with you</h1>
       <h2>Ewhere by EXPLORE you with an award-winning<br> local expert to craft your personalized, unforgettable trip.</h2>
   <p> Make a trip request, connect with a local expert, and sit back while our experts craft a custom <br>itinerary based on expertise, exclusivity, and ease. It’s a trip you couldn’t plan yourself, all with 24/7 <br>on-the-ground support.</p>
</div>
<div>
    <button class="text-h-btn"onclick="ViewallDestination()">Explore Elsewhere 🔜</button>
    </div>
    <div id="box-body">

    </div>
    
    <div id="tbody">
        <div class="hbody">
            <ul>
                <H1>TOP DESTINMATION</H1>
                <li><a href="#">PURI</a></li>
                <li><a href="#">Kashmir</a></li>
                <li><a href="#">UJJAIN</a></li>
                <li><a href="#">LADAK</a></li>
                <li><a href="#">MATHURA</a></li>
                <li><a href="#">MANALI</a></li>
                <li><a href="#">RISHIKESH</a></li>
                <li><a href="#">SURYA MANDIR</a></li>
                <li><a href="#">KEDARNATH</a></li>
                <li><a href="#">MEGHALE</a></li>
                <li><a href="#">DHARJALING</a></li>
                <li><a href="#">PANCHMADI</a></li>
                <li><a href="#">DWARIKA</a></li>
                <li><a href="#">SOMNATH</a></li>
                <li><a href="#">MANIKAARNIKA GHAT</a></li>
                <li><a href="#">SANGAM</a></li>
                <li><a href="#">JAIPUR</a></li>
                <li><a href="#">GOA</a></li>
                <li><a href="#">SHIMLA</a></li>
                </ul>
                
        </div>
    </div>
    <div class="Abody">
        <ul>
            <H1>TRAVEL INTERESTS</H1>
            <li><a href="#">adventure travel</a></li>
            <li><a href="#">Art and cultures</a></li>
            <li><a href="#">Beaches, coasts and islands</a></li>
            <li><a href="#">Family Holidays</a></li>
            <li><a href="#">Festivals</a></li>
            <li><a href="#">Food and deink</a></li>
            <li><a href="#">Honeymoon and Romance</a></li>
            <li><a href="#">Road Trip</a></li>
            <li><a href="#">Sustainable Travel</a></li>
            <li><a href="#">Travel on a budget</a></li>
            <li><a href="#">Wildlife and Nature</a></li>
            </ul>
    </div>
    <div class="shop">
        <ul>
        <H1>SHOP</H1>
        <li><a href="#">Destination Guides</a></li>
        <li><a href="#">Lonely Planet Kide</a></li>
        <li><a href="#">Lonely Planet Shop</a></li>
        <li><a href="#">Non-English Guides</a></li>
</ul>
    </div>
    <div class="about">
        <ul>
            <H1>About As</H1>
            <li><a href="#">About Lonely Planet</a></li>
            <li><a href="#">Contact Us</a></li>
            <li><a href="#">Trade and Advertising</a></li>
            <li><a href="#">privecy Policy</a></li>
            <li><a href="#">Terms and Conditions</a></li>
            <li><a href="#">Work For us</a></li>
            <li><a href="#">Write For us</a></li>
            <li><a href="#">Consumer Health Data Privacy Policy</a></li>
            <li><a href="#">Cookie Settings</a></li>
            <li><a href="#">Do Not or Share My Personal Information</a></li>
        </ul>
    </div>
    <div id="maill">
        <div class="web">
            <h1>
                EXPLORE
            </h1>
        </div>
        <div class="webp">
            For Explorers Everywhere
        </div>
        <div class="follo">
            Follow us
        </div>
        <div class="link">
            <a href="#"><i class="fa-brands fa-square-instagram" style="color: #ff00f7;"></i></a>
            <a href="#"><i class="fa-brands fa-facebook"></i></a>
            <a href="#"><i class="fa-brands fa-twitter" style="color: #121212;"></i></a>
            <a href="#"><i class="fa-brands fa-youtube" style="color: #ed0202;"></i></a>
        </div>
    </div>
    <div class="side-sharch">
        <input type="search"placeholder="Email address">
        </div>
        <div>
            <button class="side-btnx" onclick="Shop()">Subscrib Now</button>
            </div>
            <div class="sub">
                <p>SUBSCRIBE</p>
            </div>
            <div class="gift">
                <p>
                    Get 20% off your first order
                </p>
            </div>
            <div class="FT">
                <footer>
                    © 2025 EXPLORE, a Red Ventures company. All rights reserved. No part of this site may be reproduced without our written permission. 
                </footer>
            </div>
<script>
    function login() {
        const username = document.getElementById('username').value;
        const password = document.getElementById('password').value;
        const errorMessage = document.getElementById('error-message');
        const loginContainer = document.getElementById('login-container');
        
        if(username === "user" && password === "password") {
            alert("Login successful!");
        } else {
            errorMessage.style.display = 'block';
            errorMessage.style.opacity = '1';
            loginContainer.classList.add('shake');
            setTimeout(() => loginContainer.classList.remove('shake'), 500);
            setTimeout(() => {
                errorMessage.style.opacity = '0';
                setTimeout(() => errorMessage.style.display = 'none', 500);
            }, 3000);
        }
    }

    function togglePassword() {
        const passwordField = document.getElementById('password');
        passwordField.type = passwordField.type === "password" ? "text" : "password";
    }
</script>
    </body>
    </html>
