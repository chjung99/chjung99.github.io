# Linux Container Primitives

리눅스 컨테이너(Linux Container)는 애플리케이션을 실행하기 위한 격리된 환경을 제공하는 기술입니다. 가상 머신(VM)과 달리 별도의 운영체제(OS)를 부팅하지 않고 호스트 OS의 커널을 공유하며, 리눅스 커널에서 제공하는 핵심 기능들을 조합하여 컨테이너라는 가상의 공간을 만들어냅니다.

이 문서는 컨테이너를 구성하는 리눅스의 핵심 기반 기술들에 대해 다룹니다:

* **[Namespace](1.Namespace.md)**: 프로세스가 볼 수 있는 시스템 리소스(PID, Network, Mount 등)를 격리하여 독립적인 뷰(View)를 제공하는 기술입니다.
* **[Cgroups (Control Groups)](2.Cgroups.md)**: 프로세스가 사용할 수 있는 시스템 리소스(CPU, Memory, I/O, Network 등)의 한도를 설정하고 모니터링 및 제어하는 기술입니다.
* **[OverlayFS](3.OverlayFS.md)**: 여러 개의 파일 시스템 계층을 겹쳐서 하나의 디렉터리 구조로 보여주는 Union Mount 방식의 파일 시스템으로, 컨테이너 이미지 레이어를 구성하는 데 주로 사용됩니다.
* **[veth (Virtual Ethernet Pair)](4.veth.md)**: 두 개의 격리된 네트워크 네임스페이스(예: 호스트와 컨테이너)를 연결해주는 가상의 네트워크 케이블과 같은 역할을 하는 인터페이스입니다.
