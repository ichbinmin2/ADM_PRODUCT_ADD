
<h1 align="middle">2022 원티드 프리온보딩 프론트엔드 코스 기업과제 - 설로인</h1>
<p align="middle">⚡️ React를 기반으로 구현한 커머스 노출 상품 등록 어드민 페이지</p>
<p align="middle">
<img width="1656" alt="image" src="https://user-images.githubusercontent.com/53133662/177025012-8f3db8cc-32c6-429d-b01a-7b43289a03ea.png">
</p>

<br />


## 🔎 프로젝트 소개 ( [Demo](https://brave-visvesvaraya-053de0.netlify.app/) )

**설로인에 노출되는 상품 등록/수정 어드민 페이지를 구현했습니다.**

커머스에 노출되는 상품의 신규 등록/수정이 가능한 상품 등록 어드민 페이지 프로젝트입니다. 제가 맡은 정보고시 form 섹션은 form 내부에서 각각의 input 값을 하나의 form 객체로 생성하여 처리할 수 있도록 하였고, 옵션 추가를 통해 유저가 자유롭게 form 안에서 새로운 옵션을 추가하고 데이터를 관리할 수 있도록 구현했습니다. 실시간으로 각 정보고시 form 마다 입력한 값들을 배열의 객체 값으로 관리하고 각 form을 카운트 하여, 백에서 최대한 처리하기 좋은 데이터 형태로 처리해주었습니다. 

<br />

## 📚 기술 스택

| React.js  |  Styled-Components   | 
| :--------:| :-----: |
|  <img src="https://user-images.githubusercontent.com/21965795/176630651-1248191d-432c-45ac-b876-9e5ff54e36f9.png" width="100px" > |<img src="https://user-images.githubusercontent.com/21965795/176630662-2d123d45-d642-409b-b448-503a0d9810d8.png"  width="100px"/>|

<br />

## 🧩 디렉터리 구조

```bash
src
├── App.css
├── App.js
├── components
│   ├── buyerRecommend
│   │   └── BuyerRecommend.jsx
│   ├── common
│   │   ├── Button.jsx
│   │   ├── Input.jsx
│   │   ├── InsertImage.jsx
│   │   ├── InsertImagePreview.jsx
│   │   ├── Radio.jsx
│   │   ├── Toggle.jsx
│   │   ├── datepicker
│   │   │   ├── DateRange.jsx
│   │   │   └── SingleDate.jsx
│   │   └── index.js
│   ├── infoNotice
│   │   ├── InfoNotice.jsx
│   │   └── infoNoticeForm
│   │       └── InfoNoticeForm.jsx
│   ├── layout
│   │   ├── Contentwrap.jsx
│   │   ├── navbar
│   │   │   └── Navbar.jsx
│   │   └── sidebar
│   │       ├── Sidebar.jsx
│   │       ├── SidebarData.js
│   │       └── SubMenu.jsx
│   ├── productExpoSalesPeriod
│   │   ├── ExposurePeriodSet.jsx
│   │   └── SalesPeriodSet.jsx
│   ├── productInfo
│   │   ├── Category.jsx
│   │   ├── CategoryObject.js
│   │   └── ProductInfo.jsx
│   ├── productInfoImage
│   │   └── ProductInfoImage.jsx
│   ├── productOrderSet
│   │   ├── ProductOrderStart.jsx
│   │   └── ProductPickUp.jsx
│   ├── productPreOrderReservation
│   │   └── PreOrderReservetionSet.jsx
│   └── productoption
│       ├── Optionset.jsx
│       ├── Suboption.jsx
│       └── index.js
├── hooks
│   ├── SubmitForm.jsx
│   ├── useForm.js
│   └── validate.js
├── index.css
├── index.js
├── logo.svg
├── pages
│   ├── admin.jsx
│   └── adminSection
│       ├── ExpoSalesPeriodSet.jsx
│       ├── addoption.jsx
│       ├── buyerRecmmend.jsx
│       ├── pagesInfoNotice.jsx
│       ├── productInfo.jsx
│       ├── productInfoImg.jsx
│       └── productorder.jsx
└── style
    ├── globalstyle.js
    └── theme.js
```

<br />

## 📌 프로젝트 과정 및 이슈 처리를 담은 회고

[**프로젝트 회고 보러가기!**](https://velog.io/@ichbinmin2/원티드-프리온보딩-프론트엔드-과정-2차-과제-상품-등록-관리-페이지)

<br />

## ✅ 과제 주요 구현 내용

**상품소개 이미지, 구매자 추천 이미지 섹션, 상품 정보 고시(민지연)**

✓ 정보고시 form 의 갯수 count로 관리(default 값은 1)

✓ 정보고시 form 추가 기능, 추가 될 때마다 생성 순서 숫자 count +1

✓ 정보고시 form 삭제 기능, 삭제 될 때마다 생성 순서 숫자 count -1 

✓ [리팩토링 추가(update : 3/21)](https://velog.io/@ichbinmin2/원티드-프리온보딩-프론트엔드-과정-2차-과제-상품-등록-관리-페이지) : 정보고시 form 삭제 기능 고유한 id 값으로 컨트롤하여 form count 순서대로 배치할 수 있도록 구현

✓ form input의 title, placeholder 를 mock data로 관리 및 실시간 업데이트 기능 구현

✓ [항목 추가 버튼]을 누르면 [항목 옵션]이 추가되고 'title' 및 '내용' 입력 가능

✓ [항복 삭제 버튼]을 누르면 해당 [항목 옵션] 만 삭제 가능

✓ 정보고시 form 내 입력된 모든 값(항목추가옵션 포함)은 해당하는 form 데이터 형태로 실시간 업데이트 가능

✓ 공통 UI 컴포넌트 : Radio

- 사용하고자 하는 컴포넌트에 content, select, onChange를 받아 onChange로 event가 실행되면 select가 되도록 기능 

- '제한 없음'을 default값으로 지정하여 자동으로 select 값 유지

✓ 공통 UI 컴포넌트 : Toggle 

- boolean state 값을 받아 true, false로 state를 관리되도록 기능

</br>

<img width="1656" alt="image" src="https://user-images.githubusercontent.com/53133662/177025012-8f3db8cc-32c6-429d-b01a-7b43289a03ea.png">

```
[
	{
	"count":1,
	"id":0.17664733026533797,
	"name":""소고기 500g",
	"origin":"국산",
	"ranking":"1+++ 등급",
	"keep":"냉동 보관",
	"type":"포장육",
	"추가 항목":"추가 항목 사항",
	},
]
```

<br/>

## ✍🏻 추가 리팩토링 : [id 값으로 form 삭제/관리하기 (update : 3/21)](https://velog.io/@ichbinmin2/원티드-프리온보딩-프론트엔드-과정-2차-과제-상품-등록-관리-페이지)

#### ☑️ 이슈 확인 

정보고시 폼을 추가/삭제하는 기능을 구현하면서, 정보고시 폼 리스트에 `count` 값을 추가하여 폼의 갯수를 `count`로 관리하도록 해왔다. 그런데 정보고시 폼 삭제 기능에 약간의 문제가 있었다는 걸 깨달았다. 삭제 버튼을 클릭하여 삭제되는 폼이 해당 폼이 아니라 정보고시 리스트의 마지막 순서의 폼이 삭제되었기 때문이다.

#### InfoNotice.jsx

```js
  const [count, setCount] = useState(2);
  const [form, setForm] = useState([{ count: 1 }]);

  const addNotice = (newNotice) => {
    setCount((prev) => prev + 1);
    setForm((prev) => [...prev, { ...newNotice, count }]);
  };

  const delNotice = () => {
    if (count <= 1) return;
    setCount((prev) => prev - 1);
    setForm((prev) => prev.slice(0, prev.length - 1));
  };

  return (
    <InfoContainer>
      {form.map((notice) => (
        <InfoNoticeForm
          key={notice.count}
          count={notice.count}
          notice={notice}
          delNotice={delNotice}
...

```

`count` 로 갯수를 관리하면서 정보고시 폼 리스트의 배열을 `slice(0, prev.length - 1)` 로 가장 마지막 순서만 삭제하다보니 내가 선택해서 삭제하려고 했던 form을 삭제할 수 없었다.

#### ☑️ 어떻게 해결했을까?

특정한 폼을 삭제하기 위해서는 정보고시 폼 마다 고유한 `id` 값이 필요했다. 현재는 `count`로 관리해주고 있었지만, 고유한 `id` 값을 추가해서 `id`를 기반으로 폼 리스트를 필터링해주려고 했다. 이제 `form`의 상태(state) 초기값에 `id` 값을 지정하고, 정보고시 폼이 추가될 때에도 마찬가지로 `Math.random()`을 이용하여`id` 값이 자동으로 생성될 수 있도록 했다.

#### InfoNotice.jsx

```js
const [form, setForm] = useState([{ count: 1, id: 1 }]);

  const addNotice = (newNotice) => {
    setCount((prev) => prev + 1);
    setForm((prev) => [...prev, { ...newNotice, count, id: Math.random() }]);
  };

```

먼저 삭제 버튼의 `onClick` 이벤트로 특정 `form`의 데이터를 받아와야 했기 때문에 `form`을 매핑할 때 `InfoNoticeForm` 컴포넌트에 prop으로 전달했던 `delNotice()` 함수에 해당 `form`을 인자로 전달해주었다.


```js
  const delNotice = (targetItem) => {
    if (count <= 1) return;
    setCount((prev) => prev - 1);
    setForm((prev) => prev.slice(0, prev.length - 1));
  }
  
  return (
    <InfoContainer>
      {form.map((notice) => (
        <InfoNoticeForm
          key={notice.count}
          count={notice.count}
          notice={notice}
          delNotice={() => delNotice(notice)}
...
```
#### InfoNoticeForm.jsx

```js
const InfoNoticeForm = ({ count, notice, setNotice, delNotice }) => {
  ...
  return (
    <Button 
		...
    	onClick={() => {
    		delNotice();
  		}} 
	/>
};
```

`delNotice()` 의 인자로 받아온 `targetItem`(form) 의 `id` 값과 기존의 폼 내부의 `id` 값과 비교하여 `targetItem`의 `id` 값이 form 의`id` 값과 다른 form(삭제 버튼으로 선택하지 않은 폼)만 남길 수 있도록 `filter()` 메소드로 필터링해주었다.


```js
  const delNotice = (targetItem) => {
    if (count <= 1) return;
    setCount((prev) => prev - 1);

    setForm((prev) => {
      const filteredList = prev.filter(
        (formItem) => formItem.id !== targetItem.id
      );

      return filteredList.map((item, index) => {
        return { ...item, count: index + 1 };
      });
    });
  }

```


그리고 필터링 된 배열을 매핑하여 스프레드 연산자로 기존의 form 객체들을 그대로 받아오고, `count`를 index 값에 1을 더하는 방식으로 `count`를 새롭게 카운팅 해주었다. 여기까지 로직 상에는 크게 문제는 없어보였는데 라이브 서버로 확인해보았을 때 원하는 폼을 삭제하려고 해도 다른 폼이 삭제되는 이슈가 지속해서 발생했다. console로 남은 form을 출력해보면서 분명 삭제를 누른 폼의 데이터가 삭제 되었음을 확인했지만, UI상에서는 해당 폼이 삭제가 되는 것처럼 보여지지 않았던 것이다.

```js
return (
    <InfoContainer>
      {form.map((notice) => (
        <InfoNoticeForm
          key={notice.count}
          count={notice.count}
          notice={notice}
          delNotice={() => delNotice(notice)}
...
```

다시 코드를 천천히 살펴보니 아주 간단한 부분에서 문제가 있었음을 깨달았다. 바로 `form`을 매핑하여 `InfoNoticeForm` 컴포넌트에 prop으로 데이터를 넘길 때 `key`를 `notice.count`로 넘겨주고 있었던 것이다.


```js
return (
    <InfoContainer>
      {form.map((notice) => (
        <InfoNoticeForm
          key={notice.id}
          count={notice.count}
          notice={notice}
          delNotice={() => delNotice(notice)}
...
```

`key={notice.count}`을 `key={notice.id}`로 변경하고 나서야 원하는 form이 데이터 뿐만 아니라, UI 상으로도 정상적으로 삭제가 되는 것을 확인할 수 있었다. 또한 중간에 위치한 form을 삭제할 때마다 `count`도 삭제된 폼을 제외하고 재 카운팅되었다. 

> React는 `key`를 통해서 현재 배열의 길이를 비롯하여 이미 렌더링한 아이템의 갯수를 확인할 수 있고 동시에 아이템의 '위치'까지 고려하게 된다. 그런데 React가 개별 아이템을 식별할 수 있도록 해주는 바로 이 `key` 값을 `count`로 설정을 해주었기 때문에, 해당 form을 삭제 해도 `key` 값은 교체가 되지 않아 이러한 문제가 발생했던 것이다. 초반에 `key`의 문제라고 생각하지 못하고 여러번 로직을 수정했는데.. 꽤나 허탈한 감이 있다. 앞으로는 아무리 간단한 로직이라도, 기본을 지키고 있는지 체크하면서 코드를 좀더 면밀하게 살펴보며 코드를 작성해야 겠다는 생각이 든다. 


<br/>

## 👯‍♀️ 팀 Repo 링크 가기

["On-Basic" Repo 바로가기](https://github.com/On-Basic/ADM_PRODUCT_ADD)

<br/>

## 🖥 설치 및 시작하는 법

**프로젝트 클론**

```
$ git clone https://github.com/On-Basic/ADM_PRODUCT_ADD.git
```

**패키지 설치**

```
$ yarn
```

**서버 실행**

```
$ yarn start
```
