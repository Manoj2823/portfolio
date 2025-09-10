<!DOCTYPE html>

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Potfolio</title>
    <link rel="stylesheet" href="style.css">
    <script src="https://kit.fontawesome.com/67e5987627.js" crossorigin="anonymous"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/7.0.0/css/all.min.css"
        integrity="sha512-DxV+EoADOkOygM4IR9yXP8Sb2qwgidEmeqAEmDKIOfPRQZOWbXCzLC6vjbZyy0vPisbH2SyW27+ddLVCN+OMzQ=="
        crossorigin="anonymous" referrerpolicy="no-referrer" />
    <style>
        * {
    margin: 0;
    padding: 0;
    font-family: 'Poppins', sans-serif;
    box-sizing: border-box;
}

body {
    background-color: #000000;
    color: white;
}
html{
    scroll-behavior: smooth;
}

#header {
    width: 100%;
    height: 100vh;
    background-image: url('image/background.png');
    background-size: cover;
    background-position: center;
}

.container {
    padding: 10px 10%;
}

nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
}

.logo {
    width: 200px;


}

nav ul li {
    display: inline-block;
    list-style: none;
    margin: 10px 20px;
}

nav ul li a {
    color: #FFF;
    text-decoration: none;
    font-size: 18px;
    position: relative;
}

nav ul li a::after {
    content: '';
    width: 0;
    height: 3px;
    background-color: #ff004f;
    position: absolute;
    left: 0;
    bottom: -6px;
    transition: 0.5s;
}

nav ul li a:hover::after {
    width: 100%;
}

.header-text {
    margin-top: 20%;
    font-size: 30px;
}

.header-text h1 {
    font-size: 60px;
    margin-top: 20px;
}

.header-text h1 span {
    color: #ff004f;
}

/* ------------about-------------------- */
#about {
    padding: 80px 0;
    color: #ababab;
}

.row {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}

.about-col-1 {
    flex-basis: 35%;
}

.about-col-1 img {
    width: 90%;
    border-radius: 35px;
}

.about-col-2 {
    flex-basis: 60%;
}

.sub-title {
    font-size: 60px;
    font-weight: 600;
    color: white;
}

.tab-titles {
    display: flex;
    margin: 20px 0 40px;
}

.tab-links {
    margin-right: 50px;
    font-size: 18px;
    font-weight: 500;
    cursor: pointer;
    position: relative;
}

.tab-links::after {
    content: '';
    width: 0;
    height: 3px;
    background-color: #ff004f;
    position: absolute;
    left: 0;
    bottom: -8px;
    transition: 0.5s;
}

.tab-links.active-links::after {
    width: 50%;
}

.tab-contents ul li {
    list-style: none;
    margin: 10px 0;
}

.tab-contents ul li span {
    color: #b54769;
    font-size: 14px;
}

.tab-contents {
    display: none;
}

.tab-contents.active-tab {
    display: block;
}

/* --------------services----------- */
#services {
    padding: 30px 0;
}

.services-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    grid-gap: 40px;
    margin-top: 50px;
}

.services-list div {
    background-color: #262626;
    padding: 40px;
    font-size: 13px;
    font-weight: 300;
    border-radius: 10px;
    transition: 0.5s, transform 0.5s;
}

.services-list div i {
    font-size: 50px;
    margin-bottom: 30px;
}

.services-list div h2 {
    font-size: 30px;
    font-weight: 500;
    margin-bottom: 15px;
}

.services-list div a {
    text-decoration: none;
    color: white;
    font-size: 12px;
    margin-top: 20px;
    display: inline-block;
}

.services-list div:hover {
    background: #ff004f;
    transform: translateY(-10px);
}

/* ---------------portfolio-------------- */
#portfolio {
    padding: 50px 0;
}

.work-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    grid-gap: 40px;
    margin-top: 50px;
}

.work {
    border-radius: 10px;
    position: relative;
    overflow: hidden;
}

.work img {
    width: 100%;
    border-radius: 10px;
    display: block;
    transition: transform 0.5s;
}

.layer {
    width: 100%;
    height: 0;
    background: linear-gradient(rgba(0, 0, 0, 0.6), #ff004f);
    border-radius: 10px;
    position: absolute;
    left: 0;
    bottom: 0;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    padding: 0 40px;
    text-align: center;
    font-size: 14px;
    transition: height 0.5s;
}

.layer h3 {
    font-weight: 500;
    margin-bottom: 20px;
}

.layer a {
    margin-top: 20px;
    color: #ff004f;
    text-decoration: none;
    font-size: 18px;
    line-height: 60px;
    background: #fff;
    height: 60px;
    width: 60px;
    border-radius: 50%;
    text-align: center;
}

.work:hover img {
    transform: scale(1.1);
}

.work:hover .layer {
    height: 100%;
}

.btn {
    display: block;
    margin: 50px auto;
    width: fit-content;
    border: 1px solid #ff004f;
    padding: 14px 50px;
    border-radius: 6px;
    text-decoration: none;
    color: #fff;
    transition: background 0.5s;
}

.btn:hover {
    background: #ff004f;
}

/* ---------------contact------------- */
.contact-left {
    flex-basis: 35%;
}

.contact-right {
    flex-basis: 60%;
}

.contact-left p {
    margin-top: 30px;
}

.contact-left p i {
    color: #ff004f;
    margin-right: 15px;
    font-size: 25px;
}

.social-icons {
    margin-top: 30px;
}

.social-icons a {
    text-decoration: none;
    font-size: 30px;
    margin-right: 15px;
    color: #ababab;
    display: inline-block;
    transition: transform 0.5s;
}

.social-icons a:hover {
    color: #ff004f;
    transform: translateY(-5px);
}

.btn.btn2 {
    display: inline-block;
    background: #ff004f;
}

.contact-right form {
    width: 100%;
}

form input,
form textarea {
    width: 100%;
    border: 0;
    outline: none;
    background: #262626;
    padding: 15px;
    margin: 15px 0;
    color: #fff;
    font-size: 18px;
    border-radius: 6px;
}

form .btn2 {
    padding: 14px 60px;
    font-size: 18px;
    margin-top: 20px;
    cursor: pointer;
}

.copyright {
    width: 100%;
    text-align: center;
    padding: 25px 0;
    background: #262626;
    font-weight: 300;
    margin-top: 20px;
}

.copyright i {
    color: #ff004f;
}

/* ------------------- css for ss------------ */
nav .fa-solid {
    display: none;
}

@media only screen and (max-width: 600px) {
    #header {
        background-image: url(image/phn\ img.png);
    }

    .header-text {
        margin-top: 100%;
        font-size: 16px;
    }

    .header-text h1 {
        font-size: 30px;
    }

    nav .fa-solid {
        display: block;
        font-size: 25px;
    }
    nav ul{
        background: #ff004f;
        top: 0;
        position: fixed;
        right: -200px;
        width: 200px;
        height: 100vh;
        padding-top: 50px;
        z-index: 2;
        transition: right 0.5s;
    }
    nav ul li{
        display: block;
        margin: 25px;
    }
    nav ul .fa-solid{
        position: absolute;
        top: 25px;
        left: 25px;
        cursor: pointer;
    }
    .sub-title{
        font-size: 40px;
    }
    .about-col-1, .about-col-2{
        flex-basis: 100%;
    }
    .about-col-1{
        margin-bottom: 30px;
        padding-left: 28px;
    }
    .about-col-2{
        font-size: 14px;
    }
    .tab-links{
        font-size: 16px;
        margin-right: 20px;
    }
    .contact-left, .contact-right{
        flex-basis: 100%;
    }
    .copyright{
        font-size: 14px;
    }
}
#msg{
    color: #61b752;
    margin-top: -40px;
    display: block;
}
    </style>
</head>

<body>
    <div id="header">
        <div class="container">
            <nav>
                <img src="image/MANOJ logo.jpeg" class="logo">
                <ul id="sidemenu">
                    <li><a href="#header">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#portfolio">Protfolio</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <i class="fa-solid fa-xmark" onclick="closemenu()"></i>
                </ul>
                <i class="fa-solid fa-bars" onclick="openmenu()"></i>
            </nav>
            <div class="header-text">
                <p>FRONTEND DEVELOPER</p>
                <h1>Hi, I'm <span>Manoj Ramesh </span>,<br>From Madurai, Tamil Nadu</h1>
            </div>
        </div>
    </div>
    <!---- ------------------about-------- -->
    <div id="about">
        <div class="container">
            <div class="row">
                <div class="about-col-1">
                    <img src="image/m1.png">
                </div>
                <div class="about-col-2">
                    <h1 class="sub-title">About Me</h1>
                    <p>Hello! I'm [Manoj.R], a passionate and dedicated developer with a keen interest in building
                        impactful digital solutions. I specialize in Python, Web Development, and UI/UX Design, with
                        hands-on experience in tools like Tkinter, MySQL, Pygame, and modern front-end technologies.

                        I enjoy turning complex problems into simple, beautiful, and intuitive designs. Whether it’s
                        developing a robust Hospital Management System, designing an engaging Food delivery app, or
                        crafting responsive websites, I aim to deliver quality and innovation in every project.

                        I’m a quick learner, a strong team player, and always eager to explore new technologies and
                        ideas. My goal is to keep growing as a developer while contributing to meaningful projects that
                        make a difference.
                    </p>

                    <div class="tab-titles">
                        <p class="tab-links active-links" onclick="opentab('Skills')">Skills</p>
                        <p class="tab-links" onclick="opentab('experience')">Experience</p>
                        <p class="tab-links" onclick="opentab('education')">Education</p>
                    </div>
                    <div class="tab-contents active-tab" id="Skills">
                        <ul>
                            <li><span>WEB DEVELOPMENT(HTML,CSS)</span><br>Responsive, interactive design</li>
                            <li><span>UI/UX</span><br>Designing Web/App Interfaces</li>
                            <li><span>PYTHON</span><br>Versatile, backend logic</li>
                            <li><span>MY SQL</span><br>Efficient data management</li>
                        </ul>
                    </div>
                    <div class="tab-contents" id="experience">
                        <ul>
                            <li><span>08/07/2024 - 10/08/2024</span><br>Internship for Mobile Application Development at
                                Wizinoa</li>
                            <li><span>18/01/2024 - 03/02/2024</span><br>Internship for Technology job simulation at
                                deloitte</li>
                            <li><span>22/06/2023 - 05/07/2023</span><br>Internship for Web development at WebGapp</li>
                        </ul>
                    </div>
                    <div class="tab-contents" id="education">
                        <ul>
                            <li><span>2021 - 2025</span><br> BE/CSE from Fatima Michael College Of Engineering and
                                Technology</li>
                            <li><span>2020 - 2021</span><br>12 th Grade from Subramaniya Bharathi Mt.Hr.Sec.School</li>
                            <li><span>2018 - 2019</span><br>10 th Grade from Sri Sundareshwara Vidya Sala
                                Mt.Hr.Sec.School</li>
                            <li><span>Sep/2020 - Feb/2021</span><br>Diploma in Computer Application from Vels Institute
                                Of Technology</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- -----------------services------------------------ -->
    <div id="services">
        <div class="container">
            <h1 class="sub-title">My Services</h1>
            <div class="services-list">
                <div>
                    <i class="fa-solid fa-code"></i>
                    <h2>Web Development</h2>
                    <p>Crafting responsive and modern websites using HTML, CSS, JavaScript, and frameworks like React
                        and Django. Ensuring clean UI, fast performance, and mobile-friendly designs.</p>
                    <a href="#">Learn More</a>
                </div>
                <div>
                    <i class="fa-brands fa-python"></i>
                    <h2>Python Development</h2>
                    <p>Design and develop dynamic, secure, and scalable web applications using Python frameworks like
                        Django and Flask. Ideal for custom dashboards, content management systems, APIs, and more.</p>
                    <a href="#">Learn More</a>
                </div>
                <div>
                    <i class="fa-brands fa-app-store"></i>
                    <h2>App Design</h2>
                    <p>Design modern and user-friendly mobile and web applications using Figma. From wireframes to
                        high-fidelity prototypes, focusing on clean UI and smooth user experience.</p>
                    <a href="#">Learn More</a>
                </div>
                <div>
                    <i class="fa-solid fa-crop-simple"></i>
                    <h2>UI/UX</h2>
                    <p>Turning ideas into beautiful, easy-to-use app and website designs! I use Figma to create smooth,
                        fun, and user-friendly experiences—from simple sketches to clickable prototypes that feel real.
                    </p>
                    <a href="#">Learn More</a>
                </div>
            </div>
        </div>
    </div>
    <!-- ------------portfolio------------------- -->
    <div id="portfolio">
        <div class="container">
            <h1 class="sub-title">My Work</h1>
            <div class="work-list">
                <div class="work">
                    <img src="image/pycharm1.png">
                    <div class="layer">
                        <h3>Hospital Management System</h3>
                        <p>Developed a full-featured desktop application using Python, Tkinter, and MySQL.

                            Modules include patient registration, doctor management, and

                            Focused on secure login, data handling, and real-time database integration.</p>
                        <a href="#"><i class="fa-solid fa-arrow-up-right-from-square"></i></a>
                    </div>
                </div>
                <div class="work">
                    <img src="image/work2.png">
                    <div class="layer">
                        <h3>Food Delivery App</h3>
                        <p>Designed a modern and intuitive food delivery app interface.

                            Prioritized mobile-first design principles with clean, user-friendly layouts.

                            Tools used: Figma / Adobe XD for prototyping and user flow mapping.</p>
                        <a href="#"><i class="fa-solid fa-arrow-up-right-from-square"></i></a>
                    </div>
                </div>
                <div class="work">
                    <img src="image/work3.jpeg">
                    <div class="layer">
                        <h3>Virtual Mouse Using Hand Gestures</h3>
                        <p>Created a virtual mouse system using Python, OpenCV, and Mediapipe.

                            Enabled touchless control of the computer using hand gestures via webcam.

                            Aimed at enhancing accessibility and hands-free interaction.</p>
                        <a href="#"><i class="fa-solid fa-arrow-up-right-from-square"></i></a>
                    </div>
                </div>
            </div>
            <a href="" class="btn">See more</a>
        </div>
    </div>
    <!-- --------------------conctact-------------------- -->
    <div id="contact">
        <div class="container">
            <div class="row">
                <div class="contact-left">
                    <h1>Contact Me</h1>
                    <p><i class="fa-solid fa-paper-plane"></i>manojramesh2808@gmail.com</p>
                    <p><i class="fa-solid fa-square-phone"></i>6374320021</p>
                    <div class="social-icons">
                        <a href="https://www.facebook.com/mersal.manoj.58726"><i class="fa-brands fa-facebook"></i></a>
                        <a href="https://www.instagram.com/__m_a__n__n__u__/?hl=en"><i
                                class="fa-brands fa-instagram"></i></a>
                        <a href="https://www.linkedin.com/in/manoj-r-1b7115282/"><i
                                class="fa-brands fa-linkedin"></i></a>
                    </div>
                    <a href="image/Manoj CV-1.pdf" download class="btn btn2">Download CV</a>
                </div>
                <div class="contact-right">
                    <form name="submit-to-google-sheet">
                        <input type="text" name="Name" placeholder="Your Name" required>
                        <input type="email" name="Email" placeholder="Your Email" required>
                        <textarea name="Messages" rows="6" placeholder="Your Messages"></textarea>
                        <button type="submit" class="btn btn2">Submit</button>
                    </form>
                    <span id="msg"></span>
                </div>
            </div>
        </div>
        <div class="copyright">
            <p>Copyright &copy; Manoj <i class="fa-solid fa-heart"></i></p>
        </div>
    </div>





    <script>
        var tablinks = document.getElementsByClassName("tab-links")
        var tabcontents = document.getElementsByClassName("tab-contents")
        function opentab(tabname) {
            for (tablink of tablinks) {
                tablink.classList.remove("active-links");
            }
            for (tabcontent of tabcontents) {
                tabcontent.classList.remove("active-tab");
            }
            event.currentTarget.classList.add("active-links")
            document.getElementById(tabname).classList.add("active-tab");
        }
    </script>

    <script>

        var sidemenu = document.getElementById("sidemenu")
        function openmenu() {
            sidemenu.style.right = "0";
        }
        function closemenu() {
            sidemenu.style.right = "-200px";
        }


    </script>
    <script>
        const scriptURL = 'https://script.google.com/macros/s/AKfycbyIzKeeA2k-PUdQauf21Tt2BMF3G5vNDYzngqXLekPf8g7Jn6z7p2qBaFXwLlEWBIsa/exec'
        const form = document.forms['submit-to-google-sheet']
        const msg = document.getElementById("msg")

        form.addEventListener('submit', e => {
            e.preventDefault()
            fetch(scriptURL, { method: 'POST', body: new FormData(form) })
                .then(response => {
                    msg.innerHTML = "Message sent successfully"
                    setTimeout(function(){
                        msg.innerHTML = ""
                    },5000)
                    form.reset()
                })
                .catch(error => console.error('Error!', error.message))
        })
    </script>
</body>

</html>
