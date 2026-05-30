## C++ types

| Category | Data Type | Description | Introduced / Major Change | Literal Example |
| :--- | :--- | :--- | :--- | :--- |
| **Integer** | `int` | Standard signed integer. | C++98 (Legacy from C) | `42` |
| | `short` | Short signed integer (at least 16 bits). | C++98 (Legacy from C) | `42` |
| | `long` | Long signed integer (at least 32 bits). | C++98 (Legacy from C) | `42L` |
| | `long long` | Extended long signed integer (at least 64 bits). | C++11 | `42LL` |
| | `unsigned int / short / long / long long` | Unsigned variants of the integers above. | Same as signed counterparts | `42U`, `42UL`, `42ULL` |
| **Fixed-Width Integer** | `int8_t / uint8_t` | Signed/unsigned integer guaranteed to be exactly 8 bits. | C++11 (via <cstdint>) | `int8_t(42)` |
| | `int16_t / uint16_t` | Signed/unsigned integer guaranteed to be exactly 16 bits. | C++11 (via <cstdint>) | `int16_t(42)` |
| | `int32_t / uint32_t` | Signed/unsigned integer guaranteed to be exactly 32 bits. | C++11 (via <cstdint>) | `42` / `42U` |
| | `int64_t / uint64_t` | Signed/unsigned integer guaranteed to be exactly 64 bits. | C++11 (via <cstdint>) | `42LL` / `42ULL` |
| **Floating-Point** | `float` | Single-precision floating-point number. | C++98 (Legacy from C) | `3.14f` |
| | `double` | Double-precision floating-point number. | C++98 (Legacy from C) | `3.14` |
| | `long double` | Extended precision floating-point number. | C++98 (Legacy from C) | `3.14L` |
| | `std::float16_t / 32_t / 64_t / 128_t` | Fixed-width floating-point types (optional/extended). | C++23 | `3.14f16`, `3.14f32` |
| **Boolean** | `bool` | Represents true or false. | C++98 | `true` |
| **Character** | `char` | An 8-bit integer type used to represent character codes. | C++98 (Legacy from C) | `'A'` |
| | `signed char / unsigned char` | Explicitly signed/unsigned character types. | C++98 (Legacy from C) | `(signed char)'A'` |
| | `wchar_t` | Wide character type (used for larger character sets). | C++98 | `L'A'` |
| | `char16_t` | Character type for UTF-16 character representation. | C++11 | `u'A'` |
| | `char32_t` | Character type for UTF-32 character representation. | C++11 | `U'A'` |
| | `char8_t` | Character type for UTF-8 character representation. | C++20 | `u8'A'` |
| **Raw Binary** | `std::byte` | Represents a single byte of raw data. No arithmetic allowed. | C++17 | `std::byte{42}` |
| **Void** | `void` | Represents an empty set of values (absence of type). | C++98 (Legacy from C) | None |
| **Null Pointer** | `std::nullptr_t` | The type of the null pointer literal nullptr. | C++11 | `nullptr` |


#### Notes
- The [sizeof()](https://en.cppreference.com/cpp/language/sizeof) operator:
  - It computes the size (in bytes) of your variable/expression
  - It evaluates the type or expression at compile time.
  - For instance, sizeof(my_variable++) will report the size but will not actually increment the variable at runtime.
- Fixed-Width Integers vs. Type Aliases: 
  - Types like int32_t are not new fundamental compiler types
  - They are type aliases managed via the using mechanism behind the scenes, mapping directly to whatever underlying native type satisfies the exact bit-width criteria.
- The Unicode Strategy: 
  - C++ doesn't increase the size of basic char variables to support modern Unicode text. 
  - Instead, it utilizes char8_t, char16_t, and char32_t as strict type barriers, giving the compiler explicit clarity over string data representations.
