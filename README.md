<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Color Changer</title>
  <style>
    /* Container styles */
    .container {
      text-align: center;
      margin-top: 50px;
      font-family: Arial, sans-serif;
    }

    /* The color-changing box */
    #color-box {
      width: 200px;
      height: 200px;
      margin: 20px auto;
      background-color: lightblue;
      border: 2px solid #333;
      border-radius: 8px;
      transition: background-color 0.3s ease;
    }

    /* Button styling */
    #change-color-btn {
      padding: 10px 20px;
      font-size: 16px;
      background-color: #007bff;
      border: none;
      border-radius: 6px;
      color: white;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    #change-color-btn:hover {
      background-color: #0056b3;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Color Changer</h1>
    <div id="color-box"></div>
    <button id="change-color-btn">Change Color</button>
  </div>

  <script>
    document.addEventListener("DOMContentLoaded", () => {
      const colorBox = document.getElementById("color-box");
      const changeColorBtn = document.getElementById("change-color-btn");

      // Function to generate a random hex color
      function getRandomColor() {
        const letters = "0123456789ABCDEF";
        let color = "#";
        for (let i = 0; i < 6; i++) {
          color += letters[Math.floor(Math.random() * 16)];
        }
        return color;
      }

      // Event listener to change box color
      changeColorBtn.addEventListener("click", () => {
        const randomColor = getRandomColor();
        colorBox.style.backgroundColor = randomColor;
      });
    });
  </script>
</body>
</html>
