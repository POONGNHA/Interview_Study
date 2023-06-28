 - 에러 종류 :: 권한 에러
 -------------------------------------------------------------------------------------------------------------------
 - 에러 내용 :: 
PS C:\Develops\vue3_example> vue create vuedongsan
vue : 이 시스템에서 스크립트를 실행할 수 없으므로 C:\Users\sss96\AppData\Roaming\npm\vue.ps1 파일을 로드할 수 없습니다. 자세한 내용은 about_Execution_Policies(https://go.microsoft.com/fwlink/?LinkID=135170)를 참조하십시
오.
위치 줄:1 문자:1
+ vue create vuedongsan
+ ~~~
    + CategoryInfo          : 보안 오류: (:) [], PSSecurityException
    + FullyQualifiedErrorId : UnauthorizedAccess
---------------------------------------------------------------------------------------------------------------------
- 에러 해결 ::
(참조 페이지)[https://hellcoding.tistory.com/entry/VSCode-%EC%98%A4%EB%A5%98-%EC%9D%B4-%EC%8B%9C%EC%8A%A4%ED%85%9C%EC%97%90%EC%84%9C-%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8%EB%A5%BC-%EC%8B%A4%ED%96%89%ED%95%A0-%EC%88%98-%EC%97%86%EC%9C%BC%EB%AF%80%EB%A1%9C]
cmd-powershell에서 권한을 Restricted에서 RemoteSighed로 변경해주면 스크립트 허용이 가능하게 된다.
즉 시스템에서 스크립트를 실행할 수 있도록 권한을 부여해주면 된다.
