# Radix 이해하기
 Golang의 redis client인 radix의 동작을 이해해본다.
 https://github.com/mediocregopher/radix

### Radix NewCluster() 동작 파악
1. cluster를 생성할때 host 정보와 함께 실행할 cluster operation을 받는다.
2. 기본적으로 실행되어야 하는 default operation을 실행하고, 인자로 받은 operation을 실행한다.
3. default operation : default pool 생성 함수 지정, cluster sync 주기 설정, cluster down state 기준 설정
