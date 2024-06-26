# 네트워크 종류와 구성을 알아보자

## 1. 클라이언트 서버형과 피어 투 피어형 - 장치를 연결하는 방식의 차이

    네트워크에는 다양한 장치가 연결됩니다. 장치를 연결하는 방법으로는 각 장치의 역할에 따라 클라이언트 - 서버형이나 피어 투 피어형 등이 있습니다.

### 클라이언트 - 서버형의 구조

- 미니컴퓨터나 워크스테이션(전문적인 작업이나 업무에 특화된 컴퓨터 시스템) 등이 발전하면서 함꼐 확산된 형태
- 한쪽에선 업무 애플리케이션이나 네트워크 애플리케이션 등을 실행하여 서비스 제공, 다른 컴퓨터(단말기)에선 네트워크를 통해 서비스를 받습니다.
  - 이때 서비스를 제공하는 쪽이 **서버**, 서비스를 받는(요청하는) 쪽을 클라이언트라고 합니다.
- 서버나 클라이언트 명칭은 장치 역할에 따라 붙음
  - ex) 워크스테이션이 역할에 따라 클라이언트 or 서버가 될 수 있다.

### 피어 투 피어형의 필요성

- TCP/IP 및 인터넷도 전 세계 미니컴퓨터 등을 연결하려고 고안된 프로토콜 및 기술입니다.
- 인터넷은 기본적으로 클라이언트-서버 형태로 사용하지만 인터넷에서도 실시간 동영상 전송, 고도화 및 맞춤형 통신 등으로 서버를 거치지 않고 단말기끼리 직접 통신하는 것이 효율적일 때가 있습니다.
- 인터넷에서는 IP 주소와 전용 통신 앱 등을 사용하여 LAN의 단말기끼리 직접 연결할 수 있습니다, 이런 방식을 피어 투 피어라고 합니다.
- 예시: 파일 공유 네트워크(BitTorrent), 가상 통화(Bitcoin), 스트리밍(BitTorrent Live), 파일 공유 애플리케이션(Shareit), 토렌트 클라이언트(µTorrent)

#### 클라이언트 - 서버형

| 구분       | 기능                                              | 설치 장소                                                    |
| ---------- | ------------------------------------------------- | ------------------------------------------------------------ |
| 서버       | 처리나 기능, 데이터 등 서비스를 제공하는 쪽       | LAN 안이나 밖, 인터넷 등으로 예상된다                        |
| 클라이언트 | 처리나 기능, 데이터 등 서비스를 받는(요청하는) 쪽 | 서비스를 받는 것은 모두 클라이언트로, 컴퓨터가 아니어도 된다 |

#### 중앙 집중형

네트워크 이용 형태와 관리 방식에 따라 중앙 집중형으로 분류하기도 합니다.
중앙집중형은 과거 컴퓨터 이용 형태를 기반으로 한 것으로 대형 컴퓨터(호스트 컴퓨터)에 전동 타자기 같은 단말기를 다수 연결하는 방식입니다. 중앙 호스트 컴퓨터가 모든 처리를 담당하고 CPU의 짧은 처리 시간을 순차적으로 할당하는 TSS(Time Sharing Service) 방식으로 처리를 수행

- 예시: 전통적인 클라이언트 - 서버 모델, 전통적인 은행 시스템, 전통적인 교육 시스템, 전통적인 데이터 센터, 전통적인 소프트웨어 배포 모델

- 현재: 클라우드 컴퓨팅 서비스, 온라인 금융 서비스, 소셜 미디어 플랫폼, 전통적인 기업 정보 시스템, 관리 시스템 및 엔터프라이즈 소프트웨어

- 반대는 분산형 시스템 or 탈중앙화 기술 : 블록체인

<hr/>

## 2. LAN - 제한된 범위의 네트워크

### 좁은 범위의 네트워크를 가리키는 LAN

- LAN(Local Area Network) 정의는 간단하지 않지만, 일반적으로 같은 건물 내부나 같은 층 등 제한된 범위의 네트워크를 의미합니다.
- 기업이나 대학 등 같은 부지 내에 복수의 건물이 있을 떄 이들을 하나의 LAN으로 관리하기도 합니다.
- 본사와 지사 등 지리적으로 떨어져 있는 거점을 중앙에서 관리하고자 하나의 LAN으로 구성하기도 합니다.

  - 이런 경우 특정 상황에 따라 효율적일 수 있다.

    - 적은 대역폭 요구: 지점 간의 데이터 교환이 매우 적고, 대역폭 요구가 낮은 경우엔 하나의 LAN으로 구성하여 비용을 절감하고 관리를 간소화할 수 있습니다.
    - 보안이 중요하지 않은 경우

  - 일반적으론 효율성이 떨어지기 떄문에 WAN(Wide Area Network)을 사용하여 연결하는 것이 더 효과적일 수 있습니다.

### LAN을 구성하는 장치와 프로토콜

현재 LAN을 구성하는 네트워크는 **이더넷**이 주류입니다.
이더넷에서는 트위스트 페어 케이블로 만든 LAN 케이블로 장치끼리 연결합니다. 각 장치를 연결할 때는 RJ-45라는 규격의 커넥터를 사용합니다.
이더넷에서는 연결 대상(컴퓨터, 서버, 프린터 등)을 식별하는데 MAC 주소를 이용합니다.
노드 식별자는 MAC 주소만으로 충분하지만, 실제로는 이더넷의 상위 계층 프로토콜, TCP/IP의 식별자인 IP주소도 이용합니다.
MAC 주소는 주소 값에 계층 구조가 없기 떄문에 부서마다 계층 구조를 갖는 일반적인 기업의 LAN구성이나 관리가 번거로워지므로 이더넷 프레임의 페이로드에 포함된 IP주소를 사용해서 네트워크를 구성하는 L3 스위치를 이용합니다.- L3 스위치는 MAC 주소 테이블이라는 내부적인 데이터베이스를 유지합니다. 이 테이블은 특정 포트로 들어오는 프레임의 송신자 MAC 주소를 기록하고, 목적지 MAC 주소에 대응하는 포트 정보를 저장합니다.

    cf. mac 주소는 주소 자체가 단일 값으로 구성되어 있다. 다른 주소의 일부 또는 하위 부분이 아니라는 의미.  예를 들어 IP 주소는 계층 구조를 가지며, 네트워크 부분과 호스트 부분으로 나뉘어 있습니다. 그러나 MAC 주소는 네트워크 계층에서 사용하는 IP 주소와는 달리 단일한 값으로만 표현됩니다.
    mac주소의 예) 00:1A:2B:3C:4D:5E
    각각 2자리의 16진수로 이루어진 6바이트(48비트)의 값,

###### MAC 주소에 계층구조가 없기 떄문에 LAN구성이나 관리가 번거로워지는 이유

1. 주소 할당 및 관리: MAC주소는 전세계적으로 고유해야함. 대규모 기업에서는 모든 네트워크 장비에 고유한 MAC주소를 할당 및 관리해야함. 부서나 지역이 늘어날 수록 MAC주소 고유성을 유지하기 위해 더욱 복잡한 할당 및 관리작업이 필요해진다.

2. 네트워크 구성의 변경 어려움: 부서나 지사를 추가 or 변경할 때, mac주소의 고유성을 유지하면서 네트워크 구성을 변경하는 것은 번거로운 과정. 새로운 장비를 추가 or 교체할 때마다 MAC 주소의 충돌을 방지하기 위해 주소를 일일이 관리해야함.

3. 보안 정책의 유지 어려움: 보안을 강화하고자 할 때 특정 MAC 주소를 허용하거나 차단하는 등의 정책을 적용하는 것이 어려울 수 있습니다. 특히, 계층 구조가 없어 개별적인 MAC 주소를 대상으로 하는 정책 설정이 복잡해집니다.

4. 네트워크 모니터링 및 문제 해결: 부서마다 계층 구조가 없는 경우, 네트워크에서 발생하는 문제를 식별하고 해결하기가 더 어려울 수 있습니다. 어떤 부서에서 문제가 발생했는지 정확히 파악하기 어려울 수 있습니다.

#### 구체적인 LAN의 실체

    LAN에 연결된 장치를 생각하면 컴퓨터와 서버는 LAN 케이블로 스위치와 연결됩니다.
    스위치는 LAN의 최소 단위를 구성합니다. 각 스위치는 L3 스위치나 라우터를 이용해서 과, 부, 사업소 등 조직 구성에 따라 묶습니다. 이것이 구체적인 LAN의 실체이며,
    L2 스위치로 묶인 LAN은 그대로는 다른 스위치로 묶인 LAN과 통신할 수 없습니다.

    이를 해결하기 위해 캐스캐이드 연결 or 모든 장치를 연결할 수 있는 스위치를 이용합니다.
    하지만 캐스케이드는 연결댓수제한이 있습니다. 또 사무실을 하나의 LAN으로 관리하는 것은 유지 보수가 번거롭고 보안상 무넺가 될 수 있습니다.
    --> L2 스위치를 묶어 다른 LAN 사이에서 교통을 정리하는 라우터 or L3 스위치를 도입해서 대응합니다.

<hr/>

## 3. 이더넷 - 오피스 내부를 연결하는 네트워크

### 이더넷의 기본 원리

    사무실이나 연구실의 장치를 연결하는 네트워크로 이더넷이 개발 되었습니다.
    다수의 장치가 독자적인 타이밍에 통신을 시작하는 것을 목표로 잡고 패킷 통신을 이용한 랜덤 액세스 방식을 채용했습니다.
    랜덤 액세스 방식은 전송 중일 때 다른 기기가 전송 중이면 조금 기다린 후 재전송을 시도하는 원리입니다.
    회선의 사용 상황을 탐지해서 재전송하는 방식을 CSMA/CD라고 합니다.
    재전송 대기 시간에 재전송 횟수를 고려한 난수를 이용해서 전송 재전송 충돌률을 낮추는 CSMA/CA 방식도 있습니다.

    개발 당시에는 태핑으로 각 기기를 연결하는 버스형 네트워크였지만 전송 속도가 100Mbps 이상이면 CSMA/CD 방식이 제대로 작동하지 않기 떄문에, 현재는 스위칭 허브를 이용하여 패킷 식별자로 목적지를 전환하는 스타형 네트워크로 구성하고 있습니다

###### 전송속도에 따른 CSMA/CD

    CSMA/CD는 이더넷과 같은 통신프로토콜에 사용되는 충돌 감지 기반의 접근 방식!!!(네트워크에서 여러 장치가 동시에 데이터를 전송하지 않도록 하기위함)

    전송 속도가 100Mbps 이상이면 제대로 작동 하지 않는 이유는

    1. 충돌 감지 시간의 한계: CSMA/CD는 충돌이 발생했을 때 이를 감지하고, 충돌이 발생한 모든 장치에게 경고를 보내는 시간을 고려합니다. 이 시간은 데이터의 전파 시간과 충돌을 감지하는 시간으로 구성되며, 높은 전송 속도에서는 이 시간이 매우 짧아집니다. 따라서 100Mbps 이상의 높은 속도에서는 충돌을 감지하고 효과적으로 처리하는 것이 어려워집니다.

    2. 데이터 전파 시간의 증가: 데이터 전송 속도가 높아질수록 데이터가 전파되는 시간도 감소합니다. 따라서 충돌이 발생했을 때 이를 빠르게 감지하고 적절한 조치를 취하는 것이 더 어려워집니다.

    3. 이더넷 프레임 최소 크기의 영향: 이더넷은 최소 프레임 크기가 정해져 있습니다. 전송 속도가 높아질수록 최소 프레임 크기에 해당하는 비트 수가 많아지므로 충돌이 더 오랜 시간 동안 계속될 가능성이 있습니다.

    대신 이러한 높은 속도에선 전이중(Full Duplex) 통신이 더 효과적으로 사용됩니다.
    전이중 통신(전화처럼 송신과 수신이 동시에 되는 통신 방식)에서는 송신과 수신이 별도로 경로를 사용하므로 충돌이 발생하지 않습니다.

### 이더넷 프레임의 구조

    이더넷 프레임은 이더넷으로 주고받는 데이터 덩어리(TCP/IP에서 패킷이라고 불리는 것과 같다)이고, 5가지 필드로 나눌 수 있습니다.
    1. 패킷의 출발지 식별자 정보
    2. 목적지 식별자 정보
    3. 패킷 종류나 페이로드 프로토콜 정보(타입 필드)
    4. 페이로드
    5. 체크섬
    이더넷 식별자는 MAC 주소를 이용합니다 앞서 말하 스위칭 허브는 이 MAC주소를 참조해서 어느 포트와 어느 포트를 연결하면 좋을지 판단합니다.

##### 패킷의 종류

    1. 이더넷 프레임 (Ethernet Frame): 이더넷 네트워크에서 사용되는 데이터 전송 단위입니다. 프레임은 목적지 및 출발지 MAC 주소, 타입 필드, 페이로드(데이터), 오류 검사 등의 필드로 구성됩니다.

    2. IP 패킷 (IP Packet): 인터넷 프로토콜(IP)에서 사용되는 패킷으로, 송신자와 수신자의 IP 주소, 프로토콜 정보, 페이로드(데이터) 등을 포함합니다.

    3. TCP 세그먼트 (TCP Segment): 전송 제어 프로토콜(TCP)에서 사용되는 패킷으로, 송신자와 수신자의 포트 번호, 일련 번호 및 확인 응답 번호, 제어 플래그, 페이로드(데이터) 등을 포함합니다.

    4. UDP 데이터그램 (UDP Datagram): 사용자 데이터그램 프로토콜(UDP)에서 사용되는 패킷으로, 송신자와 수신자의 포트 번호, 길이 정보, 체크섬, 페이로드(데이터) 등을 포함합니다.

    5. ICMP 메시지 (ICMP Message): 인터넷 제어 메시지 프로토콜(ICMP)에서 사용되는 패킷으로, 네트워크에서 발생하는 에러 메시지나 제어 메시지를 전달하는 데 사용됩니다.

    6. ARP 프레임 (ARP Frame): 주소 해결 프로토콜(ARP)에서 사용되는 패킷으로, 논리적인 IP 주소를 물리적인 MAC 주소로 매핑하는 데 사용됩니다.

    7. DNS 패킷 (DNS Packet): 도메인 이름 시스템(DNS)에서 사용되는 패킷으로, 도메인 이름과 IP 주소 간의 매핑 정보를 전송하는 데 사용됩니다.

    8. HTTP 요청 및 응답 메시지: 하이퍼텍스트 전송 프로토콜(HTTP)에서 사용되는 패킷으로, 웹 서버 및 클라이언트 간의 통신을 처리합니다.

    9. DHCP 메시지 (DHCP Message): 다이내믹 호스트 구성 프로토콜(DHCP)에서 사용되는 패킷으로, 네트워크 장치가 IP 주소 및 기타 네트워크 설정을 동적으로 얻는 데 사용됩니다.

#### 용어 노트

- 태핑: 동축 케이블 외피에 금속침으로 구멍을 내서 중심선에 직접 연결하는 방법이다.
- 체크섬: 전송 오류를 찾아내는 부호다. 원본 데이터에서 얻은 계산 값과 수신한 데이터의 계산 값을 비교했을 때 서로 일치하지 않으면 올바르게 전송되지 않은 것으로 판단한다.

- 버스형 네트워크: 임의의 버스(모선) 위치에 연결장치(스테이션)를 설치할 수 있고, 동시에 복수의 장치에 패킷을 전송하는 동보 통신에 적합하며, 전송로가 혼잡해지기 쉽다.

- 스타형 네트워크: 연결장치(스테이션)가 집선 장치(허브나 스위치)의 포트 수로 제한되며, 집선장치가 스위치라면 혼잡과 충돌을 제어하기 쉽다.
<hr/>

## 4. 무선 LAN - 전파로 장치를 연결한 네트워크

### 전파를 사용하는 무선 LAN의 장점과 단점

- 장점: 케이블의 제약없이 전파가 닿는 범위 내에서 자유롭게 장치를 설치할 수 있다.

- 단점: 전파는 누군가 무단으로 가로챌 수 있는 위험이 있다.
  - 허용되지 않은 연결을 차단하는 방법
    - MAC 주소 인증
    - IEEE 802.11시리즈에선 무선 통신을 암호화

무선 LAN에 연결하려면 SSID를 지정해서 액세스포인트를 식별합니다.
일반적으로는 SSID는 주변에 브로드캐스트되지만, 이를 제한하는 기능(스텔스 SSID)도 있습니다.

- SSID(Service Set Identifier): 무선 액세스 포인트가 브로드 캐스트하는 식별자로써, 무선 클라이언트가 특정 네트워크에 연결할 때 사용됩니다.

### 무선 LAN의 보안 대책

    일반적으로 무선 LAN은 도청 위험이 높다고 여겨져 앞서 언급한 보안 기능이 프로토콜에 구현되어 있습니다. 그러나 이런 프로토콜의 보안은 완전하다고는 할 수 없습니다.
    암호화도 오래된 WEP 방식은 안전하지 않습니다(몇 시간 안에 분석 가능).
    WPA나 WPA2와 같은 새로운 암호화 기술 이용이 필수적입니다. 무선LAN을 안전하게 이용하려면 LAN 내 별도 인증 서버를 설치하는 등 상위계층에서 대책도 필요합니다

#### 용어 노트

- 무선 LAN: 규격으로서는 IEEE 802.11이 규정되어 있고, 통신에는 2계층을 사용한다.
- MAC 주소 인증: 액세스 포인트에 등록된 주소 테이블을 사용하고, 사전에 등록된 장치만 연결시키는 기능이다.
- 스텔스 SSID: SSID를 주변에 알리지 않아 참조할 수 없게 하는 기능이다.
- WEP: RC4 알고리즘을 이용한 암호 방식이다. 다양한 취약점이 발견되어 사용을 권장하지 않는다.
- WPA: TKIP로 암호화를 복잡하게 한 방식이다. 현재 개량이 진행되고 있으며 WPA2나 WPA3가 등장했다

#### 도청

유선 LAN에서도 케이블에 작업하거나 특수한 소프트웨어를 사용해서 도청할 수 있지만, 무선 LAN은 떨어져 있어도 전파를 수신할 수 있기 때문에 일반적으로 도청 위험이 높다고 여겨진다.

- 유선 LAN의 도청

  - 스니핑(Sniffing): 공격자가 네트워크에 연결된 물리적인 케이블을 감시하고 패킷을 수집하는 방식입니다. 이를 통해 데이터의 내용이나 민감한 정보를 탈취할 수 있습니다. 스니핑에는 특수한 네트워크 장비나 소프트웨어를 사용하는 경우가 많습니다.

  - 케이블 도청: 물리적으로 유선 LAN의 케이블에 접근하여 특수한 장비를 사용해 데이터를 도청하는 것입니다. 이는 네트워크에 물리적으로 접근할 수 있는 공격자가 이를 시도할 수 있는 상황에서 발생할 수 있습니다.

<hr/>

## 5. IEEE 802.x 규격 - LAN을 규정하는 규격

    IEEE 802시리즈는 LAN에 관한 다양한 사양을 규정하는 규격 체계입니다.
    이더넷이나 무선LAN이라고 하는 규격도 IEEE 802 시리즈로 규정되어있습니다.

### IEEE 802.3은 이더넷 규격

- 현재 LAN을 대표하는 이더넷 규격입니다.
- 초기 이더넷은 굵은 동축 케이블을 사용했으나, 현재는 8가닥의 트위스트 페어 케이블(LAN케이블)을 사용합니다.
- 전송 속도도 100Mbps에서 1Gbps로 고속화되었고, 1Gbps이상의 네트워크에서는 광섬유 케이블도 사용합니다.

- IEEE 802.3은 프로토콜뿐만 아니라 케이블도 규정하고 있습니다. 즉, 물리계층과 데이터 링크계층을 아우르는 규격입니다.
- 케이블은 전송속도에 따라 100BASE-T, 1000BASE-FX등으로 규격이 나뉩니다.
- 숫자는 전송속도(100Mbps, 1000Mbps)를 나타냅니다.
- 'T'는 트위스트 페어 케이블, 'FX'는 광섬유 케이블을 나타낸다

### IEEE 802.11은 무선 LAN 규격

- 이용하는 주파수 대역과 전송 속도에 따라 규격 번호 뒤에 a, b, g, ac라는 **서픽스**가 붙습니다.
- 무선 LAN의 규격은 a, ac등 서픽스 부분으로 구분하는데, 최근에는 무선LAN의 일종인 Wi-Fi라는 말을 사용하여 'Wi-Fi 5'나 'Wi-Fi 6'등으로 부르기도 합니다.

#### 용어 노트

- 트위스트 페어 케이블: 전선의 + 와 -(신호선과 GND)를 각각 2가닥씩 나선형으로 꼬아 놓은 전선으로, 노이즈에 강하다.
- 서픽스: 모델 번호 뒤에 붙이는 코드 번호다.
- Wi-Fi: 무선 LAN의 일종으로, IEEE 802.11 시리즈의 보급 및 촉진을 위해 업계 단체가 책정해서 정착되었다.

<hr/>

## 6. WAN - 넓은 범위를 연결하는 네트워크

### 광범위한 네트워클르 가리키는 WAN

    WAN은 일반적으로 LAN보다 더 넓은 물리적 범위를 연결하는 네트워크를 의미합니다. 다만 용어로서는 불특정 다수의 호스트나 디바이스 등이 연결되는 네트워크(망) 의미로도 사용됩니다.

    통신 사업자가 제공하는 전용선도 WAN이라고 할 수 있습니다.
    전용선은 은행의 ATM 회선처럼 계약자가 회선을 독점하고, 특정 거점이나 데이터센터, 인터넷을 효율적으로 상호 접속해 주는 IX 연결등에 이용됩니다.

### LAN과 WAN의 차이점

    이전에는 단지 연결 범위의 차이를 나타내는 용어였습니다.

    광역 LAN: LAN이 이더넷을 이용하면서 중간에 게이트웨이나 다른 네트워크 프로토콜을 끼워 원거리 거점을 이어주는 서비스로 네트워크는 LAN입니다.(논리적인 로컬 영역)

    또 기업의 LAN 내에서도 WAN이라는 용어가 사용됩니다.
    예를 들어 라우터의 포트에는 LAN, WAN이라고 표시 되어 있습니다. 이 경우 여러 세그먼트로 LAN을 구성할 때 장치를 집선하는 쪽이 LAN, 다른 라우터나 상위 라우터(집선장치)에 연결하는 쪽이 WAN이 됩니다. 여기에서 WAN은 LAN(세그먼트)의  바깥이라는 의미입니다.

#### 용어 노트

- IX: internet exchange의 약어. 통신 사업자, ISP, 데이터 센터 등 대량의 인터넷 통신을 취급하는 사업자가 상호 연결해서 경로 정보 등을 교환하는 연결점.

- 게이트웨이: 넓은 의미로는 네트워크의 연결 지점을 의미한다. 광역LAN에서는 원거리 통신을 위해 LAN과 다른 프로토콜의 회선을 사용할 때가 있다. 이때 프로토콜 변환과 연결 인터페이스의 역할을 담당한다.

- 네트워크 프로토콜: 원거리 거점 사이를 동일한 LAN으로 연결할 때, 중간 회선은 다양한 프로토콜과 방식, 통신 사업자를 이용한다. 통신사에 따라서는 자체적으로 대규모 이더넷망을 구축해서 원거리도 이더넷으로 연결할 때도 있다.

<hr/>

## 7. VLAN - 세그먼트를 분할하거나 결합시키는 기술

### 네트워크 구성을 유연하게 설계할 수 있는 VLAN

LAN은 L2 스위치(스위칭 허브)로 묶은 세그먼트가 최소 단위 입니다. 같은 스위치에 연결된 장치들이 하나의 세그먼트를 구성합니다.
ex) 일반적인 기업 LAN에서는 관리하기 쉽도록 층별, 부서별로 세그먼트를 분리합니다. 이때 스위치는 층이나 조직 구성에 따라 준비합니다.

스위치에 연결할 수 있는 포트 수가 정해져 있으므로 연결할 장치가 늘어나면 새로운 세그먼트를 추가해야합니다. 이 경우 **VLAN**을 사용하면 서로 다른 스위치에 연결된 장치도 같은 세그먼트로 묶을 수 있습니다.

### 세그먼트를 분할하는 이유

VLAN은 **VLAN-ID**라는 식별자를 사용해서 스위치 안팎의 논리적(가상) 세그먼트를 구성할 수 있습니다.

동일한 세그먼트는 2계층에서 브로드캐스트 패킷이 도달할 수 있는 범위를 정의할 수 있으며, ARP나 DHCP같은 프로토콜은 목적지 IP주소를 찾거나 IP주소 발급을 요청할 때 네트워크 전체에 브로드캐스트 전송을 수행합니다.
브로드캐스트 패킷은 일반적으로 같은 네트워크 세그먼트 내에서만 전파되지만, 잘못된 네트워크 디자인이나 관리 부족으로 인해 다른 세그먼트까지 확산될 수 있습니다.
-> VLAN을 사용하여 네트워크를 논리적인 세그먼트로 나누어 각각을 독립적으로 관리하면 됩니다.

3계층에서 통신하는 라우터는 IP 주소와 서브넷으로 세그먼트를 관리합니다.
라우터에서 브로드캐스트 패킷을 차단하거나, 필요한 경우에만 전파하도록 설정하거나, 서브넷을 사용하여 IP주소 범위를 나누어, 라우터를 통해 브로드캐스트가 세그먼트를 넘어가지 않도록 하면 됩니다.
또 VLAN 기능을 가진 스위치는 L3스위치뿐만 아니라 L2스위치도 있습니다.

#### 용어 노트

- VLAN-ID: 스위치 포트마다 할당하는 가상적인 번호(ID)이다.

<hr/>

## 8. SDN - 네트워크 관리 기능을 집약하는 기술

### 유연한 네트워크 구성이 가능한 가상 네트워크

논리적 구성으로 네트워크를 관리하는 기술을 가상 네트워크라 하고 가상 네트워크에는 VLAN,VPN,MPLS 등이 있습니다.

이런 기술은 네트워크 설계와 구성을 태그와 레이블을 이용해서 가상화합니다.

"태그"와 "레이블은" 네트워크에의 다양한 부분에서 사용되지만, 주로 VLAN에선 태그, VPN,MPLS에선 레이블를 사용합니다.

    1. 태그(Tag): VLAN ID를 패킷에 부착하는 과정 또는 그 결과물을 나타냅니다. 이 태그는 스위치가 패킷을 어떤 VLAN으로 전달할지 결정하는 데 사용됩니다.

    2. VPN(Virtual Private Network)의 레이블: 패킷에 암호화된 정보와 함께 VPN에 대한 식별 정보가 들어 있는 헤더가 추가됩니다. 이것을 '레이블'이라고 부를 수 있습니다.이 레이블은 패킷이 안전한 터널을 통해 전송되도록 도와주며, 외부에서의 엿보기를 방지합니다.

    3. MPLS(Multiprotocol Label Switching)의 레이블: MPLS에서는 패킷에 MPLS 레이블이 추가됩니다. 이 레이블은 최적의 전송 경로를 결정하는 데 사용되며, 패킷이 네트워크를 횡단할 때 효율적인 라우팅을 지원합니다.

대규모 네트워크를 구축하거나 좀 더 유연하게 네트워크를 구성하고 싶을 때 태그나 라벨을 이용한 가상화로는 충분하지 않을 수 있습니다. 이런 필요에 대처할 수 있는 것이 SDN입니다.

### SDN으로 관리, 제어 기능을 집약

SDN에서는 전용 스위치로 각 장치를 하나의 LAN으로 모으고, 네트워크상의 장치를 연결하는 기능(하드웨어)과 세그먼트나 라우팅을 관리 및 제어하는 기능(소프트웨어)을 분리하여 설정 정보와 네트워크 제어를 관리부분(컨트롤 플레인)에 잡중합니다. 각 장치는 전용 스위치로 연결(데이터 플레인)되어 있으면, 상세한 구성이나 제어 등은 컨트롤 플레인에서 할 수 있습니다.

SDN(Software-Defined Networking)의 관리나 제어는 REST API를 이용합니다.

    REST API: 웹 애플리케이션이나 웹 서비스 등에도 사용되는 기술로, 데이터 플레인 제어나 컨트롤 플레인 설정에는 웹 브라우저를 이용할 수도 있습니다.

SDN의 관리나 제어는 NETCONF, OpenFlow라는 프로토콜이 표준화 되어 있습니다.

<hr/>

## 9. LAN끼리 연결한 네트워크 - 각 세그먼트를 모아 구성되는 기업의 LAN

### 세그먼트를 스위치로 모아서 구성

일반적인 조직에서는 부 단위나 과 단위로 세그먼트를 구성합니다.물리적(1,2계층)에선 스위치 등으로 하나의 세그먼트로 묶어 줍니다. 그리고 이 세그먼트를 또 다른 스위치로 묶어 과에서 부, 사업부 등 상위 세그먼트로 구성해갑니다.

이때 통합할 세그먼트의 트래픽양이나 장치 수 등에 따라 라우터나 L3 스위치로 통합하기도 합니다. 3계층 장비를 사용하면 1,2계층에서 숨긴 **추상적인 IP**로 유연하게 관리할 수 있습니다.

- **추상적인 IP**는 3계층에서 사용되는 ID 주소를 의미합니다.
  - IP 주소는 네트워크에서 장치를 유일하게 식별하는 주소체계이며, 이를 사용하여 패킷이 어떤 목적지로 가야 하는지를 결정합니다. 3계층에서는 이러한 IP주소를 사용하여 네트워크를 관리하고, 상위 세그먼트의 트래픽 양이나 장치 수 등을 관리합니다.
  - IP주소를 사용하면 네트워크를 보다 유연하게 관리할 수 있습니다
    - 예를 들어, 여러 부서나 사업부 간의 통신이 필요할 때, IP 주소를 통해 라우팅을 수행하여 네트워크 트래픽을 효율적으로 관리할 수 있습니다(목적지에 따라 최적의 경로를 선택하여 패킷을 전송할 수 있기 때문). IP 주소는 계층 간의 상세한 물리적 구성과는 독립적으로 동작하므로, 네트워크의 확장성과 유연성이 향상됩니다.

### 클라이언트만 설치하는 인트라넷

세그먼트에는 업무에 사용하는 컴퓨터(클라이언트) 이외에 업무 애플리케이션 서버나 데이터베이스 서버, 파일 서버, 인증 서버 등도 연결됩니다. 서버는 보통 여러 부서와 같이 사용하므로 서버만 세그먼트를 별도로 만듭니다. 애플리케이션, 데이터베이스, 인증 시스템 등 기능 및 취급 데이터별로 독립시킵니다. 단, 해당 부서에서만 쓰이는 시스템은 해당 부서 세그먼트 내에 서버를 연결하기도 합니다.

업무 시스템을 클라우드로 옮겨서 컴퓨터나 프린터 등 클라이언트만 설치하는 사무실도 있습니다. LAN에는 인트라넷이라는 용어도 있습니다. 인트라넷은 인터넷에 직접 연결되지 않은 기업 내부 시스템을 위한 네트워크입니다.

#### L3 스위치와 라우터의 구분

- L3 스위치

  - 처리속도가 라우터보다 빠르다.
  - 패킷 내용에 따른 제어가 불가능하다.
  - 포트 수가 많다(16~48개).
  - L2 스위치를 묶을 때 사용한다

- 라우터
  - 처리속도는 L3스위치보다 느리다
  - 패킷 내용에 따른 제어가 가능하다.
  - 포트 수가 적다
  - 인터넷이나 WAN의 경계(에지)에 설치한다.

<hr/>

## 10. 인터넷에 연결된 네트워크 - 인터넷을 라우터로 중계하는 네트워크

### 에지 라우터로 인터넷과 LAN을 중계한다

LAN내에 있는 각 장치는 인터넷에 직접 연결하지 않고 인터넷과 LAN사이에 라우터나 방화벽 등을 두고 보안기능이나 주소 변환 기능 등을 갖게 합니다.
각 기업의 모든 장치에 IPv4주소(약43억개 뿐인)를 할당하는 것은 현실적이지 않고 인터넷에는 무수히 많은 공격패킷이 돌아다니므로 이런 연결 방식은 보안상 권장하지 않습니다. 이에 따라 일반적인 LAN에서는 인터넷과 LAN 사이에 라우터를 설치해서 내부와 외부 패킷을 분리합니다.

이떄 라우터는 내부와 외부 네트워크를 분리하는 방화벽 역할을 합니다.
방화벽은 전용 장비가 있지만 라우터에 방화벽 기능을 포함한 제품도 있습니다.

### 보안 기능과 주소 변환 기능이 필요하다

- 공격 패킷, 불법적인 액세스를 차단

  - 방화벽: IP주소 정보를 기반으로 외부 위협이 되는 패킷을 차단합니다.
  - 패킷의 프로토콜 종류나 출발지 포트 번호를 참조해서 특정 서비스나 연결을 차단할 수도 있습니다.

  인터넷상에서 주고받는 패킷은 **에지 라우터**나 서버 등과 글로벌IP 주소를 사용해서 교환됩니다. 외부에서 LAN 내부의 각 장치까지 패킷을 전달하려면 NAT, NAPT기능도 필요합니다. NAT, NAPT기능은 대부분 방화벽에 통합되어 있습니다.

#### 용어 노트

- 공격 패킷: 정찰, 방해, 파괴, 도용 등 의도(악의)를 가진 자가 생성 및 전송한 패킷이다. 프로토콜상의 형식(데이터 구성 규칙)만으로는 악의성 여부를 판단할 수 없기 때문에 공격 패킷 식별은 쉽지 않다.

- 에지 라우터에 필요한 기능
  - NAT, NAPT(글로벌 IP <--> 프라이빗 IP 변환)
  - 외부 위협 패킷 차단 (방화벽 기능)

<hr/>

## 11. 모바일 네트워크를 활용한 네트워크 - 모바일에서 인터넷에 연결하는 네트워크

### 모바일 네트워크의 구조

인터넷에 연결하려면 3계층 이상의 프로토콜을 사용합니다. 프로토콜 스택의 개념을 적용하면 1,2계층은 주로 물리적인 데이터 전송과 관련이 있어 어떤 어떤 상위 계층 프로토콜을 사용하는지에 크게 영향을 받지 않지만, 3계층 이상부터는 프로토콜에 따라 통신의 목적과 방식이 결정됩니다.

스마트폰의 회선을 모바일 네트워크라고합니다. 인터넷과 호환되지 않는 프로토콜로 통신하지만, **패킷 교환 방식**은 공통입니다. 따라서 패킷의 페이로드를 프로토콜 스택으로 **캡슐화**하면 모바일 네트워크에 인터넷 패킷을 실을 수 있습니다(스마트폰 앱이 인터넷 패킷을 생성하고, 이를 모바일 네트워크 프로토콜의 페이로드로 변환하는 것).
통신사의 모바일 네트워크에 설치된 **인터넷 게이트웨이**는 이런 패킷을 처리하여 인터넷으로 전송하는 역할을 합니다.

### 통신 모듈이나 텔레워크에서 네트워크 연결

IoT기기 등은 액세스 포인트(AP)를 이용하여 인터넷에 속하지만, 4G,5G를 지원하는 통신 모듈을 이용해서 인터넷에 접속할 수 있는 제품도 있습니다.

통신모듈은 화면이나 키패드만 없을 뿐 무선 부분과 SIM카드는 스마트폰이나 휴대전화 등과 동일합니다. ex) 스마트카, 스마트홈 기기, 산업용IoT기기, 웨어러블 기기, 스마트 농업 기술

#### 용어 노트

- 통신 모듈: 계약 정보가 입력된 SIM카드와 기지국과 통신하는 송수신기를 갖춘 통신 단말기다. 장치에 내장하는 것을 전제로 하며, 디스플레이나 키패드는 갖지 않는다.

##### 게이트웨이와 인터넷 게이트웨이

1. 게이트웨이: 네트워크에서 여러 프로토콜이나 네트워크 간에 통신할 수 있도록 해주는 장치. 즉, 게이트웨니는 서로 다른 프로토콜을 사용하는 네트워크 간의 통신을 중계하고 변환하는 역할을 합니다.

2. 인터넷 게이트웨이: 주로 내부 사설 네트워크와 인터넷 간의 통신을 관리하는 데 사용되는 특정 유형의 게이트웨이. 인터넷 게이트웨이는 주로 NAT, 방화벽, 프록시 서버 등을 포함한 기능을 수행하여 내부 네트워크의 디바이스들이 안전하게 인터넷에 접속하고 통신할 수 있도록 합니다.

--> 게이트웨이는 네트워크 간의 통신을 중계하고 변환하는 일반적인 용어이며, 인터넷 게이트웨이는 주로 내부 네트워크와 인터넷 간의 통신을 관리하는 특정한 종류의 게이트웨이입니다.
