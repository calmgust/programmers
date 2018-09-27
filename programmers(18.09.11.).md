# 프로그래머스



## 이상한 문자 만들기 (level 1)

문자열 s는 한 개 이상의 단어로 구성되어 있습니다. 각 단어는 하나 이상의 공백문자로 구분되어 있습니다. 각 단어의 짝수번째 알파벳은 대문자로, 홀수번째 알파벳은 소문자로 바꾼 문자열을 리턴하는 함수, solution을 완성하세요.



**제한 사항**

* 문자열 전체의 짝/홀수 인덱스가 아니라, 단어(공백을 기준)별로 짝/홀수 인덱스를 판단해야합니다.



**입출력 예**

| s                 | return            |
| ----------------- | ----------------- |
| "try hello world" | "TrY HeLlO WoRlD" |



**입출력 예 설명**

"Try hello world"는 세 단어 "try", "hello", "world"로 구성되어 있습니다. 각 단어의 짝수번째 문자를 대문자로, 홀수번째 문자를 소문자로 바꾸면 "TrY", "HeLlo", "WoRlD"입니다. 따라서 "TrY HeLlO", "WoRlD"입니다. 따라서 "TrY HeLlO WoRlD"를 리턴합니다.



```javascript
function solution(s){
    
    var testArr = s.split(' ');
    var resultArr = [];
    
    for(var i = 0; i < testArr.length; i++){
        resultArr.push(' ');
        for(var j = 0; j < testArr[i].length; j++){
            if(j % 2 === 0){
                resultArr.push(testArr[i][j].toUpperCase());
            }
            else if(j % 2 === 1){
                resultArr.push(testArr[i][j].toUpperCase());
            }
        }
    }
    
    return resultArr.slice(1).join('');
    /*
    var result = [];
    for(var k = 1; k < resultArr.length; k++){
        result.push(resultArr[k]);
    }
    return result.join('');
    */
}

//-----
// 다른 사람들의 풀이

// 정규표현식
/*
function toWeirdCase(s){

  return s.toUpperCase().replace(/(\w)(\w)/g, function(a){return a[0].toUpperCase()+a[1].toLowerCase();})

}
*/
```

