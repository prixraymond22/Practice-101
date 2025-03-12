<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Date?</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f8ff;
            font-family: Arial, sans-serif;
            text-align: center;
        }
        h1 {
            color: #2c3e50;
            display: none; /* Initially hidden */
        }
        .envelope {
            width: 100px;
            height: 60px;
            background-color: #fff;
            border: 2px solid #2c3e50;
            border-radius: 5px;
            position: relative;
            cursor: pointer;
            transition: transform 0.3s;
        }
        .envelope:hover {
            transform: scale(1.1);
        }
        .envelope:before {
            content: '';
            position: absolute;
            top: -20px;
            left: 10px;
            width: 80px;
            height: 20px;
            background-color: #2c3e50;
            border-radius: 5px;
        }
        button {
            padding: 10px 20px;
            margin: 10px;
            font-size: 16px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .yes {
            background-color: #28a745;
            color: white;
        }
        .no {
            background-color: #dc3545;
            color: white;
        }
        .error {
            color: #dc3545;
            display: none;
        }
    </style>
</head>
<body>

<div>
    <div class="envelope" onclick="showMessage()"></div>
    <h1 id="message">Will you be my date on Saturday?</h1>
    <button class="yes" id="yesButton" style="display:none;" onclick="handleYes()">Yes</button>
    <button class="no" id="noButton" style="display:none;" onclick="handleNo()">No</button>
    <p class="error" id="error-message">Please say yes!</p>
</div>

<script>
    function showMessage() {
        document.getElementById("message").style.display = "block";
        document.getElementById("yesButton").style.display = "inline-block";
        document.getElementById("noButton").style.display = "inline-block";
    }

    function handleYes() {
        window.location.href = "date-details.html"; // Redirect to date details page
    }

    function handleNo() {
        document.getElementById("error-message").style.display = "block"; // Show error message
    }
</script>

</body>
</html>
