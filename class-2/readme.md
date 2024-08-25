
## **Review Session**

Let's break down and understand the given code step by step.

### **JavaScript Code Explanation**

```javascript
var a = 10;
var b = 20;
var c = 8;

var x = ((-b) + (((b * b) - (4 * a * c)) ** (1 / 2))) / (2 * a);

alert(x);
```

Let's dissect each part of this code:

#### **Variable Declarations**

```javascript
var a = 10;
var b = 20;
var c = 8;
```

- **`var a = 10;`**: Assigns the value 10 to variable `a`.
- **`var b = 20;`**: Assigns the value 20 to variable `b`.
- **`var c = 8;`**: Assigns the value 8 to variable `c`.

These variables represent coefficients in a quadratic equation of the form **ax² + bx + c = 0**.

#### **Calculating the Root using Quadratic Formula**

```javascript
var x = ((-b) + (((b * b) - (4 * a * c)) ** (1 / 2))) / (2 * a);
```

This line computes one of the roots of the quadratic equation using the quadratic formula:

**x = [ -b ± √(b² - 4ac) ] / 2a**

**Breakdown of the calculation:**

1. **`(b * b)`**: Calculates b squared (**b²**).
2. **`(4 * a * c)`**: Calculates 4ac.
3. **`(b * b) - (4 * a * c)`**: Computes the discriminant (**b² - 4ac**).
4. **`((b * b) - (4 * a * c)) ** (1 / 2)`**: Calculates the square root of the discriminant.
5. **`(-b) + ...`**: Adds the negative of b to the square root calculated above.
6. **`... / (2 * a)`**: Divides the result by 2a to get the root value.

**Note**: This calculation only computes one root (using the '+' in the ±). To compute the other root, you would replace the '+' with a '-' in the formula.

#### **Displaying the Result**

```javascript
alert(x);
```

- **`alert(x);`**: Displays the value of `x` in an alert dialog box.

**Result Explanation**:

Given the values:
- **a = 10**
- **b = 20**
- **c = 8**

The computation will yield a numerical value for `x` which is one of the solutions to the equation **10x² + 20x + 8 = 0**.

---

## **Real-World Example with Arithmetic Operators**

Let's create a real-world example that demonstrates the use of various arithmetic operators along with explanatory comments.

**Scenario**: Calculating the monthly payment for a car loan using the loan amount, annual interest rate, and loan term.

### **Code Example**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Car Loan Calculator</title>
</head>
<body>

<script>
    // Loan amount in dollars
    var principal = 25000; // The total loan amount for the car

    // Annual interest rate in percentage
    var annualInterestRate = 5; // Annual interest rate of 5%

    // Loan term in years
    var years = 5; // Loan duration of 5 years

    // Convert annual interest rate to monthly and decimal
    var monthlyInterestRate = (annualInterestRate / 100) / 12; // Dividing by 100 to convert percentage to decimal and by 12 for monthly rate

    // Total number of payments (months)
    var numberOfPayments = years * 12; // Multiplying years by 12 to get total months

    // Calculate monthly payment using the formula
    var numerator = principal * monthlyInterestRate; // Multiplying principal by monthly interest rate
    var denominator = 1 - (1 + monthlyInterestRate) ** (-numberOfPayments); // Calculating the denominator part of the formula using exponentiation

    var monthlyPayment = numerator / denominator; // Dividing numerator by denominator to get monthly payment

    // Calculate total payment over the entire term
    var totalPayment = monthlyPayment * numberOfPayments; // Multiplying monthly payment by total number of payments

    // Calculate total interest paid
    var totalInterest = totalPayment - principal; // Subtracting principal from total payment to get total interest

    // Display the results
    console.log("Monthly Payment: $" + monthlyPayment.toFixed(2)); // Logs monthly payment rounded to 2 decimal places
    console.log("Total Payment: $" + totalPayment.toFixed(2)); // Logs total payment rounded to 2 decimal places
    console.log("Total Interest Paid: $" + totalInterest.toFixed(2)); // Logs total interest paid rounded to 2 decimal places
</script>

</body>
</html>
```

### **Explanation of the Code**

1. **Variable Declarations**:
    - **`principal`**: The total loan amount needed to purchase the car.
    - **`annualInterestRate`**: The annual interest rate provided by the lender.
    - **`years`**: The duration of the loan in years.

2. **Interest Rate Conversion**:
    - **`monthlyInterestRate`**: Converts the annual interest rate to a monthly rate in decimal form by dividing by 100 (to convert percentage to decimal) and then by 12 (months in a year).

3. **Total Number of Payments**:
    - **`numberOfPayments`**: Calculates the total number of monthly payments by multiplying the number of years by 12.

4. **Monthly Payment Calculation**:
    - **`numerator`**: Calculates the numerator of the loan payment formula by multiplying the principal by the monthly interest rate.
    - **`denominator`**: Calculates the denominator using exponentiation. The formula uses the expression **(1 + r)^-n** where **r** is the monthly interest rate and **n** is the total number of payments.
    - **`monthlyPayment`**: Divides the numerator by the denominator to find the monthly payment amount.

5. **Total Payment and Interest Calculation**:
    - **`totalPayment`**: Calculates the total amount paid over the life of the loan by multiplying the monthly payment by the total number of payments.
    - **`totalInterest`**: Determines the total interest paid by subtracting the principal from the total payment.

6. **Displaying Results**:
    - **`console.log`** statements are used to display the monthly payment, total payment, and total interest paid. The **`toFixed(2)`** method rounds the numbers to two decimal places for currency formatting.

### **Output**

When you run this script, you will get the following output in the console:

```
Monthly Payment: $471.78
Total Payment: $28306.80
Total Interest Paid: $3306.80
```

**Explanation**:
- **Monthly Payment**: You need to pay $471.78 every month for 5 years.
- **Total Payment**: Over 5 years, you'll pay a total of $28,306.80.
- **Total Interest Paid**: Out of the total payment, $3,306.80 is the interest paid to the lender.

### **Use of Arithmetic Operators**

This example utilizes various arithmetic operators:

- **`+` (Addition)**: Used in `(1 + monthlyInterestRate)` and when concatenating strings in `console.log`.
- **`-` (Subtraction)**: Used in calculating `totalInterest` and in the exponent `(-numberOfPayments)`.
- **`*` (Multiplication)**: Used in calculating `numerator`, `numberOfPayments`, `totalPayment`.
- **`/` (Division)**: Used in converting interest rates and calculating `monthlyPayment`.
- **`**` (Exponentiation)**: Used in calculating the denominator with `(1 + monthlyInterestRate) ** (-numberOfPayments)`.
- **`()` (Parentheses)**: Used to control the order of operations and group calculations appropriately according to BODMAS rule.



## **Mathematical Formula**

The formula used in the code is derived from the **amortization formula** for calculating the monthly payment (EMI) on a loan.

**Monthly Payment (EMI)**:  
\[ \text{EMI} = \frac{P \cdot r \cdot (1 + r)^n}{(1 + r)^n - 1} \]

Where:
- \( P \) = Principal (Loan Amount)
- \( r \) = Monthly Interest Rate (Annual Interest Rate divided by 12 and converted to decimal)
- \( n \) = Total Number of Payments (Loan Term in years multiplied by 12)

**In the code, this formula is implemented as follows:**

### **Mathematical Representation of Code**

1. **Monthly Interest Rate Calculation**:
   \[
   r = \frac{\text{Annual Interest Rate}}{100 \times 12}
   \]
   - In the code: `var monthlyInterestRate = (annualInterestRate / 100) / 12;`

2. **Total Number of Payments Calculation**:
   \[
   n = \text{Years} \times 12
   \]
   - In the code: `var numberOfPayments = years * 12;`

3. **EMI Calculation**:
   \[
   \text{EMI} = \frac{P \cdot r \cdot (1 + r)^n}{(1 + r)^n - 1}
   \]

   - The **Numerator**:
     \[
     \text{Numerator} = P \times r
     \]
     - In the code: `var numerator = principal * monthlyInterestRate;`
   
   - The **Denominator**:
     \[
     \text{Denominator} = 1 - (1 + r)^{-n}
     \]
     - In the code: `var denominator = 1 - (1 + monthlyInterestRate) ** (-numberOfPayments);`
   
   - **Monthly Payment**:
     \[
     \text{Monthly Payment} = \frac{\text{Numerator}}{\text{Denominator}} = \frac{P \times r}{1 - (1 + r)^{-n}}
     \]
     - In the code: `var monthlyPayment = numerator / denominator;`

4. **Total Payment over the Entire Term**:
   \[
   \text{Total Payment} = \text{EMI} \times n
   \]
   - In the code: `var totalPayment = monthlyPayment * numberOfPayments;`

5. **Total Interest Paid**:
   \[
   \text{Total Interest} = \text{Total Payment} - P
   \]
   - In the code: `var totalInterest = totalPayment - principal;`

### **Summary of the Formula**
- The EMI formula calculates the fixed monthly payment required to fully repay a loan over a specified period.
- It accounts for both the principal and the interest accrued on the loan amount, ensuring equal payments each month.

This formula is widely used in financial calculations for loans, mortgages, and other forms of installment-based payments.

### **BODMAS Rule in Programming**

The **BODMAS** (Bracket, Order, Division, Multiplication, Addition, Subtraction) rule dictates the order in which operations are performed:

1. **Brackets**: Operations inside parentheses are performed first.
2. **Order**: Exponentiation operations are performed next.
3. **Division and Multiplication**: Performed from left to right.
4. **Addition and Subtraction**: Performed last, from left to right.

In our example, parentheses are used extensively to ensure calculations are performed in the correct order, especially in complex expressions like the denominator calculation.

---

## **Conclusion**

Understanding and effectively utilizing arithmetic operators along with proper application of mathematical rules like BODMAS is essential in programming to perform accurate calculations. Whether solving mathematical equations or calculating financial metrics, these fundamentals form the backbone of many computational tasks in software development.

Feel free to modify the values in the example to see how different loan terms and interest rates affect the payment calculations!

---
