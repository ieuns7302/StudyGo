# 🔎 fmt 패키지
> 표준 입출력 기능을 제공하는 Go 언어 기본 패키지

</br>

## 선언 방법

``` Go
import "fmt"
```

</br>

## 출력

* fmt는 3 가지 표준 출력용 함수를 제공한다. </br></br>
  1. `Print()` : 함수 입력값들을 출력한다. </br>
  2. `Println()` : 함수 입력값들을 출력하고  개행한다.
  3. `Printf` : format에 맞도록 입력값들을 출력한다.

### 🧐 Example
---

</br>

``` Go
package main

import "fmt"

func main() {

	Number := 10
	Float := 3.141592

	fmt.Print("Num:", Number, "Flo:", Float)     // 1
	fmt.Println("Num:", Number, "Flo:", Float)         // 2
	fmt.Printf("Num: %d Flo: %f \n", Number, Float)    // 3
}

```

</br>

#### 1. Print() 함수
---
* 기본 서식에 맞춰서 출력
* 출력이 끝나고 개행을 하지 않기 때문에 바로 `2` 출력 결과와 이어진다.

</br></br>

#### 2. Println() 함수
---
* 기본 서식에 맞춰서 출력
* `1`과 다른 점은 출력값 사이에 공란을 삽입하고 출력이 끝나면 개행한다는 점이 있다.

</br></br>

#### 3. Printf() 함수
---
* 주어진 사용자 서식에 맞춰서 입력값을 출력
* 출력 서식에 입력값들이 들어갈 자리를 만들어주고 각 입력값이 해당 자리에 들어가게 된다.
  * 값이 들어갈 자리는 서식 문자를 적는다.

</br></br>

## 입력

* fmt는 3가지 표준 입력용 함수를 제공한다. </br></br>
  1. `Scan()` : 표준 입력에서 값을 입력 받는다.
  2. `Scanf()` : 표준 입력에서 서식 형태로 값을 입력받는다.
  3. `Scanln()` : 표준 입력에서 한 줄을 읽어서 값을 입력받는다.

### 🧐 Example

#### 1. Scan()
> 값을 채워넣을 변수들의 메모리 주소를 인수로 받는다.
```Go
func Scan(a ...interface{}) (n int, err error)
```
  * 함수 반환값은 성공저긍로 입력한 값 개수와 입력 실패시 에러를 반환한다.

</br>

#### 2. Scanf()
> 서식에 맞춘 입력을 받는다.
```Go
func Scanf(format string, a ...interface{}) (n int, err error)
```
  * 한줄 띄우기에 맞춰진 입력을 받는다.

</br>

#### 3. Scanln()
> 한 줄을 입력받아서 인수로 들어온 변수 메모리 주소에 값을 채워준다.
```Go
func Scanln(a ...interface{}) (n int, err error)
```
* 마지막 입력값 이후 반드시 `enter` 키로 입력을 종료해야한다.
