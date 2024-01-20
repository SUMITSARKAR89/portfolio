
<----HTML------>
!---for menu bar---!
<---- sticky--->
<body>
<header class="sticky">
        <div >
            <a href="#" class="logo">Cod<span>e</span>r.</a>
        </div>
        <ul class="nav">
            <li><a href="#home" class="active">Home</a></li>
            <li><a href="#about">about </a></li>
            <li><a href="#service">services</a></li>
            <li><a href="#portfolio">portfolio</a></li>
            <li><a href="#contact">contact us</a></li>    
        </ul>
  <---- menu---->
        <div class="bx bx-menu" id="menu-icon">      
        </div>
  </header>
 </body>

 <--------CSS---------->
 <style>
   header.sticky{
    background: linear-gradient(to bottom, rgb(0, 0, 0), #38160249);
    padding: 13px 10%;
    backdrop-filter: blur(5px);    
}
   header{
    padding: 18px 10%;
    background-color: transparent;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: fixed;
    width: 100%;
    top: 0;
    right: 0;
    z-index: 1000;
    transition: all 0.4s ease;    
}
   #menu-icon{
    font-size: 25px;
    color: var(--main-text-color);
    border: none;
    display: none;
    cursor: pointer;
    margin-left: 35px;
    z-index: 10001;

}
   @media (max-width: 735px){
     .nav a{
        display: block;
        font-size: 15px;
        font-weight: 700;
        padding: 5px 0;
    }
    header.sticky{ 
        backdrop-filter: none;  
    }
    .nav{
        position: absolute;
        top: -500px;
        right: 0;
        left: 0;
        display:inline-block;
        text-align: left;
        background-color:black;
        opacity: 1;
        height: 30vh;
        transition: 0.5s ease-in;    
    }
    /* this is for Java  */
    .nav.open{
        top: 100%;   
    }
    #menu-icon{
        display: block;
        margin-left: -30px;
        font-size: 30px;
        transition: 0.5s;
    }
   }
 </style>

 <--------------js-------------->
 <script>
   const header = document.querySelector("header");
header.addEventListener("scroll", function(){
    header.classList.toggle("sticky", window.scrollY > 100)
});

const menu = document.querySelector("#menu-icon");
const nav = document.querySelector(".nav");

menu.onclick = () => {
    menu.classList.toggle('bx-x');
    nav.classList.toggle('open');
}
window.onscroll = () => {
    menu.classList.remove('bx-x');
    nav.classList.remove('open');
}
   
 </script>
