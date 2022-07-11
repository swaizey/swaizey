<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="all.min.css">
    <script src="all.min.js"></script>
    <title>Video Background</title>
</head>
<body>
    <section class="showcase ">
        <header>
            <h2 class="logo">Travel</h2>
            <div class="toggle "></div>
        </header>
      <video src="Mountains.mp4" autoplay loop muted>
        </video> 
        <div class="overlay"></div>
        <div class="text">
            <h2>Never Stop</h2>
            <h3>Explore The World</h3>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia recusandae neque cumque laboriosam harum accusamus nisi animi soluta. Molestiae, aliquid.</p>
            <a href="#">Explore</a>
        </div>
        <ul class="social">
            <li><a><i class="fa fa-brands fa-facebook fa-2x"></i></a></li>
            <li><a><i class="fa fa-brands fa-twitter fa-2x"></i></a></li>
            <li><a><i class="fa fa-brands fa-instagram fa-2x"></i></a></li>
            <li><a><i class="fa fa-brands fa-telegram fa-2x"></a></i></li>
        </ul>
    </section>
    <div class="menu">
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Contact</a></li>
            <li><a href="#">Services</a></li>
        </ul>
    </div>
<script>

    const menuToggle = document.querySelector(".toggle");
    const showcase = document.querySelector(".showcase");

    menuToggle.addEventListener('click', ()=>{
        menuToggle.classList.toggle('active')
        showcase.classList.toggle('active')
    })
</script>

</body>
</html>


CSS Styles


:root{
    --overlay-color:#03a9f4;
}

*{
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;

}
.showcase{
    position: absolute;
    right:0;
    width: 100%;
    min-height: 100vh;
    padding: 100px;
    display: flex;
    justify-content: space-between;
    align-items: center;
   background: #111;
   color: #fff;
    z-index: 2;
    transition: 0.5s;
}

.showcase.active{
    right: 300px;
}
.showcase header{
position: absolute;
top: 0;
left: 0;
width: 100%;
padding: 40px 100px;
z-index: 100;
display: flex;
align-items: center;
justify-content: space-between;
}
.logo{
    text-transform: uppercase;
    cursor: pointer;
}
.toggle.active {
    background: url('close.jpg');
    background-repeat: no-repeat;
    background-position: center;
    background-size: 30px;
    color: #111;
}
.toggle{
    position: relative;
    cursor: pointer;
    background: url("menu.jpg");
    width: 60px;
    height: 60px;
    background-repeat: no-repeat;
    background-position: center;
    background-size: 30px;

}
.showcase video{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    opacity: 0.8;
}
.text{
    position: relative;
    z-index: 10;
}
.overlay{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: #03a9f4;
    mix-blend-mode: overlay;
}

.text h2{
    font-size: 5em;
    font-weight: 800;
    line-height: 1.6em;
    text-transform: uppercase;
}

.text h3{
    font-size: 4em;
    font-weight: 600;
    line-height: 1.4rem;
    text-transform: uppercase;
}
.text p{
    font-size: 1.1em;
    margin: 20px 0;
    max-width: 700px;
    font-weight: 400;
}
.text a{
    display: inline-block;
    font-size: 1em;
    background:white ;
    padding: 10px 30px;
    text-decoration: none;
    color: black;
    text-transform: uppercase;
    margin-top: 10px;
    letter-spacing: 2px;
    transition: 0.4s;
}
.text a:hover{
    letter-spacing: 6px;
}
.social{
    position: absolute;
    bottom: 20px;
    z-index: 10;
    display: flex;
    justify-content: center ;
    align-items: center;
}
.social li{
    list-style: none;
}
.social li a{
    display: inline-block;
    margin-right: 20px;
    transform: scale(0.5);
    transition: 0.5s;
}
.social li a:hover{
    transform: scale(0.5) translateY(-15px);
}
@media(max-width:798px){
    .showcase,
    .showcase header{
        padding: 40px;
    }
    .text h2{
        font-size: 3em;
    }
    .text h3{
        font-size: 2em;
    }
}

.menu{
    position: absolute;
    top:0;
    right: 0;
    width: 300px;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}
.menu ul{
    position: relative;
    list-style: none;
}
.menu ul li a{
    text-decoration: none;
    font-size: 24px;
    color: black;
}
.menu ul li a:hover{
    color:var(--overlay-color)
}
