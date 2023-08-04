# CODSOFT

## Flashlight App 🔦
### An app that turns on the device's flashlight when the app is launched and turns it off when the app is closed.

## Output
### https://github.com/Esraa200114/CODSOFT/assets/83236742/14d100af-38a0-48d8-a1fe-e9b99723f2fd

## Covered Rules
### 1. UI Design: The layout contains a single screen with a toggle button (`flashlightSwitch`) to control the flashlight. The `Switch` is provided for the user to turn the flashlight on and off.

### 2. Flashlight Functionality: The code checks for the availability of a camera flash on the device using `getPackageManager().hasSystemFeature(PackageManager.FEATURE_CAMERA_FLASH)`. If the device has a camera flash, it will use the `CameraManager` to turn on and off the flashlight based on the user's input (`isChecked` parameter).

### 3. App Lifecycle: The app handles the lifecycle events by overriding `onPause()` and `onDestroy()` methods. When the app is paused or destroyed, the flashlight is turned off using `flashLight(false)` to ensure the flashlight is not left on when the app is closed.

### 4. Error Handling: The code implements error handling for scenarios where the device doesn't have a camera flash or if the flashlight fails to turn on. If the device doesn't have a camera flash, it displays a toast message: "No flashlight available on your device." If there's any `CameraAccessException` during the flashlight operation, it prints the stack trace to handle the exception.

## Calculator App 🖩
### An app that performs basic arithmetic operations like addition, subtraction, multiplication, and division.

## Output
### https://github.com/Esraa200114/CODSOFT/assets/83236742/08012b49-5b86-4606-bc45-74db21fd2719

## Covered Rules
### 1. UI Design: The layout includes an equal button (=), a clear button , a clear-all button (AC), a dot character button (.), number buttons (0–9) and operator buttons (+, -, x, /), along with a display area to show the entered numbers, the operation being performed, and the results. 

### 2. Number Input: The `onNumberClickEvent` method captures user input when number buttons are pressed and stores the entered numbers for further processing. 

### 3. Operator Selection: The `onOperatorClickEvent` method enables the selection of arithmetic operators through button clicks and identifies the selected operator. 

### 4. Calculation: The `onEqualClickEvent` method performs arithmetic calculations based on the selected operator and handles division by zero and invalid operations. 

### 5. Display: The display area is updated in various parts of the code to show entered numbers, operators, and results. Decimal numbers are handled using the dot character button, and the rounding is performed using the `RoundingMode.HALF_UP mode`. In this project, I specified the number of decimal places to be 5. 

### 6. Clear and Reset: The `onAllClearClickEvent` method adds an all-clear button to reset the calculator, clearing entered numbers and resetting other variables. While the `onClearClickEvent` method is used to remove the last entered digit or dot character. 

### 7. Error Handling: The code includes various checks for error handling. For example, it shows appropriate messages for invalid input and operations and handles the display of errors in the result area.

### Invalid Operations and input such as:
#### 1. Division by zero.
#### 2. Having more than one decimal point in a number.
#### 3. Entering consecutive decimal points.
#### 4. Exceeding the character limit.
#### 5. Entering consecutive arithmetic operators.
#### 6. Starting with an operator without providing the first operand.
#### 7. Pressing the equal button without entering operands first.

### Handling Overflow: By checking if a BigDecimal variable called `output_big_decimal` exceeds the maximum value that can be represented by a double data type in Java. If it does, it is considered an overflow and a flag is set to `true` to indicate the overflow. The text color of the result field is changed to red and a text saying "Overflow occurred" is displayed in it. Otherwise, if no overflow is detected, the output is formated using the "FormatBigDecimal" function and the BigDecimal value is displayed in the result field.

