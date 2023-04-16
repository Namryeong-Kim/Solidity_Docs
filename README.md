# Solidity_Docs

## Getter function

- The [getter function](https://docs.soliditylang.org/en/v0.8.19/contracts.html#getter-functions) created by the `public` keyword is more complex in the case of a mapping.

## Gas

- each transaction is charged with a certain amount of **gas** that has to be paid for by the originator of the transaction (`tx.origin`)
- `gas price`는 `tx.origin`이 설정한 값으로, `gas_price * gas`를 선불로 지불해야 함

## Message Calls

- 컨트랙트는 message call을 통해 다른 컨트랙트를 호출하거나 컨트랙트가 아닌 계정으로 이더를 보낼 수 있음
- message call은 source, a target, data payload, ether, gas, return data가 있음(트랜잭션과 유사)

## Precompiled Contracts

- 1-8인 address는 `precompiled contracts`라고 부름
- 다른 컨트랙트와 동일하게 호출할 수 있지만 실행해야 하는 것은 해당 주소에 저장된 EVM 코드에 의해 정의되지 않고(코드가 포함되지 않음) EVM 실행 환경 자체에서 구현됨

## SPDX License Identifier

- 스마트 컨트랙트 소스 코드를 공개하는 것은 저작권 등의 법적 문제와 관련됨
- solidity compiler는 machine-readable한 SPDX license identifier를 사용하는 것을 권장함
- 이는 주석으로 시작해야 함
- 사용 예
    
    ```solidity
    // SPDX-License-Identifier: MIT
    ```
    

## Pragmas

- pragma는 특정 컴파일러 기능이나검사를 활성화하는데 사용됨
- pragma는 항상 로컬 소스 파일을 지칭하므로, 전체 프로젝트에서 pragma를 활성화하기 위해서는 모든 소스 파일에 추가해줘야 함
- 다른 파일을 가져왔을 때 자동적으로 추가되지 않음
- 사용 예
    
    ```solidity
    pragma solidity ^0.5.2;
    ```
    

## ****Importing other Source Files****

### Syntax and Semantics

- import는 지원하지만 export는 지원하지 않음
- 사용 예
    
    ```solidity
    import "[import_path]";
    
    //global symbol로 받기
    import * as symbolName from "filename";
    import "filename" as symbolName;
    
    //naming collisiion 발생 시, importing하는 동안 rename할 수 있음
    import {symbol1 as alias, symbol2} from "filename";
    ```
    

## Comments

- 사용 예
    
    ```solidity
    //single line
    // ...
    
    //multi line
    /* ... */
    
    //NatSpec comment(multi line) -> 함수 선언 또는 statements 바로 위에 작성해야 함
    /// ... 
    /** ... */
    ```
