# 🔐 Custom String Encoder & Binary Converter (C Language)

This is a simple C program that **encodes alphabetic characters into a custom symbolic language** using a predefined mapping (`a`, `b`, `c`, `d`) and then converts that encoded output into a **binary string**.

---

## 🎯 Objective

To demonstrate character encoding, symbolic transformation, and binary conversion, along with evaluating **compression effectiveness**.

---

## 🛠️ Features

- 🔄 Converts letters A–Z/a–z into custom codes like `a`, `bb`, `abc`, etc.
- 🔢 Converts each symbol (`a`, `b`, `c`, `d`) into 2-bit binary:
  - `a` → `00`
  - `b` → `01`
  - `c` → `10`
  - `d` → `11`
- 📏 Calculates and compares:
  - Original byte size
  - Final encoded byte size
  - Compression percentage (if any)

---

## 💡 Example

For input `"AZ"`:

- **Encoded:** `aadb`
- **Binary:** `0000110101`
- **Original Size:** 2 bytes
- **Final Size:** 1 byte (rounded)
- **Compression:** Achieved ✔️

---

## 🧩 Mapping Table

| Letter | Code |
|--------|------|
| A      | a    |
| B      | b    |
| C      | c    |
| D      | d    |
| E      | aa   |
| F      | bb   |
| G      | cc   |
| H      | dd   |
| I      | ab   |
| J      | ba   |
| K      | ac   |
| L      | ca   |
| M      | ad   |
| N      | da   |
| O      | bc   |
| P      | cb   |
| Q      | bd   |
| R      | db   |
| S      | cd   |
| T      | dc   |
| U      | aaa  |
| V      | bbb  |
| W      | ccc  |
| X      | ddd  |
| Y      | abc  |
| Z      | adb  |

---

## 🚀 How to Compile & Run

```bash
gcc encoder.c -o encoder
./encoder
```

💡 Make sure you have GCC installed (`sudo apt install build-essential` on Linux)

---

## 📄 License

This project is free and open-source. Feel free to modify or extend it.

> Built with 🧠 in C by Ali Raza
