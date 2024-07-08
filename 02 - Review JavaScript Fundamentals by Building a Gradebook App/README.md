
# Student Grades Calculation

This project is a part of the JavaScript Algorithms and Data Structures certification on freeCodeCamp. By completing this project, I have learned various JavaScript concepts such as functions, loops, conditionals, and how to solve real-world problems with code. The project involves calculating average scores, converting scores to letter grades, determining if a student has a passing grade, and messaging the student with their results.

## Project Overview

The project consists of four main steps:
1. Calculating the average score for a class.
2. Converting numerical scores to letter grades.
3. Checking if a student has a passing grade.
4. Messaging the student with their results.

## What I Have Learned

### 1. Calculating the Average Score

#### Step 1: Calculate the Average Score

The `getAverage` function takes an array of test scores and returns the average score.

**Example Code:**

```javascript
function getAverage(scores) {
    // Variable to store the sum of all scores
    let total = 0;
    
    // Loop through the scores array and add each score to the total
    for (let i = 0; i < scores.length; i++) {
        total += scores[i];
    }
    
    // Calculate the average by dividing the total by the number of scores
    let average = total / scores.length;
    
    // Return the average
    return average;
}

// Test the function with provided test cases
console.log(getAverage([92, 88, 12, 77, 57, 100, 67, 38, 97, 89])); // Expected output: 71.7
console.log(getAverage([45, 87, 98, 100, 86, 94, 67, 88, 94, 95])); // Expected output: 85.4
```

### 2. Converting Scores to Letter Grades

#### Step 2: Convert Scores to Letter Grades

The `getGrade` function takes a number score as a parameter and returns a string representing a letter grade based on the score.

**Example Code:**

```javascript
function getGrade(score) {
    if (score === 100) {
        return "A++";
    } else if (score >= 90) {
        return "A";
    } else if (score >= 80) {
        return "B";
    } else if (score >= 70) {
        return "C";
    } else if (score >= 60) {
        return "D";
    } else {
        return "F";
    }
}

// Test the function with provided test cases
console.log(getGrade(96)); // Expected output: "A"
console.log(getGrade(82)); // Expected output: "B"
console.log(getGrade(56)); // Expected output: "F"
```

### 3. Checking for a Passing Grade

#### Step 3: Check for a Passing Grade

The `hasPassingGrade` function takes a student score as a parameter and returns true if the student has a passing grade and false if they do not.

**Example Code:**

```javascript
function hasPassingGrade(score) {
    // Get the grade using the getGrade function
    const grade = getGrade(score);
    
    // Check if the grade is not "F"
    return grade !== "F";
}

// Test the function with provided test cases
console.log(hasPassingGrade(100)); // Expected output: true
console.log(hasPassingGrade(53));  // Expected output: false
console.log(hasPassingGrade(87));  // Expected output: true
```

### 4. Messaging the Student with Their Results

#### Step 4: Message the Student

The `studentMsg` function takes `totalScores` and `studentScore` as parameters and returns a string representing a message to the student. The message includes the class average and the student's grade, and indicates whether the student passed or failed the course.

**Example Code:**

```javascript
function studentMsg(totalScores, studentScore) {
    const average = getAverage(totalScores);
    const grade = getGrade(studentScore);
    const passed = hasPassingGrade(studentScore);
    
    let message = "Class average: " + average + ". Your grade: " + grade + ". ";
    
    if (passed) {
        message += "You passed the course.";
    } else {
        message += "You failed the course.";
    }
    
    return message;
}

// Test the function with provided test cases
console.log(studentMsg([92, 88, 12, 77, 57, 100, 67, 38, 97, 89], 37)); // Expected output: Class average: 71.7. Your grade: F. You failed the course.
console.log(studentMsg([45, 87, 98, 100, 86, 94, 67, 88, 94, 95], 87)); // Expected output: Class average: 85.4. Your grade: B. You passed the course.
```

## Conclusion

By working on this project, I have reinforced my understanding of basic JavaScript concepts and learned how to apply them to solve real-world problems. This project is a significant step in my journey to becoming proficient in JavaScript and web development.
