# Advanced-Web-Technology

Assignment No - 1 

Write a ECMA Script program that will return 1 if the array is sorted in ascending order,-1 if it is sorted in descending order or 0  if it is not sorted.

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


  Assignment No - 2
  Write a ECMAScript program to convert an asynchronous function to return a promise.

  console.log("line 1")
let promise = new Promise((resolve,reject)=>{
let str1="hi";
let str2="hi";
setTimeout(()=>;
{
if(str1 === str2){
resolve("success");
}
else{
reject("failed");
}
},2000)
});

promise.then((message)=>;{
console.log("My self Mayuri");
})
.catch((message)=>{
console.log("completed");
});
console.log("line2");
console.log("line3")

output:
line 1
line2
line3
My self Mayuri

Assignment No :- 3

Title :- Read & Write File in Node.js

const file=require('fs'); const write=()=>{
file.writeFile("test.txt","new updated content",err=>{ if(err){
console.log(err);
}
else{
console.log("success");
}
})
}

const read=()=>{
file.readFile("test.txt",(err,data)=>{ if(err){
console.log(err);
}
else{
console.log(data.toString());
}
})
}
const append=()=>{
file.appendFile("test.txt","append",(err,data)=>{ if(err){
console.log(err);
}
else{
console.log("success");
}
})
}
write(); read();
append();

Assignment No - 4

Const express = require('express');
const app = express();

app.get('/',(req,res)=>{
    res.send("welcome to MCA");
});
app.listen(4000,()=>{
    console.log("Listen to port 4000")
});
