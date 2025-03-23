# problem-solving-js

//Reverse a String
// Function to reverse a string
function reverseString(str) {
  // Convert the string into an array using split, reverse it, and then join it back to a string
  return str.split('').reverse().join('');
}

// Example usage
console.log(reverseString("hello")); 


//Find the Second-Largest Number in an Array
// Function to find the second-largest number in an array
function secondLargest(arr) {
  if (arr.length < 2) {
    return null; // If there are less than 2 elements, return null
  }
  
  // Remove duplicates by converting the array to a Set, then back to an array
  const uniqueArr = [...new Set(arr)];
  
  // Sort the array in descending order and return the second element
  uniqueArr.sort((a, b) => b - a);
  
  return uniqueArr[1]; // The second-largest number
}

// Example usage
console.log(secondLargest([1, 2, 3, 4, 5])); 


//Check if a Given String is a Palindrome
// Function to check if a string is a palindrome
function isPalindrome(str) {
  // Convert the string to lowercase and remove all non-alphanumeric characters
  const cleanedStr = str.toLowerCase().replace(/[^a-z0-9]/g, '');
  
  // Reverse the cleaned string and compare it with the original cleaned string
  return cleanedStr === cleanedStr.split('').reverse().join('');
}

// Example usage
console.log(isPalindrome("A man, a plan, a canal, Panama")); 

