2025/09/19

# Pointers to an array

[Back](./README.md)

```c
int (*grid)[26] = (int(*)[26]) calloc(rows * 26, sizeof(int));
```

The core of this code's functionality lies in its use of a specific type of pointer: a **pointer to an array**. This allows a one-dimensional block of memory to be treated as a two-dimensional grid, making it easier to manage a spreadsheet-like data structure.

-----

### 1\. The `int (*grid)[26]` Declaration

This is the most critical line. It defines a variable named `grid` that is a **pointer to an array of 26 integers**.

  - **`*grid`**: This part identifies `grid` as a pointer. The parentheses `()` are essential; without them, the declaration would mean something completely different (an array of pointers).
  - **`[26]`**: This specifies that the pointer `grid` points to a data type that is an array containing exactly 26 elements.
  - **`int`**: The elements of the array are integers.

This means that `grid` doesn't point to a single integer; it points to a "chunk" of memory that is `26 * sizeof(int)` bytes long.

-----

### 2\. Pointers and Dynamic Memory Allocation

**`calloc`** is used to allocate a single, contiguous block of memory.

```c
int (*grid)[26] = (int(*)[26]) calloc(rows * 26, sizeof(int));
```

  - **`calloc`** allocates a flat, one-dimensional block of memory. If `rows` is 2, the memory is a single chunk of `52 * sizeof(int)` bytes.
  - The cast **`(int(*)[26])`** is a type cast that tells the compiler to treat the starting address of this flat memory block as a pointer to a row (an array of 26 integers).
  - The pointer `grid` is then assigned this starting address.

This setup allows you to use `grid` as a pointer to the "first row" of your spreadsheet.

-----

### 3\. Pointer Arithmetic in Action

Because `grid` is a pointer to an array of 26 integers, the compiler understands how to perform pointer arithmetic to navigate the "rows" and "columns."

  - **Row Navigation**: When you write `grid[1]`, the compiler doesn't just move forward one memory address. It moves forward by the **size of the type `grid` points to**, which is `sizeof(int[26])` or `26 * sizeof(int)`. This places the pointer at the beginning of the second row of the spreadsheet.

      - `grid[0]` points to the first row (offset 0).
      - `grid[1]` points to the second row (offset `26 * sizeof(int)`).
      - `grid[n]` points to the `(n+1)`-th row.

  - **Column Navigation**: Once at a specific row, standard array access is used for columns. For example, `grid[1][5]` first jumps to the second row and then moves forward 5 integer-sized steps to access the sixth element in that row.

This is a powerful abstraction that allows simple `grid[row][column]` syntax to perform complex memory calculations under the hood, making the code both efficient and easy to read.