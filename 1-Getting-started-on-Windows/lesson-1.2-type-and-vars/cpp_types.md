## C++ types

|Category | Data Type |Description | Introduced / Major Change |
|---------|-----------|------------|---------------------------|
|Integer | int | Standard signed integer. | C++98 (Legacy from C)| |
| |short| Short signed integer (at least 16 bits). | C++98 (Legacy from C)|
| |long,Long signed integer (at least 32 bits). |C++98 (Legacy from C)|
| |long long | Extended long signed integer (at least 64 bits). | C++11|
| |unsigned int / short / long / long long,Unsigned variants of the integers above.,Same as their signed counterparts
|Fixed-Width Integer|	int8_t / uint8_t|	Signed/unsigned integer guaranteed to be exactly 8 bits with no padding. (Usually aliases for signed/unsigned char). |C++11 (via <cstdint>)|
| |int16_t / uint16_t | Signed/unsigned integer guaranteed to be exactly 16 bits. (Usually aliases for short). |C++11 (via <cstdint>)|
| |int32_t / uint32_t | Signed/unsigned integer guaranteed to be exactly 32 bits. (Usually aliases for int). | C++11 (via <cstdint>)|
| |int64_t / uint64_t |Signed/unsigned integer guaranteed to be exactly 64 bits. (Usually aliases for long long).| C++11 (via <cstdint>)|
|Floating-Point |float |Single-precision floating-point number. |C++98 (Legacy from C)|
| |double |Double-precision floating-point number.| C++98 (Legacy from C)|
| |long double |Extended precision floating-point number. |C++98 (Legacy from C)|
| |"std::float16_t, std::float32_t, std::float64_t, std::float128_t" |Fixed-width floating-point types (optional/extended). |C++23|
|Boolean |bool |Represents true or false. |C++98 |
|Character | char |"An 8-bit integer type used to represent character codes (like ASCII). Can be used for arithmetic." |C++98 (Legacy from C)|
| |signed char / unsigned char | Explicitly signed/unsigned character types. | C++98 (Legacy from C) |
| |wchar_t |Wide character type (used for larger character sets). |C++98 |
| |char16_t |Character type for UTF-16 character representation. |C++11 |
| |char32_t | Character type for UTF-32 character representation. |C++11|
| |char8_t |Character type for UTF-8 character representation. |C++20|
|Raw / Native Binary| std::byte| Represents a single byte of raw data. No arithmetic allowed; only bitwise operations.	| C++17|
|Void | void | Represents an empty set of values (absence of type). | C++98 (Legacy from C)|
| Null Pointer | std::nullptr_t |The type of the null pointer literal nullptr. |C++11|


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
