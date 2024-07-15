# BESTful
| CLI를 활용한 배달의 민족 어플리케이션 <br />
| Java만 사용하여(Spring 사용 X) MVC를 분리하여 구현
- 기간 2024.07.10 ~ 2024.07.15

### 입출력 흐름 설계
회원가입부터 주문 완료까지 전반적인 서비스의 입출력 흐름을 아래와 같이 설계함
<img width="632" alt="BESTfull_입출력흐름설계" src="https://github.com/user-attachments/assets/e6c2ba51-dde8-428c-8846-dc9a99a7004f">




### 패키지 구조 설계
MVC를 도메인 단위로 분리함
- M: 비즈니스로직, DB,기타 연산
- V: 콘솔 출력, 콘솔 입력
- C: view와 모델을 가지고 결과를 도출하는 로직이 있는 메소드들의 모임
```
📦src
 ┣ 📂exception
 ┃ ┣ 📜ExceptionHandler.java
 ┃ ┣ 📜InvalidInputException.java
 ┃ ┗ 📜MenuNotFoundException.java
 ┣ 📂function
 ┃ ┣ 📜MainFunction.java
 ┃ ┣ 📜OrderFunction.java
 ┃ ┣ 📜StoreFunction.java
 ┃ ┗ 📜UserFunction.java
 ┣ 📂main
 ┃ ┣ 📂view
 ┃ ┃ ┗ 📜MainView.java
 ┃ ┗ 📜MainController.java
 ┣ 📂order
 ┃ ┣ 📂model
 ┃ ┃ ┣ 📜Cart.java
 ┃ ┃ ┣ 📜CartService.java
 ┃ ┃ ┣ 📜Order.java
 ┃ ┃ ┣ 📜OrderDAO.java
 ┃ ┃ ┣ 📜OrderMenu.java
 ┃ ┃ ┗ 📜OrderService.java
 ┃ ┣ 📜OrderController.java
 ┃ ┗ 📜OrderView.java
 ┣ 📂store
 ┃ ┣ 📂model
 ┃ ┃ ┣ 📜DishInfo.java
 ┃ ┃ ┣ 📜Menu.java
 ┃ ┃ ┣ 📜MenuGM.java
 ┃ ┃ ┣ 📜Store.java
 ┃ ┃ ┣ 📜StoreDB.java
 ┃ ┃ ┣ 📜StoreModel.java
 ┃ ┃ ┗ 📜StoreOrderDTO.java
 ┃ ┣ 📜StoreController.java
 ┃ ┗ 📜StoreView.java
 ┣ 📂user
 ┃ ┣ 📂entity
 ┃ ┃ ┣ 📜User.java
 ┃ ┃ ┗ 📜UserDAO.java
 ┃ ┣ 📂service
 ┃ ┃ ┗ 📜UserService.java
 ┃ ┣ 📜UserController.java
 ┃ ┗ 📜UserView.java
 ┣ 📜Application.java
 ┣ 📜Main.java
 ┗ 📜OrderManager.java
```



### 팀 소개
<table>
  <tbody>
    <tr>
        <td align="center"><a href="https://github.com/ymkdev"><b>강경민</b></td>
        <td align="center"><a href="https://github.com/do-yoongyo2"><b>고유민</b></td>
        <td align="center"><a href="https://github.com/ijustwannabeme"><b>김경륜</b></td>
        <td align="center"><a href="https://github.com/wlsdk9803"><b>김윤경</b></td>
        <td align="center"><a href="https://github.com/Onek-2"><b>박경진</b></td>
        <td align="center"><a href="https://github.com/Onek-2"><b>정원우</b></td>
    </tr>
    <tr>
      <td align="center"><img width = "150px" src="https://avatars.githubusercontent.com/u/74167204?v=4" alt=""/><br /></td>
      <td align="center"><img width = "150px" src="https://avatars.githubusercontent.com/u/97513263?v=4" alt=""/><br /></td>
      <td align="center"><img width = "150px" src="https://avatars.githubusercontent.com/u/56223389?v=4" alt=""/><br /></td>
      <td align="center"><img width = "150px" src="https://avatars.githubusercontent.com/u/164445937?v=4" alt=""/><br /></td>
      <td align="center"><img width = "150px" src="https://avatars.githubusercontent.com/u/92127658?v=4" alt=""/><br /></td>
      <td align="center"><img width = "150px" src="https://avatars.githubusercontent.com/u/99272057?v=4" alt=""/><br /></td>
    </tr>
  </tbody>
</table>
