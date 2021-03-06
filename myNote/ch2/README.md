# 2. 스파크의 파이썬 셸과 스칼라 셸 소개

스파크에서는 연산 과정을 클러스터 전체에 걸쳐 자동으로 병렬화해 분산 배치된 연산 작업들의 모음으로 표현한다. 이를 RDD라고 부른다.

스파크는 클러스터에서 다양한 **병렬** 연산을 수행하는 **드라이버 프로그램**으로 구성된다.

RDD 는 SparkContext를 통해 만들 수 있다. **드라이퍼 프로그램은** SparkContext을 통해 스파크에 접속한다. 드라이버 프로그램은 애플리케이션의 main 함수를 갖고있으며 클러스터 분산 데이터세트를 정의하고 연산작업을 수행한다.

한 애플리케이션이 스파크에 연동되려면 SparkContext 객체가 필요하다. SparkConf 객체를 만들어서 설정 후 SC 생성이 가능하다.

SparkConf 객체를 만들 땐 클러스터 URL과 애플리케이션 이름이 필요하다. URL은 클러스터로 접속할 방식으로, 한 개의 스레드나 단일 로컬머신에서 돌 경우엔 "local"이라는 특수한 값으로 설정하여 따로 접속할 필요가 없음을 알린다. 이외의 설정은 나중에..

**=> create SparkConf -> initalize SparkContext with SparkConf -> create RDD**

스파크를 끝내기 위해서는 `SparkContext.stop()` 혹은 애플리케이션 종료

