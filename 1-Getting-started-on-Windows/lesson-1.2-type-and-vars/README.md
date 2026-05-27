## C++ types

|Category | Data Type |Description | Introduced / Major Change |
|---------|-----------|------------|---------------------------|
|Integer | int | Standard signed integer. | C++98 (Legacy from C)| |
| |short| Short signed integer (at least 16 bits). | C++98 (Legacy from C)|
| |long,Long signed integer (at least 32 bits). |C++98 (Legacy from C)|
| |long long | Extended long signed integer (at least 64 bits). | C++11|
| |unsigned int / short / long / long long,Unsigned variants of the integers above.,Same as their signed counterparts
|Floating-Point |float |Single-precision floating-point number. |C++98 (Legacy from C)|
| |double |Double-precision floating-point number.| C++98 (Legacy from C)|
| |long double |Extended precision floating-point number. |C++98 (Legacy from C)|
| |"std::float16_t, std::float32_t, std::float64_t, std::float128_t" |Fixed-width floating-point types (optional/extended). |C++23|
|Boolean |bool |Represents true or false. |C++98 |
|Character | char |"Basic character type (usually 8-bit, matches system default)." |C++98 (Legacy from C)|
| |signed char / unsigned char | Explicitly signed/unsigned character types. | C++98 (Legacy from C) |
| |wchar_t |Wide character type (used for larger character sets). |C++98 |
| |char16_t |Character type for UTF-16 character representation. |C++11 |
| |char32_t | Character type for UTF-32 character representation. |C++11|
| |char8_t |Character type for UTF-8 character representation. |C++20|
|Void | void | Represents an empty set of values (absence of type). | C++98 (Legacy from C)|
| Null Pointer | std::nullptr_t |The type of the null pointer literal nullptr. |C++11|
