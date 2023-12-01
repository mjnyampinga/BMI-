function calculateBMI() {
  // Get weight and height input values
  const weight = parseFloat(document.getElementById('weight').value);
  const height = parseFloat(document.getElementById('height').value);

  // Check if inputs are valid
  if (isNaN(weight) || isNaN(height) || weight <= 0 || height <= 0) {
    alert('Please enter valid values for weight and height.');
    return;
  }

  // Calculate BMI
  const bmi = calculateBMIFromValues(weight, height);

  // Display the result with an explanation
  displayResult(bmi);
}

function calculateBMIFromValues(weight, height) {
  // BMI formula: weight / (height * height)
  const bmi = weight / (height * height);
  // Round to two decimal places
  return bmi.toFixed(2);
}

function displayResult(bmi) {
  // Get the result element and update its content with an explanation
  const resultElement = document.getElementById('result');
  resultElement.textContent = `Your BMI is: ${bmi}.`;

  // Add explanations based on BMI categories
  if (bmi < 18.5) {
    resultElement.textContent += ' This falls into the "Underweight" category. Individuals with a BMI less than 18.5 may be at risk of nutritional deficiencies and other health issues.';
  } else if (bmi >= 18.5 && bmi <= 24.9) {
    resultElement.textContent += ' This falls into the "Normal Weight" category. Individuals with a BMI between 18.5 and 24.9 are generally considered to have a healthy weight relative to height.';
  } else if (bmi >= 25 && bmi <= 29.9) {
    resultElement.textContent += ' This falls into the "Overweight" category. Individuals with a BMI between 25 and 29.9 may have a higher risk of certain health issues, such as heart disease and type 2 diabetes.';
  } else {
    resultElement.textContent += ' This falls into the "Obesity" category. Individuals with a BMI of 30 or greater may be at a significant risk of various health conditions, including cardiovascular diseases, diabetes, and certain types of cancer.';
  }
}
