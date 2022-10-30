### 프로그래머스

## 10월 4주차 티어전
### 레벨 1 (브론즈)
### 참가자
[보리사랑](https://github.com/yusw10) 🏅
[핀](https://github.com/finnn1)

### 문제 풀이
:::info
1-1. 입력된 수가 짝수라면 2로 나눕니다.
1-2. 입력된 수가 홀수라면 3을 곱하고 1을 더합니다. 
2. 결과로 나온 수에 같은 작업을 1이 될 때까지 반복합니다.
:::

```swift
func solution(_ num:Int) -> Int {
    var userInput = num
    var count = 0

    while userInput > 1 {
        if count == 500 {
            count = -1
            break
        }

        count += 1

        if userInput % 2 == 0 {
            userInput = userInput / 2
        } else {
            userInput = (userInput * 3) + 1
        }
    }

    return count
}
```
### 알게된 점
보리와 함께 문제를 풀며 로직 별로 메서드로 분리하면 나중에 어디서 문제가 발생했는지 확인하기 쉽다는 것을 배울 수 있었다. 👍👍

