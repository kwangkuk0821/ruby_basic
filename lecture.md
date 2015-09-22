<a href="https://chrome.google.com/webstore/detail/vimeo-repeat-speed/noonakfaafcdaagngpjehilgegefdima?hl=ko" target="_blank">플레이어 속도 조절 구글 크롬용 플러그인</a>

#루비 기초

<iframe src="https://player.vimeo.com/video/139999174" width="80%" height="600" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

루비에 관해서는 다음 문서에서 확인할 수 있습니다. ->
<a href="https://www.ruby-lang.org/ko/about/" target="_blank">루비</a>

```
$ irb
```

위의 명령어로 ruby 를 테스트 할 수 있는 환경으로 돌입할 수 있습니다.

###화면에 출력해보기  

`puts` 라는 메소드를 통해서 문자를 출력할 수 있습니다.

```ruby
puts "Hello World"
```

Hello World 라는 문자열을 화면에 찍어봅시다.

###<a href="https://ko.wikipedia.org/wiki/%EB%B3%80%EC%88%98" target="_blank">변수</a>에 값을 담아보기

<iframe src="https://player.vimeo.com/video/140000238" width="80%" height="600" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

자신이 정한 특정한 변수에 값을 저장하는 방법을 배워봅니다.  
유의사항 : 변수는 대문자와 소문자를 구분합니다. (변수는 반드시 소문자로 시작해야합니다)

```ruby
one  = 1
two  = 2
sum = one + two
puts sum
```

one 변수에는 **1** 라는 값을 저장했고, two 변수에는 **2** 라는 값을 저장했습니다.  
그리고 sum 변수에 one 과 two 를 더한 값을 저장합니다.  
1(one) + 2(two) = 3(sum) 이므로 화면에는 3 이 출력되게됩니다.

###<a href="https://ko.wikipedia.org/wiki/%EC%98%88%EC%95%BD%EC%96%B4" target="_blank">예약어</a>는 사용할 수 없습니다.
프로그래밍 언어 상에서 미리 정해놓은 예약어는 변수로 사용할 수 없습니다. [참고 리스트](http://www.rubymagic.org/posts/ruby-and-rails-reserved-words)

```ruby
end = 1
do = 1
if = 1
else = 1
```

위와 같이 end, do, if, else 는 전부 예약어이므로 사용 시 에러가 발생합니다.  
변수 이름을 정할 때 유의하도록 합시다.

###입력을 받아봅시다.

<iframe src="https://player.vimeo.com/video/140002448" width="80%" height="600" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

사용자(입력을 하는 자)에게 입력을 받고 이를 출력해보는 간단한 코드를 작성하겠습니다.

```ruby
print "input your name "
name = gets.chomp
print "aha! your name is "
puts name
```

`print` 는 puts 와 같이 화면에 글자를 표현하지만, 줄바꿈을 하지 않습니다.  
`gets.chomp` 로 입력을 받을 수 있고, 입력받은 문자열을 name 이라는 변수에 저장합니다.   (chomp 메소드를 사용하지 않을 경우 엔터까지 포함한 `name\n`을 입력받게 됩니다.)
그 후 `puts` 를 이용해서 name 을 출력하면 완성됩니다.

###<a href="https://ko.wikipedia.org/wiki/%EC%A1%B0%EA%B1%B4%EB%AC%B8" target="_blank">조건문</a>을 배워봅시다.

<iframe src="https://player.vimeo.com/video/140003078" width="80%" height="600" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

조건문이란 해당되는 조건이 참인지 거짓인지에 따라서 각각 다른 코드를 실행하게 만들 수 있습니다.  
입력과 출력 그리고 조건문을 활용하여 예제를 하나 만들어 보도록 합니다.  
조건문 형식은 다음과 같습니다.  

`if`(조건)  
`elsif`(추가 조건)  
`else`(어떤 조건에도 해당되지 않는 나머지 것)  
`end`(if 문 종료(필수적으로 있어야함))  
`if` 와 `end` 는 한 번씩만 사용할 수 있으며,  elsif 로 조건을 계속해서 추가시킬 수 있습니다.

```ruby
print "input your gender(성별) "
gender = gets.chomp
if gender = "male"
  puts "aha! you are male. right?"
elsif gender == "female"
  puts "aha! you are female. right?"
else
  puts "please right gender(male or female)"
end
```

성별을 입력받고 male 일 경우에는 `puts "aha! you are male. right?"`라는 코드를 실행시킵니다.  
만약 그렇지 않은 경우에는 `elsif` 를 통해서 female 인지 검사를 합니다.  
female 이 맞을 경우에는 마찬가지로 `puts "aha! you are female. right?"` 라는 코드를 실행시킵니다.  
이것도 그렇지 않은 경우에는 더이상 `elsif` 가 없으므로 `else` 로 이동.  
`puts "please right gender(male or female)"` 라는 코드를 실행시킵니다.

###배열(Array)에 대해서 배워봅시다.

<iframe src="https://player.vimeo.com/video/140004384" width="80%" height="600" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

일반적인 변수에는 한 가지의 값을 저장시킬 수 있지만, 배열을 사용하면 여러 가지 값을 한 변수에 저장할 수 있습니다.

```ruby
numbers = [1,2,3,4,5]
fruit = ["banana", "apple", "watermelon"]
numberAndFruit = [1,"banana","apple",4]
puts fruit
puts fruit[0]
puts fruit[1]
puts fruit[2]
puts fruit[3]
```

`배열명 = [값, 값, 값]` 와 같은 형식으로 값을 저장합니다.  
배열에는 다양한 타입의 값들을 저장할 수 있습니다.(물론, 배열 안에 배열도 저장 가능합니다.)  
`numberAndFruit` 변수와 같이 문자열과 숫자를 한 배열 안에 저장할 수도 있습니다.  
`fruit[0] -> fruit 배열에서 0 번째 == "banana"` 와 같이 위치(index)로 접근할 수 있습니다.  
위치(index)는 1이 아닌 0 부터 셈을 하며, `fruit[3]` 과 같이 배열에 저장된 범위(**fruit 변수의 배열에는 3개가 저장되어 있음으로 fruit[2] 가 배열의 마지막이다.**)를 넘어선 것은 nil(정의되지 않음) 값으로 출력하게 됩니다.

유용한 메소드도 있습니다.

```ruby
fruit = ["banana", "apple", "watermelon"]
puts fruit.sample
```

`sample` 메소드는 배열에서 임의의 한 요소를 뽑아 냅니다. <a href="http://ruby-doc.org/core-2.2.0/Array.html" target="_blank">배열에 관한 레퍼런스</a>

###반복문을 배워봅시다.

<iframe src="https://player.vimeo.com/video/140007790" width="80%" height="600" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

반복문은 반복되는 작업을 쉽게 하기 위한 프로그래밍 문법입니다.  
반복문의 종류는 많지만 몇 가지만 배워도록 합니다.

```ruby
10.times do |i|
  puts "#{i} Hello, World!"
end

arr = ["배터리", "비행기", "자동차"]

arr.each do |x|
  puts x
end

arr.each_with_index do |x, index|
  puts "#{index + 1}. 너는 전생에 #{x} 였을 수 있어"
end
```

`times` 메소드의 경우에는 단순 반복을 의미합니다. `|i|` 는 `i` 라는 임시 변수를 만들고 그 안에 현재 반복 중인 횟수를 저장하도록 만듭니다. 실행해보면 "0 Hello World" 부터 "9 Hello World"까지 순서대로 출력되게 됩니다.  
`arr.each` 메소드는 `arr` 변수 안의 요소들을 하나하나 가져오는 반복문입니다. 배열의 길이(저장된 갯수)만큼 반복합니다. `arr`의 각 요소는 임시 변수 `x`에 저장하여 화면에 출력하게 됩니다.
`arr.each_with_index`의 `|x, index|` (임시 변수)에서 `x` 에는 `arr`에 저장되어 있는 배터리, 비행기, 자동차 와 같은 값들이 순차대로 들어가게 되며, `index` 에는 `x` 값의 배열의 위치(index 값)이 담기게 됩니다.(배터리는 0, 비행기는 1, 자동차는 2)  
`x` 와 `index` 는 임의로 정해놓은 이름이며, 얼마든지 바꿀 수 있습니다.(마찬가지로 예약어 제외)

```ruby
loop do
  puts "0 to exit"
  cmd = gets.chomp
  break if cmd == "0"
end
```

`loop` 구문은 `do ... end` 블록 사이의 코드를 무한히 반복합니다. `break` 메소드는 반복문을 깨고 나올 수 있는 메소드 입니다. 루비에서는 위 코드에서 처럼 간단한 명령어 뒤에 조건문을 바로 쓸 수 있습니다. (영어로 말하듯 프로그래밍 언어를 구현해놓았습니다.)

###해쉬(Hash)에 대해 배워봅시다.

<iframe src="https://player.vimeo.com/video/140008096" width="80%" height="600" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

해쉬는 배열과 유사한 형태의 데이터형입니다. `키: 밸류`의 쌍으로 이루어져 있습니다. 우리가 흔히 아는 사전과 같다고 생각하시면 됩니다.

```ruby
student = {
  name: "Lic",
  age: 21,
  college: "seoul"
}
puts student
puts student[:name]
puts student[:age]
puts student[:college]
```

배열은 내장되어 있는 값들에 대해서 위치(index)로 접근하지만, 해쉬의 경우에는 키워드를 통해서 접근(사전 찾기)할 수 있습니다.  
위 예제에서 student 해쉬에는 name, age, college 라는 키워드로 각각 값들이 저장되어 있습니다.  
`student[:name]` 과 같이 `해쉬변수[:키워드]` 로 값들에 접근할 수 있으며, `student[:name]` 은 Lic 을 출력하게 됩니다.

###배열 안의 해쉬

<iframe src="https://player.vimeo.com/video/140008761" width="80%" height="600" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

지금까지 배웠던 것의 응용편입니다.

```ruby
students = [{name: "Lisa", age: 20},
            {name: "Brad", age: 20},
            {name: "Joy", age: 60}]

students.each do |u|
  puts u[:name]
end
```

students 는 배열이지만, 안에 들어있는 값들은 해쉬입니다.  
`each` 는 `each_with_index`의 기본형이라고 생각하시면 됩니다. `each_with_index` 처럼 index 값을 임시 변수에 담지 않습니다.  
먼저 `each` 메소드를 통해서 배열을 순차적으로 반복하고, `u` 라는 변수에는 배열 안의 해쉬들이 순차적으로 담깁니다.  
`u`는 해쉬값이기 때문에 name 을 출력하고 싶다면 `u[:name]` 으로 이름을 출력해야 합니다.

###수업 중 과제!

지금까지 배운 것들을 이용해서 전화번호부를 만들어봅니다.

- 조건
 - 사용자로부터 이름(name)과 전화번호(phoneNumber) 그리고 성별(gender)을 입력받고, 이를 저장시킵니다.
 - 성별의 경우에는 male 과 female 만을 입력받을 수 있으며, 다른 것을 입력받았을 경우에는 male 로 저장하도록 합니다. 
 - 입력이 완료되면 매번 전체 전화번호의 목록을 출력하도록 합니다.
