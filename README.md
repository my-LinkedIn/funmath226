# funmath226

## Source code

```rust
use list_comprehension::comp;

fn pythagorean(n: u32) -> Vec<(u32, u32, u32)> {
    let triplets: Vec<(u32, u32, u32)> = comp![
        (x, y, z)
        
        , x in 1..=n
        , y in x..=n
        , z in y..=n
        
        , (x as u32).pow(2) + (y as u32).pow(2) == (z as u32).pow(2)
        , (x + y + z) == n
    ];
    
    triplets
}

fn main() {
    for triplet in pythagorean(200) {
        println!("\n{:?}", triplet);
    }
}
```

## Output

```text
(40, 75, 85)
```

## References

  - [Fun Math 226 Problem statement](https://www.linkedin.com/feed/update/urn:li:activity:7206485712089600000?utm_source=share&utm_medium=member_desktop)
  - [Wikipedia entry](https://en.wikipedia.org/wiki/List_comprehension)
  - [list_comprehension Crate](https://crates.io/crates/list_comprehension)
