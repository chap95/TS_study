1. 
    1. `module`을 `es6/ASM/UMD` 등 `commonjs`가 아닌 옵션으로 변경한다.
    1. `moduleResolution`을 `classic`으로 설정한다.

1. 

컴파일러 실행시에 컴파일할 파일을 제시하면, config파일의 files 옵션이 무시됩니다. 이에 따라 아래와 같이 고쳐주면 됩니다.

`tsc`


3.
    1. `target` 옵션을 `es6` 혹은 그 이상으로 설정합니다.
    1. `lib`옵션에 `es6`혹은 그 이상의 라이브러리를 추가합니다.

4.
    1. `strictNullChecks`, 포함
    1. `strictPropertyInitialization`, 포함
    1. `noFallthroughCasesInSwitch`, 미포함
    1. `noImplicitThis`, 포함