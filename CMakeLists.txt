cmake_minimum_required(VERSION 3.13) #해당 cmake 사용 위해 14버전 이상

set(PROJECT_NAME cmake_project_example) #프로젝트 이름 변수 설정
set(CMAKE_CXX_STANDARD 17) #CMAKE로 시작하는 건 global 변수, c++ 버전 17버전 사용용

project(${PROJECT_NAME}) #변수 사용, 프로젝트 세팅
add_executable(${PROJECT_NAME} src/main.cpp) #뒤에 거 컴파일해서 프로젝트의 실행파일 만듦

# cmake -Bbuild . -DCMAKE_BUILD_TYPE=Debug
# -B는 빌드할 것, -D는 빌드타입
#cmake --build build
#build\Debug 안에 exe(실행파일) 생김
#.\build\DebPug\cmake_project_example
#프로그램 실행


#하지만 이 방법은 너무 귀찮음
#ctrl+shift+p에서 cmake를 검색하면 cmake:configure가 뜸
#비주얼 스튜디오 버전에 맞게 누르면 됨
#cmake : build 로 빌드 가능
#또는 cmake 관련 tab 생성된 후 빌드 눌러서 가능

#빌드는 F7, 실행은 ctrl+ F5

# repository 저장소, clone 한 번에 업뎃, commit 변경 저장, commit hash 고유 id, push, pull
# git init