# IIS 세팅
## 1. IIS란?
IIS는 Internet Information Sevices 의 약자 이며,
마이크로소프트 원도우를 사용하는 서버들을 위한 인터넷 기반 서비스들의 모임
아파치 웹서버에 이어 세계에서 두번째로 가장 잘 알려진 웹서버입니다.
서버는 현재 FTP, SMTP, NNTP, HTTP/HTTPS를 포함하고 있습니다.   
지금까지 IIS 8.0 버전이 나왔습니다
(IIS 8.0 은 windwos server 2012, Windwos 8 부터 사용 가능합니다)
장점이자 단점인 마이크로소프트에서 제공하는 윈도우 OS에서만 사용이 가능하다는점..


## 2. IIS 세팅
 ### 1. 제어판 - 프로그램 - 프로그램 및 기능 - "Windows 기능 켜기/끄기" 를 클릭합니다.
 
![994D4A4B5B02EDD411](https://user-images.githubusercontent.com/68521148/111440255-82197180-8749-11eb-994f-e8bee0617a26.png) 


 ### 2. "Windows 기능 켜기/끄기" 화면에서 필요한 기능을 켭니다.
 * "인터넷 정보 서비스(Internet Information Service)"를 확장합니다.
 * "World Wide Web 서비스" 를 켭니다. 여기서는 하위 기능은 기본으로 합니다.
 * "웹 관리 도구"에서는 "IIS 관리 콘솔"에 체크합니다.
 
![999CFA425B02EDE40B](https://user-images.githubusercontent.com/68521148/111440619-de7c9100-8749-11eb-937d-a004db8045fe.png)


 ### 3. 응용 프로그램 개발 기능
 * IIS에서 응용프로그램을 실행하기 위해서 기능을 추가할 수 있습니다.
 * "ASP"를 체크해서 asp 프로그램을 실행할 수 있습니다.(이제는 잘 사용하지않습니다.)
 * "ASP.NET 3.5" 또는 "ASP.NET 4.7" 을 선택해서 asp.net 프로그램을 실행 수 있습니다.
 * "CGI(Common Gateway Interface)" 는 IIS 가 외부 프로그램을 실행시키는 방법을 제공해줍니다. CGI는 오래전부터 사용되어진 방법인데 요즘은 잘 사용하지 않는것 같습니다. 이 방식은 요청이 있을때마다 외부 프로그램 실행해서 요청이 만큼 외부 프로그램의 프로세스가 생성됩니다.
 * "ISAPI(Internet Server Application Programming Interface)" 는 PHP 와 Java 응용프로그램의 연동에 사용되어집니다. 이 방식은 웹서버 프로세스에서 DLL을 로드한 후 필요할때 호출하는 방식이므로 CGI보다 빠르게 수행됩니다. Thread 로 수행되므로 PHP 연동시 Thread-safe 바이너리를 사용하는게 안정적입니다. Non Thread-Safe 바이너리를 사용시 ISAPI 대신에 FastCGI를 사용하게 됩니다.
* 위 까지 진행 후 확인을 눌러 기능을 켜주세요.

 ### 4. IIS 관리자 실행
 
 ![image](https://user-images.githubusercontent.com/68521148/111441258-81cda600-874a-11eb-9dff-6c4bb319c6dd.png)
 
 ![image](https://user-images.githubusercontent.com/68521148/111441339-9611a300-874a-11eb-8851-2ee0e81164b2.png)

 * 왼쪽 트리 에서  사이트의 Default Web Site 를 선택하고, 오른쪽의 시작 버튼을  눌러 웹사이트를 실행합니다.

  ![1](https://user-images.githubusercontent.com/68521148/111926213-45ee6400-8aef-11eb-9fd1-df2fc5f3bb08.png)

---
***단순 HTML로만 만들어진 사이트와 세팅 하는 방법과 닷넷을 사용해 만든 사이트를 세팅하는 방법은 다릅니다.***  
***조만간 업데이트 하도록 하겠습니다.***
