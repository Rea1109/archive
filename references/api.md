## API (rest / graphql)
---
> 응용프로그램과 대화하는 방법
> HTTP 요청을 받은 Back-end 에서 실행되는 기능   
>Back-end 로부터 받은 리턴 받은 값은 <b style='color:#03a9f4;'>JSON</b> 형식으로 옴

- Rest Api
  - url 형식으로 되어있음
    - `https://naver.com/board/`
    - `https://naver.com/profile/철수`
  - back-end에서 보내주는 모든 데이터를 받음
  - 대표적인 통신 라이브러리
    - <b style='color:#03a9f4;'>Ajax</b>
    - <b style='color:#03a9f4;'>axios</b>

- Graphql Api
  - 일반 함수와 같은 형식
    - `board(1)`
    - `profile('john')`
  - 필요한 데이터만 골라 받을 수 있음
  - 통신 라이브러리
    - <b style='color:#03a9f4;'>apollo-client</b>

- CRUD 분류
    | API CRUD | <b style='color:#03a9f4;'>axios</b> | <b style='color:#e91e63;'>apollo-client</b> |
    | :--- | :---: | :---: |
    | Create | <b style='color:#03a9f4;'>post</b> | <b style='color:#e91e63;'>mutation</b> |
    | Update | <b style='color:#03a9f4;'>put</b> | <b style='color:#e91e63;'>mutation</b> |
    | Delete | <b style='color:#03a9f4;'>delete</b> | <b style='color:#e91e63;'>mutation</b> |
    | Read   | <b style='color:#03a9f4;'>get</b> | <b style='color:#e91e63;'>query</b> |

- example
    ```jsx
    import axios from 'axios'

    const result = axios.post('API url')
    const result = axios.put('API url')
    const result = axios.delete('API url')
    const result = axios.get('API url')
    ```
    ```jsx
    import { useMutation , useQuery } from '@apollo/client'

    const result = useMutation('graphql') 
    const result = useQuery('graphql')
    ```