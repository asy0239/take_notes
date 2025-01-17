# 통합인증(SSO, Single Sign-On)

한 번의 인증 과정으로 여러 컴퓨터 상의 자원을 이용 가능하게 하는 인증 기능이다. 

예를 들어 어느 컴퓨터에 로그인한 후 그룹웨어 등의 응용 프로그램을 사용할 때에 또 로그인, 다른 서버상의 응용 프로그램을 사용할 때에도 다시 로그인이 필요한 상황이라면, 사용자는 여러 개의 아이디와 비밀번호를 관리해야 한다. 통합인증을 도입한 환경에서는 사용자는 하나의 아이디와 비밀번호로 모든 기능을 사용할 수 있다.

보안이 필요한 환경에서 통합인증을 도입하는 경우, 여러 응용 프로그램의 로그인 처리가 간소화되어 편리성을 도모할 수 있는 반면, 통합인증의 시작점이 되는, 즉 최초의 로그인 대상이 되는 응용 프로그램 혹은, 운영체제에 대한 접근 보안이 중요하게 된다. 보안위험이 적은 환경에서는 편리성만을 추구하면 되지만, 보안이 요구되는 환경에서는 1회용 비밀번호를 이용하는 등, 이중 인증 등으로 보안을 강화할 필요가 있다.

업무 시스템이 여러 웹 응용 프로그램으로 사내에 나뉘어 있는 상황이 증가하고 있어, 이에 대해서 통합인증을 제공하는 패키지도 있다. 최근에는 웹 응용 프로그램뿐만 아니라, 단말 에뮬레이터나 클라이언트 서버 모델의 응용 프로그램에 대응되는, 기업용 통합인증 제품이 나와 있다.

도입시에는 통합인증 대상 응용 프로그램 변경이 필요한지를 고려해야 한다. 응용 프로그램의 변경이 필요한 경우, 도입 비용과 위험이 높아질 수 있다.

기타 공유 인증 스킴에는 [OAuth](https://ko.wikipedia.org/wiki/OAuth), [OpenID](https://ko.wikipedia.org/wiki/OpenID), [OpenID Connect](https://ko.wikipedia.org/w/index.php?title=OpenID_Connect&action=edit&redlink=1), [페이스북 커넥트](https://ko.wikipedia.org/w/index.php?title=페이스북_커넥트&action=edit&redlink=1)가 있다. 그러나 이러한 인증 스킴들은 사용자가 다른 사이트나 애플리케이션에 접근할 때마다 로그인 자격정보를 입력해야 하기 때문에 SSO와 혼동되어서는 안 된다