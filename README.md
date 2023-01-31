# bmatrix
A boolean matrix implementation in Rust.  The implementation uses bitwise operations to represent 
the boolean values of matrix.  The idea is to explore unit testing in Rust using the CLion IDE and compare with testing 
Go and C++ code in the Jetbrains IDES.

## Sources
```rust
pub struct Matrix{
        pub n: usize,
        pub m: usize,
        bits:Vec<u64>,
}
```

The bits are stored in  a vector of u64.  The matrix is represented as a vector of rows.  Each row is represented as a u64.
The bits are stored in the u64 from left to right.  
```rust
pub fn NewMatrix(n,m:usize) -> Matrix{
    let size = getvectorsize(n * m);
    let mut avector = Vec::new();
    avector.resize(size,0u64);
    let A = Matrix {
        n,
        m,
        bits: avector,
    };
    return A;
}
```


