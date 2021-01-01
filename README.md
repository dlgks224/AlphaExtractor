# AlphaExtractor - 알파추출기
Extracts strings of Rimworld mode file with custom nodes and Exports to language xml files.  
림월드 모드 파일의 노드를 추출하고, 사용자가 문자열들을 선택하여 language xml 파일로 출력할 수 있도록 해 줍니다.

# 오류 제보 및 개선사항
항상 두 팔 벌려 환영하고 있습니다.  
github의 Issues 메뉴를 이용해 사소한 오류부터 중대한 오류까지 모든 버그를 제보받고 있습니다.  
같은 방법으로 개선 사항을 받고 있습니다.  

# 버전 일람
## 0.10
> `경고`: `0.10.4` 이후로 `xml` 파일 출력 모드에 대한 새로운 기능 추가나 개선에 대한 지원을 중단합니다. 

* 0.10.8
  * `버그`: 출력 노드 분류 화면에서, 이전의 태그 분류 일부가 저장되지 않았던 문제가 수정되었습니다.

* 0.10.7
  * `외관`: 화면의 모든 `뒤로가기` 버튼이 사라집니다. 우측 상단의 `X` 버튼을 통해 메인 화면으로 돌아갈 수 있습니다.
  * `외관`: 콘솔 화면이 제거됩니다.
    * 이에 따라 출력되는 모든 알림 메시지와 에러 메시지는 `error_report.txt`에 저장되며, 프로그램 실행 시 초기화됩니다.
    * 이에 따라 출력되는 모든 에러 메시지는 별도의 알림창으로 표시됩니다.
  * `개선`: 이제 분류한 태그 작업이 저장/불러오기 없이 기본값으로 지정할 수 있는 기능이 추가되었습니다.
  * `버그`: 출력 노드 분류 화면에서, 빈 목록의 항목을 선택한 채로 태그 분류를 시도하는 경우 에러 메시지가 출력되는 문제가 수정되었습니다.
    

* 0.10.6
  * `개선`: 이제 추출기에 기록된 림월드의 버전이 `1.2`로 변경됩니다.

* 0.10.5
  * `버그`: `xlsx` 파일을 `xml` 파일로 변환할 때, `Keyed` 폴더가 `DefInjected` 폴더 하위에 생성되는 문제가 수정되었습니다.
  * `버그`: `LoadFolders.xml`의 폴더 항목이 공백으로 되어 있을 때, 모드의 최상위 디렉토리를 검색하지 않는 문제가 수정되었습니다.
  * `버그`: 림월드 혹은 확장팩의 추출을 시도할 때, 오류가 표시되는 문제가 수정되었습니다.
  * `버그`: `DefInjected`나 `Patches`가 아닌 폴더만 추출할 때, 오류가 표시되는 문제가 수정되었습니다.

* 0.10.4
  * `경고`: `0.10.4` 이후로 `xml` 파일 출력 모드에 대한 새로운 기능 추가나 개선에 대한 지원을 중단합니다.
      * 해당 기능은 `0.10` 버전에 한해 유지되며, 다음 중소 업데이트 시 최종적으로 삭제될 수 있습니다.
      * 필요한 경우 `xlsx` 파일로 출력한 후 변환 기능을 이용하세요. 
  * `개선`: 이제 `RimWaldo (림왈도)` 대신 `Korean (한국어)`를 기본 언어로 지정합니다.
  * `개선`: 이제 `xlsx` 파일로 출력할 경우 해당 파일에 추출한 모드명과 `pakageID`를 함께 기록합니다.
      * `xml` 파일로 출력할 경우는 대응되는 사항을 지원하지 않습니다.
  * `개선`: 이제 `xlsx` 파일을 `xml` 파일로 변환할 때, 기록된 모드명이 있으면 해당 이름으로 된 폴더를 생성하여 저장합니다.
      * 이 때, 기록된 모드명이 없으면 `xlsx` 파일의 이름을 모드명으로 간주합니다.      
  * `개선`: 이제 `xlsx` 파일을 `xml` 파일로 변환할 때, 기록된 `pakageID`가 있으면 `LoadFolders.xml`에 알맞은 형식으로 출력합니다.
  * `버그`: 노드 분류 창의 검색 칸이 빈 상태로 `백스페이스 키`를 계속 입력할 때, 추출된 노드들이 누적되는 문제가 수정되었습니다.

* 0.10.3
  * `개선`: 실행파일의 경량화가 이루어져 용량이 절반 가량 축소되었습니다.
  * `개선`: 이제 모드 이름에 폴더/파일명으로 금지된 문자가 포함되어 있을 경우 출력 폴더/파일명에서 자동으로 제외됩니다.
  * `개선`: 이제 출력 폴더/파일명에 폴더/파일명으로 금지된 문자가 포함되어 있을 경우 경고를 표시합니다.
  * `버그`: 이제 시나리오 관련 노드의 추출에서 `scenario` 노드를 자동으로 삽입한 노드도 중복 추출합니다.
      * 이 때, 모드에 이미 정의된 노드가 존재한다면 추출기가 생성한 이 노드는 덮어씌워집니다.
  * `버그`: `xlsx` 파일로 출력하였을 때, `채우기 색`이 검정색으로 지정되는 문제가 추가적으로 수정되었습니다.

* 0.10.2
  * `개선`: 이제 `림왈도 팀` 내부 형식의 `xlsx` 파일을 `xml` 파일로 변환할 수 있는 기능이 추가됩니다. 
  * `버그`: 출력 폴더/파일의 이름에 너무 많은 공백이 들어가는 문제가 수정되었습니다.

* 0.10.1
  * `개선`: 이제 모드 폴더 번호를 읽을 때, `PublishedFileId.txt`를 읽는 데 실패하였을 경우 모드 폴더의 이름 사용을 시도합니다.
  * `버그`: `xlsx` 파일로 출력하였을 때, `채우기 색`이 검정색으로 지정되는 문제가 수정되었습니다.

* 0.10.0
  * `외관`: 알파추출기의 UI가 개편되어 반복 작업이 최소화되었습니다.
    * 이제 각 작업 화면의 `X` 버튼이나 `뒤로가기` 버튼을 통해 메인 화면으로 돌아갈 수 있습니다.
    * 메인 화면
        * 메인 화면과 각 작업 화면이 분리되었습니다.
        * 메인 화면에서는 각 작업 화면에서 설정된 내용의 요약을 확인할 수 있습니다.
    * 림월드 및 창작마당 위치 지정 화면
        * 이제 림월드 및 창작마당의 위치를 지정했을 경우, 해당 화면을 다시 접할 필요가 사라집니다.
    * 추출 모드 선택 화면
        * 이미 추출 작업이 이루어진 상황에서 새로 작업을 시도할 경우 경고창이 출력됩니다.
    * 출력 노드 분류 화면
        * 이제 바닐라의 노드 분류를 따라갈 경우, 해당 화면을 다시 접할 필요가 사라집니다.
        * 이제 Keyed/Strings의 추출로 인해 Defs 노드가 존재하지 않을 때 실행할 경우 경고를 표시합니다.
    * 출력 옵션 지정 화면
        * 이제 출력 형식 등 기타 설정을 변경할 필요가 없는 경우, 해당 화면을 다시 접할 필요가 사라집니다.
  * `개선`: 이제 추출기에 기록된 림월드의 버전에 맞추어 모드의 추출 버전이 자동으로 선택됩니다.
  * `개선`: 이제 출력 폴더명 및 파일명이 `모드 이름 - 모드 주소`의 기본값으로 지정됩니다.
    * 이제 사용자가 직접 변경한 출력 폴더명 및 파일명은 더 이상 다음 실행 시 보존되지 않습니다.
  * `개선`: 이제 XML 출력 시 추출기에 기록된 언어의 기본 하위 폴더가 자동으로 생성되어 저장됩니다.
  * `개선`: 이제 list 태그는 `TKey`의 값이 존재할 경우 해당 값으로 대체되어 출력되며, 분류 시 상위 태그로 분류됩니다.
  * `개선`: 이제 빈 텍스트(줄넘김이나 띄어쓰기 포함)만 가진 노드는 추출하지 않습니다.
  * `버그`: `Patches`의 `PatchOperationFindMod`에서 `nomatch`를 인식하지 못하는 문제가 수정되었습니다.
  * `버그`: `Patches`에서 다른 모드에 의존하지 않음에도 노드를 변경하는 패치를 추출하지 않는 문제가 수정되었습니다.
  * `버그`: 중복된 노드가 존재함에도 별개의 노드로 인식하는 문제가 수정되었습니다.
    * 이제 모든 중복 노드는 추출 모드 선택 창의 폴더 순서에 따라, 추출된 순서에 따라 위의 내용을 아래의 내용이 덮어씁니다.
  
## 0.9
* 0.9.3
  * `개선`: 출력 파일 이름의 확장자가 선택한 모드에 맞게 적절히 추가됩니다.
  * `개선`: `xlsx` 출력 모드의 열 규칙이 변경하였습니다. 이제 변경된 기존 노드는 번역을 제외하고 모두 버려집니다. 

* 0.9.2
  * `개선`: 이제 `xlsx` 형태의 출력이 가능합니다. 열 형식은 `림왈도 팀`의 내부 형식을 따릅니다. 
  
* 0.9.1
  * `개선`: 이제 상속된 `Defs`의 노드 추출을 지원합니다. 

* 0.9.0
  * `개선`: 이제 `Defs`, `Keyed`와 `Strings` 외에도 `Patches`의 추출을 지원합니다. 
  * `버그`: `&lt;`의 `&`도 `&amp;`로 대치하는 문제가 수정되었습니다.
  * `외관`: 프로그램의 아이콘의 크기가 더 크게 변경되었습니다.

## 0.8

* 0.8.8
  * `버그`: 프로그램이 아이콘을 불러오지 못해 실행이 불가능한 문제가 수정되었습니다.

* 0.8.7
  * `외관`: 프로그램의 아이콘이 등록되었습니다. 아이콘은 `네모냥(RKTM팀)`께서 기부해 주셨습니다!
  * `외관`: 추출할 모드 목록의 폰트 크기가 약 83%로 축소되었습니다.
  * `버그`: 게임/모드 경로 지정을 변경할 경우 프로그램을 재시작해야 적용되는 문제가 수정되었습니다.
  * `개선`: 이제 `<`와 `&`만 `&lt;`와 `&amp;`로 대치되여 추출됩니다. 검색 시 유의하세요.


* 0.8.6
  * 이제 프로그램 실행 시 최신 버전을 확인하고, 업데이트를 안내합니다.
  * 이제 `<`와 `>`는 `&lt;`와 `&rt;`로 대치하여 추출합니다.

* 0.8.5
  * 이제 바닐라의 코어/로얄티의 텍스트를 추출할 수 있습니다. `tar`로 압축되어 있는 `Keys` 폴더의 내용물은 인식이 불가능합니다.

* 0.8.4
  * `config.dat` 파일이 존재하지 않을 경우 (첫 실행 시) 프로그램이 실행되지 않는 현상이 해결되었습니다.
  * 이제 텍스트가 없을 경우 `Defs`에서는 `ERROR:{$BLANK TEXT}`도 출력되지 않으며, `Keyed`에서는 오류가 발생하지 않습니다. 

* 0.8.3
  * `병합하기`에서 추출되지 않은 노드가 삭제되는 현상이 해결되었습니다.  
  * 이제 `병합하기`모드에서 추출하지 않은 노드는 주석 처리되어 출력됩니다.

* 0.8.2
  * 이제 모든 필터(검색)에서 띄어쓰기와 대소문자 구분이 무시됩니다.  
  * 이제 분류한 태그 작업을 추후 재분류를 위해 저장/불러오기가 가능합니다.  
  * `TEST` 이제 list 태그는 분류 시 상위 태그로 분류되지만 출력은 해당하는 번호로 출력됩니다.  

* 0.8.1
  * 모드 선택창의 전반적인 개선이 이루어졌습니다.  
  * 이제 추출할 모드의 검색이 가능합니다.  
  * 이제 `LoadFolders.xml`의 모드 의존성 정보가 추출 선택창에 표시됩니다.  
  * 이제 서로 다른 버전의 다른 폴더들을 한꺼번에 추출할 수 있습니다. 노드의 중복이 발생할 경우, 위의 노드 텍스트는 아래의 노드 텍스트로 덮어씌워집니다.  
  * 이제 오류로 인해 추출되지 않던 `Strings`가 정상적으로 추출됩니다.  
  
* 0.8.0
  * 이제 `Defs` 외에도 `Keyed`와 `Strings`의 추출을 지원합니다. 

## 0.7
* 0.7.7
  * 이제 리스트 형태의 태그(숫자로 끝나는 태그)를 번역 가능한 형태로 추출할 수 있습니다. 
* 0.7.6
  * 파일 출력의 `건너뛰기` 옵션이 삭제되었습니다.  
  * 파일 출력의 텍스트 선택 모드에서 `원본`을 선택해도 다음 실행 시 `TODO`로 초기화되어 있는 현상을 수정하였습니다.  
  * `Patches`와 `Keyed` 등 여러 폴더를 지원하기 위해 코드의 구조가 개선되었습니다.  
* 0.7.5
  * 파일 출력의 `참조하기` 기능이 추가되었습니다. 해당 모드는 `추가하기` 모드와 유사하지만, 추출하지 않은 태그를 파일에 남기지 않습니다.  
  * 파일 출력의 여러 모드가 5개로 늘어남에 따라, 이제 각 선택지 위에 마우스를 올려 해당 모드의 설명을 나타내는 툴팁이 추가되었습니다.  
  * 이제 더 이상 태그 분류 작업을 확인하는 창이 뜨지 않습니다. 하지만 조심하세요! 태그 분류 작업 완료는 아직 되돌릴 수 없습니다!  
* 0.7.4
  * 파일 출력의 추가하기 모드를 사용했을 경우 파일이 출력되지 않거나 오류가 발생하는 문제를 해결했습니다.
* 0.7.3
  * 이제 파일 출력의 `추가하기` 모드에서 출력되는 태그들의 순서는 알파추출기가 새로 추출한 태그의 순서를 따릅니다.
* 0.7.2
  * 파일 출력 시 텍스트를 `{$TODO}` 대신 `TODO`로 출력합니다.  
* 0.7.1
  * 비정상적인 모드가 있을 경우 모드의 이름 대신 폴더의 이름을 로드합니다.
* 0.7
  * 이제 바닐라 번역에 등장하는 모든 태그들이 자동으로 추출 대상에 포함됩니다.  
  * 이제 태그 분류를 제외하고 입출력 폴더, 파일, 형식 등등의 모든 설정값이 저장되어 다음 실행시 유지됩니다.  

