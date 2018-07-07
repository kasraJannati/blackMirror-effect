<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .mystyle{
            background: url("break.jpg") no-repeat center center fixed;
            background-size: cover;
        }
        body{
            background: #000000;
        }
        h1{
            color:#ffffff;
            text-transform: uppercase;
            cursor: default;
            font-family: Arial;
            font-size: 10em;
            width: 100%;
            text-align: center;
            position: absolute;
            top: 35%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
        span{
            transition: all ease 10s;
        }
        #a2,#r,#k{
            display: inline-block;

        }
    </style>
</head>
    <body id="body" onload="myFunction(document.getElementById('run'))">
    <h1 id="run">
        <span id="k">k</span>
        <span id="a">a</span>
        <span id="s">s</span>
        <span id="r">r</span>
        <span id="a2">a</span>
    </h1>

    <audio autoplay controls id="vid">
        <source src="break.m4a" type="audio/mp4">
        <source src="break.m4a" type="audio/mp4">
        Your browser does not support the audio element.
    </audio>

    <script>
        function myFunction(obj){
            document.getElementById('vid').play();

            var orig = obj.style.color;
            obj.style.color = '#ffffff';
            setTimeout(function(){
                obj.style.color = "#ffffff";
                document.getElementById("k").style.opacity = "0.1";
                document.getElementById("k").style.textShadow = "-30px 10px 30px #fff";
                document.getElementById("a").style.textShadow = "10px 10px 10px #fff";
                document.getElementById("s").style.textShadow = "15px 15px 15px #fff";
                document.getElementById("s").style.opacity = "0.5";
                document.getElementById("r").style.color = "transparent";
                document.getElementById("r").style.textShadow = "0 0 5px rgba(255,255,255,0.5)";
                document.getElementById("a2").style.color = "transparent";
                document.getElementById("a2").style.textShadow = "0 0 5px rgba(255,255,255,0.5)";
                document.getElementById("a2").style.transform = "rotate(50deg)";
                document.getElementById("r").style.transform = "scale(1.5)";
                document.getElementById("k").style.transform = "scale(0.5)";
            }, 2000);

            setTimeout(function(){
                var element = document.getElementById("body");
                element.classList.add("mystyle");
            }, 10000);
        }
    </script>
</body>
</html>
