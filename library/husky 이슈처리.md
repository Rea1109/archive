## husky 이슈처리

### ***npx eslint .***   명령어가 실행되지 않는 이슈
    
    ***npx eslint '**/*.{ts,tsx}'***  
    
    간혹  "."  키워드가 읽히지 않아 발생
    
    또는 코드에 문제가 없을경우 ***즉 eslint가 에러로 간주할 만한 코드가 없을 경우*** 해당 명령어로
    
    코드를 체크해도 아무런 반응이 없다. (강제로 에러코드를 작성하고 실행)
    
### package.json 에 git commit 전 ***hook 설정후 , 제대로 실행되지 않는 이슈***
    위에 이슈와 비슷하게 키워드가 읽히지 않는 경우

    package.json 파일에서 husky 설정부분에서 아래 코드 추가
    
```shell
    "lint-staged": {
        "**/*.{ts,tsx}": [
        "npx eslint **/*.{ts,tsx}"
        ]
    }
```