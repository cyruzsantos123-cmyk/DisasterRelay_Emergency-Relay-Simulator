<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Pixel Presentation</title>

    <!-- Pixel Font -->
    <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">

    <style>

        .small-text h1 {
       font-size: 32px;
}

.small-text p {
    font-size: 15px;
    line-height: 1.5;
}

    .small-text li {
    font-size: 15px;
    line-height: 1.5;
}

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: #111;
            color: white;
            overflow: hidden;
            font-family: 'Press Start 2P', cursive;
        }

        /* =========================
           NAVBAR
        ========================= */
        /* =========================
   SOFT BACKGROUND OVERLAY
========================= */

.content {

    width: 90%;
    max-width: 1000px;

    margin: 0 !important;
    padding: 0 !important;

    text-align: center;

    background: transparent !important;
    border: none !important;
    box-shadow: none !important;
    outline: none !important;
    backdrop-filter: none !important;

    z-index: 10;
}

h1 {
    font-size: clamp(35px, 6vw, 75px);

    line-height: 1.4;

    margin-bottom: 25px;

    color: white;

    text-shadow:
        3px 3px 0px #000;
}


h2 {
    font-size: clamp(25px, 4vw, 50px);

    line-height: 1.5;

    margin-bottom: 30px;

    color: white;

    text-shadow:
        3px 3px 0px #000;
}


p {
    font-size: clamp(14px, 2vw, 22px);

    line-height: 2;

    color: white;

    text-shadow:
        2px 2px 0px #000;
}


ul {
    text-align: left;

    font-size: clamp(13px, 2vw, 20px);

    line-height: 2.2;

    padding-left: 40px;

    color: white;

    text-shadow:
        2px 2px 0px #000;
}

        .navbar {
            position: fixed;
            top: 0;
            left: 0;

            width: 100%;
            height: 75px;

            display: flex;
            align-items: center;
            justify-content: space-between;

            padding: 0 35px;

            z-index: 100;
        }


        /* LOGO */

        .logo {
            font-size: 18px;
            color: white;

            text-shadow:
                3px 3px 0px #000;
        }


        /* NAV LINKS */

        .nav-links {
            display: flex;
            gap: 10px;
            list-style: none;
        }


        .nav-links button {

            font-family: 'Press Start 2P', cursive;

            font-size: 9px;

            padding: 12px 15px;

            border: 2px solid transparent;

            background: transparent;

            color: white;

            cursor: pointer;

            transition: 0.2s;
        }


        .nav-links button:hover {

            border: 2px solid white;

            background: rgba(255,255,255,0.1);

            transform: translateY(-2px);
        }


        .nav-links button.active {

            background: white;

            color: black;

            border: 2px solid white;
        }


        /* =========================
           SLIDES
        ========================= */

        .presentation {

            width: 100vw;
            height: 100vh;

            position: relative;
        }


.slide {
    position: absolute;
    width: 100%;
    height: 100%;

    display: none;

    justify-content: center;
    align-items: center;

    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;

    box-sizing: border-box;
}

.slide.active {
    display: flex;
}

        .slide.active {

            display: flex;

            animation: fadeIn 0.5s ease;
        }


        @keyframes fadeIn {

            from {
                opacity: 0;
                transform: scale(1.02);
            }

            to {
                opacity: 1;
                transform: scale(1);
            }

        }


        /* =========================
           DARK OVERLAY
        ========================= */

        .slide::before {

            content: "";

            position: absolute;

            inset: 0;

            background:
                linear-gradient(
                    rgba(0,0,0,0.40),
                    rgba(0,0,0,0.65)
                );

            z-index: 1;
        }


        /* =========================
           CONTENT BOX
        ========================= */

        .content {

            position: relative;

            z-index: 2;

            width: min(900px, 90%);

            padding: 45px;

            text-align: center;

            background: rgba(0,0,0,0.55);

            backdrop-filter: blur(6px);

            border: 2px solid rgba(255,255,255,0.25);

            border-radius: 18px;

            box-shadow:
                0 10px 40px rgba(0,0,0,0.6);
        }


        /* =========================
           HEADINGS
        ========================= */

        h1 {

            font-size: clamp(35px, 6vw, 70px);

            line-height: 1.4;

            margin-bottom: 25px;

            color: white;

            text-shadow:
                4px 4px 0px #000;
        }


        h2 {

            font-size: clamp(25px, 4vw, 50px);

            line-height: 1.5;

            margin-bottom: 30px;

            color: white;

            text-shadow:
                3px 3px 0px #000;
        }


        /* =========================
           TEXT
        ========================= */

        p {

            font-size: clamp(14px, 2vw, 22px);

            line-height: 2;

            color: #f5f5f5;

            text-shadow:
                2px 2px 0px #000;
        }


        /* =========================
           LIST
        ========================= */

        ul {

            text-align: left;

            font-size: clamp(13px, 2vw, 20px);

            line-height: 2.2;

            padding-left: 40px;

            text-shadow:
                2px 2px 0px #000;
        }


        li {
            margin-bottom: 10px;
        }


        /* =========================
           SLIDE NUMBER
        ========================= */

        .slide-number {

            position: fixed;

            bottom: 20px;
            right: 25px;

            z-index: 20;

            font-size: 10px;

            background: rgba(0,0,0,0.75);

            padding: 12px 15px;

            border-radius: 8px;

            border: 1px solid rgba(255,255,255,0.3);
        }


        /* =========================
           PROGRESS BAR
        ========================= */

        .progress {

            position: fixed;

            bottom: 0;
            left: 0;

            height: 4px;

            background: white;

            width: 0%;

            z-index: 200;

            transition: 0.3s;
        }


        /* =========================
           MOBILE NAVBAR
        ========================= */

        @media (max-width: 850px) {

            .navbar {

                height: 65px;

                padding: 0 15px;

            }

            .logo {

                font-size: 12px;

            }

            .nav-links {

                gap: 3px;

            }

            .nav-links button {

                font-size: 7px;

                padding: 9px 7px;

            }

        }


        @media (max-width: 600px) {

            .logo {
                display: none;
            }

            .navbar {
                justify-content: center;
            }

            .nav-links button {
                font-size: 6px;
                padding: 8px 5px;
            }

            .content {
                padding: 30px 20px;
            }

            .slide {
                padding: 90px 20px 40px;
            }

        }

        .content::before,
.content::after {
    display: none !important;
    content: none !important;
    background: none !important;
    border: none !important;
    box-shadow: none !important;
}

    </style>
</head>


<body>


    <!-- =========================
         NAVIGATION BAR
    ========================= -->

    <nav class="navbar">

        <div class="logo">
            Presentation
        </div>


        <ul class="nav-links">

            <li>
                <button
                    class="active"
                    onclick="showSlide(0)">
                    HOME
                </button>
            </li>

            <li>
                <button onclick="showSlide(1)">
                    INTRO
                </button>
            </li>

            <li>
                <button onclick="showSlide(2)">
                    OBJECTIVES
                </button>
            </li>

            <li>
                <button onclick="showSlide(3)">
                    DISCUSSION
                </button>
            </li>

            <li>
                <button onclick="showSlide(4)">
                    CONCLUSION
                </button>
            </li>

            <li>
                <button onclick="showSlide(5)">
                    THANK YOU
                </button>
            </li>

        </ul>

    </nav>



    <!-- =========================
         PRESENTATION
    ========================= -->

    <div class="presentation">


        <!-- HOME -->

        <section
            class="slide active"
            style="background-image: url('https://scontent.fmnl4-2.fna.fbcdn.net/v/t1.15752-9/833184364_1851784059145072_1384463217068957478_n.jpg?stp=dst-jpg_tt6&cstp=mx640x360&ctp=s640x360&_nc_cat=110&_nc_map=urlgen_bucketless&ccb=1-7&_nc_sid=9f807c&_nc_eui2=AeHiFyHSCfLSXQyGMtH6hh_nN9JmldoGQ2830maV2gZDb1_JStQI8HpuElYkER67uLT1ltNP7h35WAWXvFpaHkhA&_nc_ohc=aekxszVgbJIQ7kNvwFfIIjU&_nc_oc=AdoIDSBnwmiLuFVajDMwfol9wYCDpUGymT2rA0lanHNKtuNdWTvjvS-D9TiLW_4x7K0&_nc_zt=23&_nc_ht=scontent.fmnl4-2.fna&_nc_ss=7b2a8&oh=03_Q7cD6gHlp9x2YxChPEpm-rw0zHV2sWZ8_UT_iDBKpc3PKYh8eg&oe=6AEB3D1C');">

            <div class="content small-text">

                <h1>
                     GROUP 5
                </h1>

                <p>
                    Presented by:
                </p>

                <br>

                <p>
                    Santos, Cyruz. Tamayosa, Cyrus. Roldan, Gilbert. Tiangco, Ranz. Saripada, Alex.
                </p>

            </div>

        </section>



        <!-- INTRODUCTION -->

        <section
            class="slide"
            style="background-image: url('https://scontent.fmnl4-2.fna.fbcdn.net/v/t1.15752-9/833184364_1851784059145072_1384463217068957478_n.jpg?stp=dst-jpg_tt6&cstp=mx640x360&ctp=s640x360&_nc_cat=110&_nc_map=urlgen_bucketless&ccb=1-7&_nc_sid=9f807c&_nc_eui2=AeHiFyHSCfLSXQyGMtH6hh_nN9JmldoGQ2830maV2gZDb1_JStQI8HpuElYkER67uLT1ltNP7h35WAWXvFpaHkhA&_nc_ohc=aekxszVgbJIQ7kNvwFfIIjU&_nc_oc=AdoIDSBnwmiLuFVajDMwfol9wYCDpUGymT2rA0lanHNKtuNdWTvjvS-D9TiLW_4x7K0&_nc_zt=23&_nc_ht=scontent.fmnl4-2.fna&_nc_ss=7b2a8&oh=03_Q7cD6gHlp9x2YxChPEpm-rw0zHV2sWZ8_UT_iDBKpc3PKYh8eg&oe=6AEB3D1C');">

            <div class="content small-text">

                <p>
                  Disaster Relay: Emergency Logistics Simulator is a 2D game about helping people during a flood.In the game,the player needs to deliver food and medical supplies to evacuation centers,rescue civilians,and manage resources such as fuel and inventory.The player also needs to deal with flooded roads and other obstacles while trying to keep as many people safe as possible.
                </p>

            </div>

        </section>



        <!-- OBJECTIVES -->

        <section
            class="slide"
            style="background-image: url('https://scontent.fmnl4-2.fna.fbcdn.net/v/t1.15752-9/833184364_1851784059145072_1384463217068957478_n.jpg?stp=dst-jpg_tt6&cstp=mx640x360&ctp=s640x360&_nc_cat=110&_nc_map=urlgen_bucketless&ccb=1-7&_nc_sid=9f807c&_nc_eui2=AeHiFyHSCfLSXQyGMtH6hh_nN9JmldoGQ2830maV2gZDb1_JStQI8HpuElYkER67uLT1ltNP7h35WAWXvFpaHkhA&_nc_ohc=aekxszVgbJIQ7kNvwFfIIjU&_nc_oc=AdoIDSBnwmiLuFVajDMwfol9wYCDpUGymT2rA0lanHNKtuNdWTvjvS-D9TiLW_4x7K0&_nc_zt=23&_nc_ht=scontent.fmnl4-2.fna&_nc_ss=7b2a8&oh=03_Q7cD6gHlp9x2YxChPEpm-rw0zHV2sWZ8_UT_iDBKpc3PKYh8eg&oe=6AEB3D1C');">

            <div class="content small-text">

                <ul>

                    <li>
                        1.To deliver food and medical supplies to evacuation centers.
                    </li>

                    <li>
                        2.To rescue civilians affected by the flood.
                    </li>

                    <li>
                        3.To properly manage fuel and supplies.
                    </li>

                    <li>
                        4.To deal with flooded roads and road blockades.
                    </li>

                    <li>
                        5.To use the right emergency vehicle for different situations.
                    </li>

                    <li>
                        6.To keep the community survival rate as high as possible.
                    </li>

                    <li>
                        7.To use Python programming concepts in creating the game.
                    </li>
        
                </ul>

            </div>

        </section>



        <!-- DISCUSSION -->

        <section
            class="slide"
            style="background-image: url('https://scontent.fmnl4-2.fna.fbcdn.net/v/t1.15752-9/833184364_1851784059145072_1384463217068957478_n.jpg?stp=dst-jpg_tt6&cstp=mx640x360&ctp=s640x360&_nc_cat=110&_nc_map=urlgen_bucketless&ccb=1-7&_nc_sid=9f807c&_nc_eui2=AeHiFyHSCfLSXQyGMtH6hh_nN9JmldoGQ2830maV2gZDb1_JStQI8HpuElYkER67uLT1ltNP7h35WAWXvFpaHkhA&_nc_ohc=aekxszVgbJIQ7kNvwFfIIjU&_nc_oc=AdoIDSBnwmiLuFVajDMwfol9wYCDpUGymT2rA0lanHNKtuNdWTvjvS-D9TiLW_4x7K0&_nc_zt=23&_nc_ht=scontent.fmnl4-2.fna&_nc_ss=7b2a8&oh=03_Q7cD6gHlp9x2YxChPEpm-rw0zHV2sWZ8_UT_iDBKpc3PKYh8eg&oe=6AEB3D1C');">

            <div class="content small-text">

                <p>
                    DisasterRelay: Emergency Logistics Simulator is a strategy and simulation game that challenges players to manage emergency situations during a flood disaster. Players must use different vehicles to deliver supplies, rescue stranded civilians, transport patients, and reach evacuation centers before time runs out. Rising flood levels, blocked roads, limited resources, and civilian health conditions require players to make quick and careful decisions. These features make the game challenging while also showing the importance of proper planning and coordination during disasters.                </p>

            </div>

        </section>



        <!-- CONCLUSION -->

        <section
            class="slide"
            style="background-image: url('https://scontent.fmnl4-2.fna.fbcdn.net/v/t1.15752-9/833184364_1851784059145072_1384463217068957478_n.jpg?stp=dst-jpg_tt6&cstp=mx640x360&ctp=s640x360&_nc_cat=110&_nc_map=urlgen_bucketless&ccb=1-7&_nc_sid=9f807c&_nc_eui2=AeHiFyHSCfLSXQyGMtH6hh_nN9JmldoGQ2830maV2gZDb1_JStQI8HpuElYkER67uLT1ltNP7h35WAWXvFpaHkhA&_nc_ohc=aekxszVgbJIQ7kNvwFfIIjU&_nc_oc=AdoIDSBnwmiLuFVajDMwfol9wYCDpUGymT2rA0lanHNKtuNdWTvjvS-D9TiLW_4x7K0&_nc_zt=23&_nc_ht=scontent.fmnl4-2.fna&_nc_ss=7b2a8&oh=03_Q7cD6gHlp9x2YxChPEpm-rw0zHV2sWZ8_UT_iDBKpc3PKYh8eg&oe=6AEB3D1C');">

            <div class="content small-text">

                <p>
                   In conclusion, DisasterRelay aims to provide an engaging and challenging disaster-response experience while highlighting the importance of helping communities during emergencies. The game encourages players to think strategically, manage resources wisely, and prioritize urgent situations. Through its different vehicles, changing environments, and time-based challenges, the game can provide an enjoyable experience while giving players a better understanding of the difficulties involved in disaster response and relief operations.                </p>

            </div>

        </section>



        <!-- THANK YOU -->

        <section
            class="slide"
            style="background-image: url('https://scontent.fmnl4-2.fna.fbcdn.net/v/t1.15752-9/833184364_1851784059145072_1384463217068957478_n.jpg?stp=dst-jpg_tt6&cstp=mx640x360&ctp=s640x360&_nc_cat=110&_nc_map=urlgen_bucketless&ccb=1-7&_nc_sid=9f807c&_nc_eui2=AeHiFyHSCfLSXQyGMtH6hh_nN9JmldoGQ2830maV2gZDb1_JStQI8HpuElYkER67uLT1ltNP7h35WAWXvFpaHkhA&_nc_ohc=aekxszVgbJIQ7kNvwFfIIjU&_nc_oc=AdoIDSBnwmiLuFVajDMwfol9wYCDpUGymT2rA0lanHNKtuNdWTvjvS-D9TiLW_4x7K0&_nc_zt=23&_nc_ht=scontent.fmnl4-2.fna&_nc_ss=7b2a8&oh=03_Q7cD6gHlp9x2YxChPEpm-rw0zHV2sWZ8_UT_iDBKpc3PKYh8eg&oe=6AEB3D1C');">

            <div class="content small-text">

                <h1>
                    That's all Thanku for listening!
                </h1>

            </div>

        </section>


    </div>



    <!-- SLIDE NUMBER -->

    <div class="slide-number">

        <span id="current">
            1
        </span>

        /

        <span id="total">
            6
        </span>

    </div>



    <!-- PROGRESS BAR -->

    <div
        class="progress"
        id="progress">
    </div>



    <script>

        let currentSlide = 0;

        const slides =
            document.querySelectorAll(".slide");

        const navButtons =
            document.querySelectorAll(".nav-links button");

        const totalSlides =
            slides.length;


        document.getElementById("total")
            .textContent = totalSlides;



        function showSlide(index) {

            if (index < 0) {
                index = totalSlides - 1;
            }

            if (index >= totalSlides) {
                index = 0;
            }


            currentSlide = index;


            /* Hide all slides */

            slides.forEach(slide => {

                slide.classList.remove("active");

            });


            /* Show selected slide */

            slides[currentSlide]
                .classList.add("active");


            /* Update navbar */

            navButtons.forEach(button => {

                button.classList.remove("active");

            });


            navButtons[currentSlide]
                .classList.add("active");


            /* Slide number */

            document.getElementById("current")
                .textContent =
                currentSlide + 1;


            /* Progress */

            const progress =
                ((currentSlide + 1) /
                totalSlides) * 100;


            document.getElementById("progress")
                .style.width =
                progress + "%";

        }



        /* Keyboard controls */

        document.addEventListener(
            "keydown",
            function(event) {

                if (event.key === "ArrowRight") {

                    showSlide(currentSlide + 1);

                }

                if (event.key === "ArrowLeft") {

                    showSlide(currentSlide - 1);

                }

            }
        );


        /* Start */

        showSlide(0);

    </script>


</body>
</html>


</body>
</html>
