# malgun-tweaked
일본어 폰트가 제거된 맑은 고딕

## 주요 특징

* 못생긴 일본어 폰트를 Yu Gothic UI로 대체해줍니다.
* 영문판에 적용할 시 언어 변경 편법 없이 UWP 앱에서 Yu Gothic UI로 일본어 폰트를 출력해줍니다.

## 적용법

### 레지스트리 (자동)
* 폰트를 다운받으신 후 C 드라이브 최상위 경로 등 기억하기 쉬운 위치에 복사해주세요.
* 기존 맑은 고딕 폰트와 HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\FontLink\SystemLink 레지스트리는 백업하십시오.
* 레지스트리를 적용해주십시오.

### 레지스트리 (수동)
* 검색 및 실행 창에서 regedit를 입력하여 레지스트리 편집기를 실행하십시오.
* HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\FontLink\SystemLink 레지스트리로 이동하십시오.
* Malgun Gothic의 문자열에 이 내용을 복사하십시오.
  * Malgun Gothic
```
SEGOEUI.TTF,Segoe UI,130,81
SEGOEUI.TTF,Segoe UI
YUGOTHM.TTC,Yu Gothic UI,128,96
YUGOTHM.TTC,Yu Gothic UI
MSJH.TTC,Microsoft Jhenghei UI,128,96
MSJH.TTC,Microsoft Jhenghei UI
MSYH.TTC,Microsoft YaHei UI,128,96
MSYH.TTC,Microsoft YaHei UI
GULIM.TTC,Gulim
MEIRYO.TTC,Meiryo UI,128,96
MEIRYO.TTC,Meiryo UI
SEGUISYM.TTF,Segoe UI Symbol

```
   * Malgun Gothic Bold
```
SEGOEUIB.TTF,Segoe UI Bold,130,81
SEGOEUIB.TTF,Segoe UI Bold
YUGOTHB.TTC,Yu Gothic UI Bold,128,96
YUGOTHB.TTC,Yu Gothic UI Bold
MSJHBD.TTC,Microsoft Jhenghei UI Bold,128,96
MSJHBD.TTC,Microsoft Jhenghei UI Bold
MSYHBD.TTC,Microsoft YaHei UI Bold,128,96
MSYHBD.TTC,Microsoft YaHei UI Bold
GULIM.TTC,Gulim
MEIRYOB.TTC,Meiryo UI Bold,128,96
MEIRYOB.TTC,Meiryo UI Bold
SEGUISYM.TTF,Segoe UI Symbol

```
   * Malgun Gothic Semilight
```
SEGOEUISL.TTF,Segoe UI Semilight,130,81
SEGOEUISL.TTF,Segoe UI Semilight
YUGOTHR.TTC,Yu Gothic UI Semilight,128,96
YUGOTHR.TTC,Yu Gothic UI Semilight
MSJH.TTC,Microsoft Jhenghei UI,128,96
MSJH.TTC,Microsoft Jhenghei UI
MSYH.TTC,Microsoft YaHei UI,128,96
MSYH.TTC,Microsoft YaHei UI
GULIM.TTC,Gulim
MEIRYO.TTC,Meiryo UI,128,96
MEIRYO.TTC,Meiryo UI
SEGUISYM.TTF,Segoe UI Symbol

```

### 폰트 적용

* 복구 메뉴로 재부팅하십시오.
  * 제조사별 복구 메뉴 부팅 키 사용 (HP 파빌리온 x360 14인치 2021년 모델 기준 F11 연타)
  * 설정 - 시스템 - 복구 - 고급 시작 옵션 항목에서 다시 시작 클릭
* 명령 프롬프트에 진입하여 C 드라이브로 이동하십시오.

```
cd C:
C:
```

* 아래의 명령어를 입력하여 맑은고딕 폰트를 바꿔주시고 폰트 캐시를 제거하십시오.

```
copy malgun.ttf C:\Windows\Fonts
copy malgunbd.ttf C:\Windows\Fonts
copy malgunsl.ttf C:\Windows\Fonts
del C:\Windows\System32\FNTCACHE.dat
```

* Windows로 진입하여 폰트가 출력되는지 확인하십시오.

## 라이선스

* 원본 폰트의 저작권은 마이크로소프트에 있으며, 변경된 폰트는 Windows 내에서의 사용을 전제로 배포됩니다.
* 웹폰트 임베딩, 상업 목적으로 사용하지 마십시오.
