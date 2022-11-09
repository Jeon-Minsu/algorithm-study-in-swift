###### tags: `스터디`
# 알고리즘 티어전
## 11월 2주차

### 레벨

[PGS] Lv.0 저주의 숫자 3
 

### 참가자

[Derrick](https://github.com/derrickkim0109) 🏅 
[수꿍](https://github.com/Jeon-Minsu) 

### 문제 풀이

**문제 설명**
> 3의 배수, 3이 포함되는 숫자를 제외한 나머지 숫자에서 n번째 숫자를 반환하는 문제


```swift

import Foundation

func solution(_ n: Int) -> Int {
    var result = [Int]()
    var count = 0
    for number in 1...200 {
        if (number % 3 != 0)
            && (((number % 100) / 10) != 3)
            && (number / 10 != 3)
            && (number % 10) != 3 {
            result.append(number)

            if count == n {
                return result[n-1]
            }

            count += 1
        }
    }

    return 0
}


print(solution(100))

```

### 알게된 점

- 고차함수로 filter를 돌리면 결과값이 늦게 도출된다.
- 제한 사항 1 ≤ n ≤ 100로 인하여, 100이하의 숫자만을 구하는 줄 알았으나, 파라미터가 100까지 들어간다는 의미였다. 즉, 100 이상의 숫자가 충분히 들어갈 수 있다.


### 기타
- Derrick 승