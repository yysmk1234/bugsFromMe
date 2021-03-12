## promise中的错误处理

promise中出现错误，一般使用 rejcet（）处理，但是 reject（）可以通过 then（）函数获取或者通过 catch（）进行错误的处理。但是 catch 中的错误无法被
抛出，必须通过 throw（）才能返回，如果不进行处理，是无法获取到错误，程序就会阻塞。

```
function test(){
  return new Promise((resolve,reject)=>{
    //do sth
     
     if(err){
        reject(err)
     }
     resolve(result);
     
  }).catch(err=>{
     throw(err);
  })
}
```
