# Interview-Questions-Coding

### 1. Convert 12 hour time format into 24 hour format
```sh
function convert(str){
    var d = str.split(" ");
    var t = d[0].split(':');
    if(d[1] === 'PM' && t[0] !== '12'){
      return (parseInt(t[0])+12 + ':' + t[1]);
    }else if(d[1] === 'AM' && t[0] === '12'){
        return (parseInt(t[0])+12 + ':' + t[1]);
      }
    return d[0];
}

console.log(convert("11:00 PM")); // 23:00
console.log(convert("11:00 AM")); //11:00
console.log(convert("12:00 PM")); //12:00
console.log(convert("12:00 AM")); //24:00

```

### 2. check the given string is pangram or not
```sh
const pangram = (str) =>{
    str = str.toUpperCase();
    var flag = true;
    for(var i=65; i<=90; i++){
        if(!str.includes(String.fromCharCode(i))){
            flag = false;
            break;
        }
    }
  if(flag) console.log('Yes')
  else console.log('No')
}

pangram("the quick brown fox jumps over the lazy dog"); // Yes
pangram("Suresh"); // No
```



  
