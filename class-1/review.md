### Review Session: Alerts and Variables in JavaScript

In this session, we focused on two important JavaScript concepts: **alerts** and **variables**. Below is a summary of what we learned:

#### 1. **Using Alerts**

Alerts are a simple way to display messages to the user. They create a pop-up box with a specified message and an "OK" button.

- **Syntax**: 
  ```javascript
  alert("Your message here");
  ```
- **Example**:
  ```javascript
  alert("Hello! I am learning HTML");
  ```

  This will display a pop-up box with the message "Hello! I am learning HTML".

- You can also use `window.alert()` which works the same way:
  ```javascript
  window.alert("Hello");
  ```

#### 2. **Declaring Variables**

Variables are used to store data that can be used and manipulated throughout your code. In JavaScript, you declare a variable using the `var` keyword, followed by the variable name and its value.

- **Syntax**:
  ```javascript
  var variableName = "value";
  ```

- **Examples**:
  - **String Variable**: Stores text.
    ```javascript
    var topic_to_learn = "Learning HTML";
    var SLEEPINGTIME = "10:00 PM";
    ```
  
  - **Number Variable**: Stores a number.
    ```javascript
    var twoplustwo = 50;
    alert(twoplustwo); // Displays 50 in an alert box
    ```

  - **Using Variables in Alerts**:
    You can use variables in an `alert` to display their values.
    ```javascript
    alert(topic_to_learn);   // Displays "Learning HTML"
    alert("till");
    alert(SLEEPINGTIME);     // Displays "10:00 PM"
    ```

#### 3. **Undefined Variables**

If you declare a variable but do not assign a value to it, the variable is `undefined`. This can be used to check if a value has been assigned yet.

- **Example**:
  ```javascript
  var person_name;
  alert(person_name);  // Displays "undefined"
  ```

  After assigning a value, the variable will display the assigned value.
  
  ```javascript
  person_name = "Sufyan";
  alert(person_name);  // Displays "Sufyan"

  person_name = "Hassan";
  alert(person_name);  // Displays "Hassan"
  ```

This session provided a basic understanding of how to use alerts to interact with users and how to work with variables to store and manipulate data in your code.