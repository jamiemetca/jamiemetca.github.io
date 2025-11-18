[Back](README)

2025/09/24

# Long long & Unsigned long long

The long long is a built in data type used to store integers.
It's an extended version long data type and is guaranteed to be at least 64 bits, but can be larger depending on the system architecture.
It is signed by default.

Suffix
---

Signed: LL or ll


Unsigned: ULL or ull

Format specifier
---
Signed: %lli or %lld
Unsigned: %llu

Example
---
```C
#include <stdio.h>

int main() {
    // --- Signed long long example ---
    // A signed long long can hold both positive and negative values.
    // The 'LL' suffix is used to denote a long long literal.
    long long signed_max = 9223372036854775807LL;
    long long signed_min = -9223372036854775807LL - 1;

    printf("Signed long long range:\n");
    printf("Maximum value: %lld\n", signed_max);
    printf("Minimum value: %lld\n", signed_min);
    printf("\n");

    // --- Unsigned long long example ---
    // An unsigned long long can only hold non-negative values (0 and above).
    // The 'ULL' suffix is used for unsigned long long literals.
    unsigned long long unsigned_max = 18446744073709551615ULL;
    unsigned long long unsigned_min = 0ULL;

    printf("Unsigned long long range:\n");
    printf("Maximum value: %llu\n", unsigned_max);
    printf("Minimum value: %llu\n", unsigned_min);

    return 0;
}
```

> [!NOTE]
> 
> Read about why the minimum value is set like this:
> [here](./Negative_numbers.md)
>
> long long signed_min = -9223372036854775807LL - 1;
