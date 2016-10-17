![](https://thomas-ko.github.io/freecodecamp-redesign/assets/img/logo-navbar.png)
#Reverse a String
```javascript
function reverseString(str) {
  return str.split("").reverse().join("");
}

reverseString("hello");
```
# Factorialize a Number
```javascript
function factorialize(num) {
  var sum=1;
  if(num===0){
    return sum;
  }
  else{
    for(i=1;i<=num;i++){
      sum=sum*i;
    }
    return sum;
  }
}

factorialize(5);
```
#Check for Palindromes
```javascript
function palindrome(str) {
  var arra=str.replace(/\s/g,"").replace(/[^a-zA-Z0-9]/g,"").replace(/\W/g,"");
  var arrd=arra.toLocaleLowerCase().split("");
  var arr=arrd.toString();
  var arrr=arrd.reverse().toString();
  if(arr==arrr){
    return true;
  }
  else{
    return false;
  }
}
palindrome("eye");
```
#Find the Longest Word in a String
```javascript
function findLongestWord(str) {
  var arr=str.split(" ");
  var cc=new Array();
  for(i=0;i<arr.length;i++){
    cc[i]=arr[i].length;
  }
  var a=new Array(); 
  a=cc.sort(function(a,b){return a-b;});
  var ans=a[a.length-1]; 
  return ans;
}

findLongestWord("The quick brown fox jumped over the lazy dog");
```
#Title Case a Sentence
```javascript
function titleCase(str) {
  var arr=str.toLowerCase().split(" ");
  for(i=0;i<arr.length;i++){
   var arrt=arr[i].charAt(0);
    arr[i]=arr[i].replace(arrt,function replace(arrt){return arrt.toUpperCase();});
  }
  return arr.join(" ");
}

titleCase("I'm a little tea pot");
```
#Return Largest Numbers in Arrays
```javascript
function largestOfFour(arr) {
  var arre=[];  
  for(i=0;i<arr.length;i++){
    arr[i].sort(function(a,b){return a-b;});
    arre[i]=arr[i][3];  
  }
  return arre;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```
#Confirm the Ending
```javascript
function confirmEnding(str, target) {
  var arr=str.split(" ");
  var stt=arr[arr.length-1];
  var sta=stt.substr(-target.length);
  if(sta==target){ 
    return true;
  }
  else{
    return false;
  }
  return str;
}

confirmEnding("Bastian", "n");
```
#Repeat a string repeat a string
```javascript
function repeat(str, num) {
  var sum="";
  if(num>0){
    for(i=0;i<num;i++){
      sum=sum+str;
    }
    return sum;
  }
  else{
    return "";
  }
}

repeat("abc", 3);
```
#Truncate a string
```javascript
function truncate(str, num) {
  if(str.length>num){
    if(num>3){
      var stt=str.slice(0,num-3)+"...";
      return stt;
    }
    else{
      return str.slice(0,num)+"...";
      } 
    }
  else{
    return str;
  }
}

truncate("A-tisket a-tasket A green and yellow basket", 11);
```
#Chunky Monkey
```javascript
function chunk(arr, size) {
  var arrt=new Array();
  var arrr=new Array();
  for(i=0;i<arr.length/size;i++){
    arrt[i]=arr.slice(i*size,(i+1)*size);
    arrr.push(arrt[i]);
  }  return arrr;
}

chunk(["a", "b", "c", "d"], 2);
```
#Slasher Flick
```javascript
function slasher(arr, howMany) {
  var art=arr.slice(howMany);
  return art;
}

slasher([1, 2, 3], 2);
```
#Mutations
```javascript
function mutation(arr) {
  var str=arr[0].toLowerCase();
  var strr=arr[1].toLowerCase();
  var arrr=new Array();
  var arrt=new Array();
  arrr=strr.split(""); 
  for(i=0;i<strr.length;i++){
    arrt[i]=str.indexOf(arrr[i]);
  }
    if(arrt.indexOf(-1)>=0){
      return false;
    }
    else{
      return true;
    }
}

mutation(["hello", "hey"]);
```
#Falsy Bouncer
```javascript
function bouncer(arr) {
  var arrt=new Array();
  for(i=0;i<arr.length;i++){
    if(Boolean(arr[i])!=false){
      arrt.push(arr[i]);
    }
  }
  return arrt;
}

bouncer([7, "ate", "", false, 9]);
```
#Seek and Destroy
```javascript
function destroyer(arr) {
  var args = [];
  for(var i = 1; i < arguments.length; i++){
    args.push(arguments[i]);
  }
  var t = arr.filter(function(item,index,array){
    return args.indexOf(item) < 0;
  });
  return t;
}
destroyer([1, 2, 3, 1, 2, 3], 2, 3);
```
#Where do I belong
```javascript
function where(arr, num) {
  var arrt=new Array();
  var arrtt=new Array();
  arr.push(num);
  arrt=arr.sort(function(a,b){return a-b;});
  return arrt.indexOf(num);
}

where([40, 60], 50);
```
#Caesars Cipher
```javascript
function rot13(str) { 
  var arrt=new Array();
  for(i=0;i<str.length;i++){
    var asd=str.charCodeAt(i);
    if(asd>64&&asd<91){
      if(asd>77){
        arrt[i]= String.fromCharCode(asd-13);
      }
      else{
        arrt[i]= String.fromCharCode(asd+13);
      }
    }
    else{arrt[i]= String.fromCharCode(asd);}
  }
  return arrt.toString().replace(/,/g,"");
}

rot13("SERR PBQR PNZC");
```
