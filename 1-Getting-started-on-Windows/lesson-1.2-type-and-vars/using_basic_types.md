# Chapter: Quick Reference: Type Layouts and Usage

This section provides a direct, single-line explanation and minimal code footprint for each fundamental and fixed-width type under the MSVC 64-bit Windows architecture.

---

## 1. Fundamental Types

### `char`

* **Explanation:** Stores a single character or a 1-byte integer using ASCII encoding.
* **Usage:**
```cpp
char letter = 'A';
std::cout << sizeof(letter); // Outputs: 1

```



### `bool`

* **Explanation:** Holds a truth value, explicitly evaluating to either `true` or `false`.
* **Usage:**
```cpp
bool isActive = true;
std::cout << sizeof(isActive); // Outputs: 1

```



### `int`

* **Explanation:** Stores a standard 4-byte signed whole number on 64-bit Windows.
* **Usage:**
```cpp
int score = -42;
std::cout << sizeof(score); // Outputs: 4

```



### `double`

* **Explanation:** Stores an 8-byte high-precision floating-point decimal number.
* **Usage:**
```cpp
double pi = 3.14159;
std::cout << sizeof(pi); // Outputs: 8

```



---

## 2. Fixed-Width Integers (`<cstdint>`)

### `std::int32_t`

* **Explanation:** Guarantees a signed integer of exactly 32 bits (4 bytes) across all platforms.
* **Usage:**
```cpp
std::int32_t modernLargeNum = 2000000;
std::cout << sizeof(modernLargeNum); // Outputs: 4

```



### `std::uint64_t`

* **Explanation:** Guarantees an unsigned large integer of exactly 64 bits (8 bytes).
* **Usage:**
```cpp
std::uint64_t bigCounter = 0xFFFFFFFFFFFFFFFFULL;
std::cout << sizeof(bigCounter); // Outputs: 8

```