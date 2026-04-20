# Java 개발자를 위한 Rust 정리

Java 개발자를 위한 단계별 Rust 전환 가이드입니다.  
Java 21 · Rust 2021 (rustc 1.75) · Go 1.21 · C++17 기준으로 작성됐으며,  
모든 예제는 복사 즉시 컴파일 · 실행 가능합니다.

## 🔗 GitHub Pages

**[hans9500.github.io/rust-guide-for-java-developer](https://hans9500.github.io/rust-guide-for-java-developer)**

---

## 📋 구성 — 탭별 학습 순서

### 시작하기
- 전체 탭 구성 안내 및 추천 학습 경로

---

### 기초 문법 (11개 섹션)

| 주제 | 내용 |
|------|------|
| 변수 · 상수 · 불변성 | `let` · `const` · 불변 기본값 |
| 기본 타입 | i32/u32/f64/bool/char · Java 비교 |
| 함수 정의 | `fn` · 반환값 · 표현식 반환 |
| 조건문 | `if`는 표현식 · Java `? :` 대응 |
| loop · while · for | `break value` · range 기반 for |
| struct · impl | 데이터와 메서드 분리 · Java 클래스 대응 |
| 접근 제한자 | `pub` · private · `pub(crate)` |
| enum · Option · Result | ADT · null 대체 · 예외 없는 에러 처리 |
| 타입 시스템 | 타입 추론 · `as/From/Into` · 숫자 타입 |
| 소유권 · 빌림 | move · `&` · `&mut` · Drop · Clone |
| 클로저 · 컬렉션 · Iterator | Fn/FnMut/FnOnce · Vec · HashMap · Iterator 체인 |

---

### 제네릭 · 템플릿 (8개 섹션)

| 섹션 | 내용 |
|------|------|
| ① 왜 제네릭이 필요한가 | 타입마다 중복 코드 문제 · 세 언어 비교 |
| ② Box\<T\> 핵심 차이 | Template Instantiation vs Type Erasure vs Monomorphization |
| ③ 함수 템플릿 · 제네릭 메서드 | 제네릭 메서드 비교 |
| ④ 타입 제한 | `static_assert` · `extends` · `trait bound` |
| ⑤ Primitive · 메모리 | Boxing 비교 · 스택/힙 구조 |
| ⑥ 런타임 타입 정보 | `typeid` · `TypeId` · Type Erasure |
| ⑦ Stack\<T\> 실전 | 안전 구현 비교 |
| ⑧ Rust 정적 vs 동적 | `&dyn` · Fat Pointer |

---

### 문자열 · 라이프타임 (6개 섹션)

| 섹션 | 내용 |
|------|------|
| ① String vs &str | 소유권과 뷰 · Java String 비교 |
| ② 메모리 구조 | 실제 저장 방식 · 스택/힙 |
| ③ 함수 파라미터 | `&str` vs `String` 선택 기준 |
| ④ 구조체 필드와 라이프타임 | 참조 필드 · 명시 필요 이유 |
| ⑤ 라이프타임 파라미터 | 컴파일러와의 계약 · 생략 규칙 |
| ⑥ 실전 | 라이프타임 + 트레이트 바운드 조합 |

---

### trait · 디스패치 (8개 섹션)

| 섹션 | 내용 |
|------|------|
| ① 상속 대체 방법 | Rust · Go · C++ 비교 |
| ② impl 블록 | Go 리시버 · Java 클래스 메서드 대응 |
| ③ trait 기본 | interface + 추가 기능 |
| 4개 언어 비교 | Java · Rust · Go · C++ |
| Go interface vs Rust dyn | 구조적 vs 명시적 타이핑 |
| 상속 대신 컴포지션 | `extends` vs 필드 포함 |
| fat pointer 구조 | JVM vs Rust 메모리 비교 |
| 정적 vs 동적 디스패치 | 메모리 비교 |

---

### 전체 예제
- Java · Rust 전체 비교 예제 1개 (Main.java vs main.rs)

---

### 레퍼런스
- Rust Book · JLS SE21 · JVM Spec SE21 링크 모음

---

## 🛠 기술 스택

- **언어**: HTML · CSS · JavaScript (순수 바닐라)
- **코드 실행**: [Wandbox](https://wandbox.org) API
  - Java: `openjdk-jdk-22+36`
  - Rust: `rust-1.82.0`
  - C++: `gcc-13.2.0 (-std=c++17)`
- **테마**: VS Code Dark Modern 기반 커스텀 하이라이터

## 📄 License

MIT
