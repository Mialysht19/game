<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Love Animation</title>
    <style>
        body { 
            display: flex; 
            justify-content: center; 
            align-items: center; 
            height: 100vh; 
            background-color: pink; 
            margin: 0;
        }
        .heart {
            position: relative;
            width: 100px;
            height: 100px;
            background-color: red;
            transform: rotate(-45deg);
            animation: beat 1s infinite;
        }
        .heart:before,
        .heart:after {
            content: "";
            position: absolute;
            width: 100px;
            height: 100px;
            background-color: red;
            border-radius: 50%;
        }
        .heart:before {
            top: -50px;
            left: 0;
        }
        .heart:after {
            top: 0;
            left: 50px;
        }
        @keyframes beat {
            0%, 100% { transform: scale(1) rotate(-45deg); }
            50% { transform: scale(1.2) rotate(-45deg); }
        }
    </style>
</head>
<body>
    <div class="heart"></div>
</body>
</html>
