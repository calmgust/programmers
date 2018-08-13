# 프로그래머스



## 약수의 합 (level 1)

자연수 n을 입력받아 n의 약수를 모두 더한 값을 리턴하는 함수, solution을 완성해주세요.



**제한 사항**

* n은 0 이상 3000 이하인 자연수입니다.



**입출력 예**

| n    | return |
| ---- | ------ |
| 12   | 28     |
| 5    | 6      |



입출력 예 설명



입출력 예 #1

12의 약수는 1, 2, 3, 4, 6, 12입니다. 이를 모두 더하면 28입니다.



입출력 예 #2

5의 약수는 1, 5입니다. 이를 모두 더하면 6입니다.



```javascript
function solution(n){
    var arr = [];
    for(var i = 0; i <= n; i++){
        if(n % i === 0){
            arr.push(i);
        }
    }
    var sum = 0;
    for(var j = 0; j < arr.length; j++){
        sum = sum + arr[j];
    }
    return sum;
}


//-----

function solution(n){
    var arr = [];
    for(var i = 0; i <= n; i++){
        if(n % i === 0){
            arr.push(i);
        }
    }
    return arr.reduce((a, b) => a + b);
}
//실패 코드
```

