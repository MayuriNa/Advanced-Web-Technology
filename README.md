# Advanced-Web-Technology
function checkArrayOrder(arr) {
    // Check for ascending order
    if (arr.every((element, index, array) => index === 0 || element >= array[index - 1])) {
      return 1; 
    }
  
    // Check for descending order
    if (arr.every((element, index, array) => index === 0 || element <= array[index - 1])) {
      return -1;
    }
  
   
    return 0;
  }
  
  
  const ascendingArray = [1, 2, 3, 4, 5];
  const descendingArray = [5, 4, 3, 2, 1];
  const unsortedArray = [3, 1, 4, 2, 5];
  
  console.log(checkArrayOrder(ascendingArray)); // Output: 1
  console.log(checkArrayOrder(descendingArray)); // Output: -1
  console.log(checkArrayOrder(unsortedArray));   // Output: 0
