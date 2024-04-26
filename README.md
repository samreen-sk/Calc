# Ex.08 Design of a Standard Calculator
## Date:25-04-2024

## AIM:
To design a web application for a standard calculator with minimum five operations.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for creating attractive colors.

### Step 4:
Write JavaScript program for implementing five different operations.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
//calc.html


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Math Calculator</title>
    <link rel="stylesheet" href="style.css">
</head>
<body bgcolor="lightblue">
    <div class="container">
        <h1>CALCULATOR</h1>
        <h3 class="text">SHAIK SAMREEN (212223110047)</h3><br>

        <div class="calculator">
            <input type="text" name="screen" id="screen">
            <table>
                <tr>
                    <td><button class="color">(</button></td>
                    <td><button class="color">)</button></td>
                    <td><button class="color">C</button></td>
                    <td><button class="color">%</button></td>
                </tr>
                <tr>
                    <td><button>7</button></td>
                    <td><button>8</button></td>
                    <td><button>9</button></td>
                    <td><button class="color">*</button></td>
                </tr>
                <tr>
                    <td><button>4</button></td>
                    <td><button>5</button></td>
                    <td><button>6</button></td>
                    <td><button class="color">-</button></td>
                </tr>
                <tr>
                    <td><button>1</button></td>
                    <td><button>2</button></td>
                    <td><button>3</button></td>
                    <td><button class="color">+</button></td>
                </tr>
                <tr>
                    <td><button>0</button></td>
                    <td><button class="color">.</button></td>
                    <td><button class="color">/</button></td>
                    <td><button class="color">=</button></td>
                </tr>
            </table>
        </div>
    </div>

    <script src="index.js"></script>
</body>
</html>

//index.js


let screen = document.getElementById('screen');
buttons = document.querySelectorAll('button');
let screenValue = '';
for (item of buttons) {
    item.addEventListener('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is ', buttonText);
        if (buttonText == 'X') {
            buttonText = '*';
            screenValue += buttonText;
            screen.value = screenValue;
        }
        else if (buttonText == 'C') {
            screenValue = "";
            screen.value = screenValue;
        }
        else if (buttonText == '=') {
            screen.value = eval(screenValue);
        }
        else {
            screenValue += buttonText;
            screen.value = screenValue;
        }
    })
}

//style.css

.container {
    text-align: center;
    margin-top: 23px;
}

.calculator {
    border: none;
    background-color: #be4b99;
    padding: 30px;
    border-radius: 0px;
    display: inline-block;
}

h1 {
    font-size: 40px;
    font-family: Arial, Helvetica, sans-serif;
}

h3 {
    font-size: 25px;
    font-weight: bold;
    color: black;
    text-align: center;
    margin: border;
    margin-top: 20px;
}

input {
    text-align: right;
    border-radius: 21px;
    border: 2px solid rgb(253, 240, 240);
    padding: 20px;
    background: rgb(242, 241, 241);
    font-size: 40px;
    height: 60px;
    width: 290px;
    color: rgb(11, 11, 11);
}

table {
    margin: auto;
}

button {
    border-radius: 20px;
    border: 10;
    outline: 0px;
    box-shadow: -8px -8px 15px rgba(180, 180, 180, 0.1),  5px 5px 15px rgba(0, 0, 0, 0.2);
    font-size: 20px;
    background: rgb(227, 129, 201);
    color: rgb(11, 11, 11);
    width: 60px;
    height: 60px;
    margin: 6px;
    cursor: pointer;
}

.color {
    color: rgb(247, 236, 236);
}

```
## OUTPUT:
![alt text](<Screenshot 2024-04-26 224528.png>)

![alt text](<Screenshot 2024-04-26 224548.png>)

## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
