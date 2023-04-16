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
