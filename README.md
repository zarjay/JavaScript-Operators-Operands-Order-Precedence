# JavaScript-Operators-Operands-Order-Precedence
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Grade Average Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            background-color: #fff;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
            text-align: center;
        }
        h1 {
            color: #333;
        }
        .result {
            margin-top: 20px;
            font-size: 1.2em;
        }
        .subject {
            margin: 10px 0;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Grade Average Calculator</h1>
        <div class="result" id="result"></div>
    </div>

    <script>
        const subjects = ["CONTEMPORARY WORLD", "GENDER & SOCIETY", "CALCULUS", "UNDERSTANDING THE SELF", "COMPUTER PROGRAMMING II"];
        const grades = [1.00, 1.25, 1.50, 1.25, 1.75];

        const totalGrades = grades.reduce((sum, grade) => sum + grade, 0);
        const average = totalGrades / grades.length;

        let output = "";
        for (let i = 0; i < subjects.length; i++) {
            output += `<div class="subject">${subjects[i]}: ${grades[i]}</div>`;
        }
        output += `<div class="subject"><strong>Total Average: ${average.toFixed(2)}</strong></div>`;

        document.getElementById('result').innerHTML = output;
    </script>
</body>
</html>
