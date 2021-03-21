### GraphQL 풀스택 웹 개발입문(Django + React/Apollo Client)
[강의 링크](https://www.udemy.com/course/graphql-web-django-reactapollo-client/) (Udemy 일본어 강좌)
1. 강의 소개
    - GraphQL을 Django(graphene-django)로 서버를, React Hooks/Apollo Client로 프론트엔드를 구현하며 배우는 강의
    - GraphQL의 기초를 배우고 직원관리 페이지를 실제로 구현해보면서 GraphQL의 자세한 동작과 서버-프론트 연계방식에 대해 배우게 됨
2. 수강 기간 (21.03.21 ~)
3. 수강 목적
    - REST API와 다른점이 무엇인지, 왜 자주 쓰이는지에 대한 의구심을 해소하기 위해
    - GraphQL을 사용해 어떤 식으로 구현할 수 있는지 실습해보기 위해
4. 수료증 링크(추후 첨부)

**21.03.21 첫번째 챕터**
* [Query: GitHub API](https://docs.github.com/en/graphql/overview/explorer)를 통해 알아보는 GraphQL

![graphql-explorer01](https://user-images.githubusercontent.com/67398691/111897814-64a81880-8a65-11eb-933a-30d1990476aa.jpg)

(Figure 01: GitHub GraphQL API를 사용한 GraphQL의 사용 예제)

![graphql-explorer02 jpg](https://user-images.githubusercontent.com/67398691/111897818-6d005380-8a65-11eb-97e2-c698cf887e03.png)
![graphql-explorer03](https://user-images.githubusercontent.com/67398691/111897819-6eca1700-8a65-11eb-9cf9-2e87043e971d.png)

(Figure 02 & 03: 같은 변수로 데이터를 받아올 수 없으므로 별칭을 지정할 것)

**Fragment**: 쿼리의 일부분을 재활용 가능한 단위로 나눠놓은 것
* GraphQL에서는 쿼리를 타입스크립트의 인터페이스 처럼 지정하여 반복 사용이 가능하다

![graphql-explorer04](https://user-images.githubusercontent.com/67398691/111897822-74bff800-8a65-11eb-934e-0fb58f7553f1.png)

(Figure 04: GraphQL의 fragment 기능을 사용하여 쿼리를 재사용한 예시)

* 해당 모델이 특정 인수를 사용하여 데이터를 받아올 수 있도록 정의되어 있다면 인수를 해당 쿼리 뒤에 소괄호로 입력하여 사용할 수 있다

![graphql-explorer05](https://user-images.githubusercontent.com/67398691/111897826-7984ac00-8a65-11eb-9d8a-5e0f22e74763.png)

(Figure 05: GraphQL에서 특정 인수를 사용한 데이터 취득 예시)

* GraphQL은 Pagenation기능 또한 제공하고 있어 startcursor, endcursor등을 통해 first, last, before, after 등의 인수를 사용할 수도 있다

![graphql-explorer06](https://user-images.githubusercontent.com/67398691/111897830-80132380-8a65-11eb-9c64-c3d6f8ee2874.png)

(Figure 06: Pagenation 기능을 사용하여 특정 지점으로부터 데이터를 취득)

* 해당 인수를 때에 따라 바꿔 사용해야 한다면 쿼리문의 최상단에 **$인수명**을 선언함으로써 블록 내 어디서든 해당 변수를 사용할 수 있다

![graphql-explorer07](https://user-images.githubusercontent.com/67398691/111897834-86090480-8a65-11eb-8066-7259b9bc9064.png)

(Figure 07: 사용하고자 하는 인수를 블록내에서 사용할 수 있는 변수로 선언하는 방법)

* **Mutation**: 데이터를 조작(CRUD)하기 위한 쿼리문으로 뮤테이션은 병렬처리되지 않고 하나씩 처리된다

![graphql-explorer08](https://user-images.githubusercontent.com/67398691/111897839-8d301280-8a65-11eb-92d8-6d42200fa401.png)

(Figure 08: Mutation의 실행을 통해 해당 repository에 star를 추가한 모습)
