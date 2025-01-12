Here's the markdown documentation for your Calculator App project named "Mrio":

```markdown
# Mrio - Calculator App

Welcome to **Mrio**, a simple yet functional calculator app built using **HTML**, **CSS**, and **JavaScript**. This project demonstrates how to create an interactive web-based calculator.

---

## Features

- Perform basic arithmetic operations: Addition, Subtraction, Multiplication, and Division.
- Simple and clean user interface.
- Real-time input display and result calculation.

---

## Technologies Used

- **HTML**: To structure the web page.
- **CSS**: To style the layout and design of the app.
- **JavaScript**: To add the functionality and logic behind the calculator operations.

---

## Screenshots

Here are a few screenshots of the app in action:

![Calculator App Screenshot](path-to-screenshot.jpg)

---

## Project Structure

```
/Mrio
│
├── index.html        # The main HTML file
├── style.css         # The CSS file for styling
├── script.js         # JavaScript file for logic
└── README.md         # Project documentation
```

---

## How to Run the App

1. Clone the repository:

   ```bash
   git clone https://github.com/your-repo/Mrio.git
   ```

2. Navigate to the project folder:

   ```bash
   cd Mrio
   ```

3. Open `index.html` in your web browser to see the app in action.

---

## Example Usage

Here is an example of how to use the calculator:

- Click the numbers and operators on the screen to input the values.
- Press the "=" button to get the result.
- Press "C" to clear the display.

---

## Code Example

### HTML (index.html)
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mrio - Calculator App</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="calculator">
        <input type="text" id="display" disabled />
        <div class="buttons">
            <button onclick="appendNumber('7')">7</button>
            <button onclick="appendNumber('8')">8</button>
            <button onclick="appendNumber('9')">9</button>
            <button onclick="setOperator('+')">+</button>
            <!-- Other buttons go here -->
        </div>
        <button onclick="clearDisplay()">C</button>
        <button onclick="calculateResult()">=</button>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

### CSS (style.css)
```css
/* Basic styles for the calculator */
.calculator {
    width: 260px;
    margin: 50px auto;
    padding: 20px;
    border: 2px solid #ccc;
    border-radius: 10px;
    background-color: #f9f9f9;
}

#display {
    width: 100%;
    height: 40px;
    font-size: 24px;
    text-align: right;
    margin-bottom: 10px;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

button {
    width: 50px;
    height: 50px;
    font-size: 20px;
    margin: 5px;
    cursor: pointer;
}
```

### JavaScript (script.js)
```javascript
let currentInput = '';
let operator = null;
let firstOperand = null;

function appendNumber(number) {
    currentInput += number;
    document.getElementById('display').value = currentInput;
}

function setOperator(op) {
    if (firstOperand === null) {
        firstOperand = parseFloat(currentInput);
        currentInput = '';
        operator = op;
    }
}

function calculateResult() {
    if (operator && firstOperand !== null && currentInput !== '') {
        let secondOperand = parseFloat(currentInput);
        let result;

        switch (operator) {
            case '+':
                result = firstOperand + secondOperand;
                break;
            case '-':
                result = firstOperand - secondOperand;
                break;
            case '*':
                result = firstOperand * secondOperand;
                break;
            case '/':
                result = firstOperand / secondOperand;
                break;
            default:
                return;
        }

        document.getElementById('display').value = result;
        firstOperand = null;
        operator = null;
        currentInput = '';
    }
}

function clearDisplay() {
    firstOperand = null;
    operator = null;
    currentInput = '';
    document.getElementById('display').value = '';
}
```

---

## License

This project is open-source and available under the [MIT License](LICENSE).

---

## Contributing

Feel free to fork the repository and submit pull requests with any improvements or bug fixes!

---

Enjoy coding with Mrio! 🎉
```

This markdown file provides clear documentation for your Calculator app project, including an overview, usage instructions, and code examples. You can modify the paths and other details as needed for your repository.
