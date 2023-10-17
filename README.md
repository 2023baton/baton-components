## description

바톤 서비스 구현에 사용된 common 컴포넌트 라이브러리

## version

version: 1.0.0 (updated in 2023.10.17)

## 사용법

### 설치

```Shell
npm i baton-components
```

## Dropdown

### 컴포넌트 삽입

```JavaScript
import { Dropdown } from 'baton-components';
```

## Prop

### Container

| props          | 타입            | 설명                                                  |
| -------------- | --------------- | ----------------------------------------------------- |
| children       | React.ReactNode | Dropdown을 열었을 때 trigger 하위에 그려지는 컴포넌트 |
| trigger        | React.ReactNode | Dropdown을 열기 위한 trigger 컴포넌트                 |
| isDropdownOpen | boolean         | Dropdown열려있는지 확인하는 상태                      |
| gapFromTrigger | string          | children과 trigger사이의 간격                         |
| onClose        | () => void      | dropdown을 닫는 함수                                  |

<br/>

```JavaScript
function App() {
  const [isOpen, setIsOpen] = useState(false);

  return (
    <>
      <div>
        <Dropdown
          trigger={
            <button
              onClick={() => {
                setIsOpen(true);
              }}
            >
              드롭다운 열기
            </button>
          }
          isDropdownOpen={isOpen}
          onClose={() => {
            setIsOpen(false);
          }}
          gapFromTrigger="40px"
        >
          <div
            style={{ width: '100px', height: '100px', backgroundColor: 'red' }}
          >
            열린 모달
          </div>
        </Dropdown>
      </div>
    </>
  );
}
```

<br/>

## 배포 링크

- [npm](https://www.npmjs.com/package/baton-components)
