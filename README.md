# Java 개발자를 위한 Rust 학습 가이드

Java 개발자를 위한 단계별 Rust 전환 가이드입니다.  
Java 21 · Rust 2021 (rustc 1.82) 기준으로 작성됐으며,  
모든 예제는 브라우저에서 바로 실행 가능합니다 (Wandbox 연동).

## 🔗 GitHub Pages

**[hans9500.github.io/rust-guide-for-java-developer](https://hans9500.github.io/rust-guide-for-java-developer)**

---

## 📚 코스 선택

| | [2시간에 배우는 Rust](rust_java-developer_2h.html) | [전체 가이드](rust_java-developer.html) |
|---|---|---|
| 대상 | 입문 · 빠르게 | 레퍼런스 · 심화 |
| 비교 언어 | Java ↔ Rust | Java ↔ C++ ↔ Rust |
| 섹션 | 24 | 37 |
| 예제 | 447 | 163 |
| 크기 | 2,314 KB | 839 KB |

---

## 🚀 2시간에 배우는 Rust

Java 개발자가 Rust로 전환하기 위한 핵심 개념을 집중적으로 다룹니다.  
도서 관리 시스템을 점진적으로 발전시키며 소유권부터 스마트 포인터까지 학습합니다.  
각 섹션 왼쪽 `+` 버튼으로 파트별 빠른 이동이 가능합니다.

### 섹션 목록

| # | 제목 | 핵심 개념 |
|---|------|---------|
| 0 | 들어가며 | Rust vs Java 철학 비교 |
| 1 | 변수와 타입 | let, mut, const, shadowing, 기본 타입 |
| 2 | 제어 흐름 | if, loop, while, for, 중첩 루프 라벨 |
| 3 | 문장과 표현식 | 표현식 지향, 세미콜론의 의미 |
| 4 | 소유권 ⭐ | Move, Copy, Clone, RAII, String 메모리 구조 |
| 5 | 빌림 ⭐ | &T, &mut T, 빌림 규칙, Slice, 참조 3단계 구조 |
| 6 | 라이프타임 ⭐ | 'a, 댕글링 참조, 시나리오 10개, 생략 규칙 3가지 |
| 7 | 문자열 | String vs &str, 주요 메서드 |
| 8 | 구조체 | struct, impl, self의 3가지 형태, derive |
| 9 | enum/match | enum, match, if let, let else, 고급 패턴 |
| 10 | Option | Option\<T\>, map, and_then, ? 맛보기 |
| 11 | Result | Result\<T,E\>, 커스텀 에러 타입 |
| 12 | 에러 처리 ? | ? 연산자, From trait, panic! |
| 13 | 제네릭 | Generics\<T\>, trait bound, 단형화 |
| 14 | 트레잇 ⭐ | trait, dyn Trait, impl Trait, 정적/동적 디스패치 |
| 15 | 컬렉션 | Vec\<T\>, HashMap\<K,V\>, HashSet\<T\> |
| 16 | 클로저/Iterator | Fn/FnMut/FnOnce, filter, map, collect |
| 17 | 동시성 | thread, Arc, Mutex, mpsc 채널, Send/Sync, async/await, Future |
| 18 | 더 깊은 Rust | Drop, From/Into, Rc, RefCell, Cow, Pin, Deref, **Box\<T\>** |
| 19 | dyn 심화 + move 심화 | fat pointer, &dyn vs Box\<dyn\>, move 클로저 내부 원리 |
| 20 | impl 완전 정복 ⭐ | 모든 impl 형태, impl Trait vs Box\<dyn\> 반환 비교 |
| 21 | 전체 예제 | 도서관 관리 시스템 (s1~s18 통합) |
| 22 | CLI 테트리스 | Rust 종합 예제 (로컬 실행 전용) |
| 23 | 마무리 | 다음 단계 안내 |

### s18 더 깊은 Rust — 파트 구성

| Part | 내용 |
|------|------|
| 1 | Drop trait — RAII 자동 소멸자 |
| 2 | From / Into trait — 타입 변환 표준 |
| 3 | Rc\<T\> / Arc\<T\> — 공유 소유권 |
| 4 | RefCell\<T\> — 내부 가변성 |
| 5 | Cow\<'a, B\> — Clone on Write |
| 6 | Pin\<P\> / Unpin — async 기반 |
| 7 | Deref / DerefMut — 역참조 커스터마이징 |
| 8 | PhantomData\<T\> — 제로 크기 마커 |
| 9 | Send / Sync — 스레드 안전성 마커 |
| 10 | Sized / ?Sized — 크기 마커와 DST |
| 11 | 마커 trait 전체 지도 |
| **12** | **Box\<T\> — 힙 포인터 스마트 포인터 (기초 4단계 + 응용 4단계, 그림 9개)** |

---

## 📖 전체 가이드

Java ↔ C++ ↔ Rust 3자 비교, 메모리 다이어그램, 디스패치 분석 등 심화 내용 포함.  
상세한 레퍼런스로 활용하세요.

### 탭별 구성

| 탭 | 내용 |
|----|------|
| 시작하기 | 전체 탭 구성 안내 및 추천 학습 경로 |
| 기초 문법 | 변수, 타입, 함수, 조건문, 반복문, struct, enum, 소유권, 클로저 (11개 섹션) |
| 제네릭·템플릿 | Box\<T\> 비교, 타입 제한, 단형화, 정적/동적 디스패치 (8개 섹션) |
| 문자열·라이프타임 | String vs &str, 메모리 구조, 라이프타임 파라미터 (6개 섹션) |
| trait·디스패치 | 상속 대체, fat pointer, JVM vs Rust 메모리 비교 (8개 섹션) |
| 전체 예제 | Java · Rust 전체 비교 예제 |
| 레퍼런스 | Rust Book · JLS SE21 · JVM Spec SE21 링크 모음 |

---

## 🛠 기술 스택

- **언어**: HTML · CSS · JavaScript (순수 바닐라, 외부 의존성 없음)
- **테마**: VS Code Dark Modern 기반 커스텀 하이라이터
- **SVG 다이어그램**: 인라인 SVG (외부 라이브러리 없음)

### 코드 실행 ([Wandbox](https://wandbox.org) API)

| 가이드 | Java | Rust | C++ |
|--------|------|------|-----|
| 2시간에 배우는 Rust | `openjdk-jdk-22+36` | `rust-1.82.0` | — |
| 전체 가이드 | `openjdk-jdk-22+36` | `rust-1.82.0` | `gcc-13.2.0 (-std=c++17)` |

---

## 📄 License

MIT
