![Activation Functions](https://cdn.discordapp.com/attachments/749301198099841114/863353727192924170/GitHub_PageBanner.png)

# Table of Contents
|**Contents**|
|:-|
|[Informations](#some-informations)|
|Documentation [(GitHub)](#documentation) [(docs.rs)](https://docs.rs/activation_functions/0.1.0/activation_functions/)|

# Some informations:
|**Name**|**Value**|
|-|-|
|Language|Rust|
|Programer|SnefDen|
|version|0.1.0|
|last update|10.07.2021|

# Documentation
## Table of Contents
|               |**sigmoid**              |**binary step**      |**tanh**           |**rectified linear unit**|**sigmoid linear unit**|**gaussian**               |
|:--------------|:-----------------------:|:-------------------:|:-----------------:|:-----------------------:|:---------------------:|:-------------------------:|
|[**f32**](#f32)|[f32::sigmoid](#sigmoidx)|[f32::bstep](#bstepx)|[f32::tanh](#tanhx)|[f32::relu](#relux)      |[f32::silu](#silux)    |[f32::gaussian](#gaussianx)|
|[**f64**](#f64)|[f64::sigmoid](#sigmoidy)|[f64::bstep](#bstepy)|[f64::tanh](#tanhy)|[f64::relu](#reluy)      |[f64::silu](#siluy)    |[f64::gaussian](#gaussiany)|

# f32
## sigmoid(x):
* [Informations](#informations-f32sigmoid)
* [Example](#example-f32sigmoid)
* [Implementation](#implementation-f32sigmoid)
### Informations (f32::sigmoid):
#### Parameter:
```rust
// variable stands for parameter

let x:f32;          // float32

```
#### Used inside:
```rust
//      variables
let x:f32;          // parameter
let result:f32;     // return variable

//      functions
std::f32::consts::E.powf();

```
#### Return:
```rust
// variable stands for return

let result:f32;     // float32

```
### Example (f32::sigmoid):
```rust
let x:f32   = 0.5;
let answer  = sigmoid(x);

println!("sigmoid({}) => {}",x,answer);
```
that would print out the answer and the given x-value in this format

`sigmoid(0.5) => 0.62245935`
### Implementation (f32::sigmoid):
```rust
pub fn sigmoid(x:f32) -> f32 {
    1 as f32 / (1 as f32 + std::f32::consts::E.powf(-x))
}
```
___
## bstep(x):
* [Informations](#informations-f32bstep)
* [Example](#example-f32bstep)
* [Implementation](#implementation-f32bstep)
### Informations (f32::bstep):
#### Parameter:
```rust
// variable stands for parameter

let x:f32;          // float32

```
#### Used inside:
```rust
//      variables
let x:f32;          // parameter
let result:f32;     // return variable

//      functions
std::f32::consts::E.powf();

```
#### Return:
```rust
// variable stands for return

let result:f32;     // float32

```
### Example (f32::bstep):
```rust
let x:f32   = 0.5;
let answer  = bstep(x);

println!("bstep({}) => {}",x,answer);
```
that would print out the answer and the given x-value in this format

`bstep(0.5) => 1.0`
### Implementation (f32::bstep):
```rust
pub fn bstep(x:f32) -> f32 {
    if x<0 as f32 {
        0 as f32
    } else {
        1 as f32
    }
}
```
___
## tanh(x):
* [Informations](#informations-f32tanh)
* [Example](#example-f32tanh)
* [Implementation](#implementation-f32tanh)
### Informations (f32::tanh):
#### Parameter:
```rust
// variable stands for parameter

let x:f32;          // float32

```
#### Used inside:
```rust
//      variables
let x:f32;          // parameter
let result:f32;     // return variable

//      functions
std::f32::consts::E.powf();

```
#### Return:
```rust
// variable stands for return

let result:f32;     // float32

```
### Example (f32::tanh):
```rust
let x:f32   = 0.5;
let answer  = tanh(x);

println!("tanh({}) => {}",x,answer);
```
that would print out the answer and the given x-value in this format

`tanh(0.5) => 0.46211714`
### Implementation (f32::tanh):
```rust
pub fn tanh(x:f32) -> f32 {
    (std::f32::consts::E.powf(x) - std::f32::consts::E.powf(-x)) / (std::f32::consts::E.powf(x) + std::f32::consts::E.powf(-x))
}
```
___
## relu(x):
* [Informations](#informations-f32relu)
* [Example](#example-f32relu)
* [Implementation](#implementation-f32relu)
### Informations (f32::relu):
#### Parameter:
```rust
// variable stands for parameter

let x:f32;          // float32

```
#### Used inside:
```rust
//      variables
let x:f32;          // parameter
let result:f32;     // return variable

//      functions
std::f32::consts::E.powf();

```
#### Return:
```rust
// variable stands for return

let result:f32;     // float32

```
### Example (f32::relu):
```rust
let x:f32   = 0.5;
let answer  = relu(x);

println!("relu({}) => {}",x,answer);
```
that would print out the answer and the given x-value in this format

`relu(0.5) => 1.0`
### Implementation (f32::tanh):
```rust
pub fn relu(x:f32) -> f32 {
    if x<=0 as f32 {
        0 as f32
    } else {
        1 as f32
    }
}
```
___
## silu(x):
* [Informations](#informations-f32silu)
* [Example](#example-f32silu)
* [Implementation](#implementation-f32silu)
### Informations (f32::silu):
#### Parameter:
```rust
// variable stands for parameter

let x:f32;          // float32

```
#### Used inside:
```rust
//      variables
let x:f32;          // parameter
let result:f32;     // return variable

//      functions
std::f32::consts::E.powf();

```
#### Return:
```rust
// variable stands for return

let result:f32;     // float32

```
### Example (f32::silu):
```rust
let x:f32   = 0.5;
let answer  = silu(x);

println!("silu({}) => {}",x,answer);
```
that would print out the answer and the given x-value in this format

`silu(0.5) => 0.31122968`
### Implementation (f32::silu):
```rust
pub fn silu(x:f32) -> f32 {
    x / (1 as f32 + std::f32::consts::E.powf(-x))
}
```
___
## gaussian(x):
* [Informations](#informations-f32gaussian)
* [Example](#example-f32gaussian)
* [Implementation](#implementation-f32gaussian)
### Informations (f32::gaussian):
#### Parameter:
```rust
// variable stands for parameter

let x:f32;          // float32

```
#### Used inside:
```rust
//      variables
let x:f32;          // parameter
let result:f32;     // return variable

//      functions
std::f32::consts::E.powf();

```
#### Return:
```rust
// variable stands for return

let result:f32;     // float32

```
### Example (f32::gaussian):
```rust
let x:f32   = 0.5;
let answer  = gaussian(x);

println!("gaussian({}) => {}",x,answer);
```
that would print out the answer and the given x-value in this format

`gaussian(0.5) => 0.7788008`
### Implementation (f32::gaussian):
```rust
pub fn gaussian(x:f32) -> f32 {
    std::f32::consts::E.powf(-(x*x))
}
```
___
# f64

## sigmoid(y):
* [Informations](#informations-f64sigmoid)
* [Example](#example-f64sigmoid)
* [Implementation](#implementation-f64sigmoid)
### Informations (f64::sigmoid):
#### Parameter:
```rust
// variable stands for parameter

let x:f64;          // float64

```
#### Used inside:
```rust
//      variables
let x:f64;          // parameter
let result:f64;     // return variable

//      functions
std::f64::consts::E.powf();

```
#### Return:
```rust
// variable stands for return

let result:f64;     // float64

```
### Example (f64::sigmoid):
```rust
let x:f64   = 0.5;
let answer  = sigmoid(x);

println!("sigmoid({}) => {}",x,answer);
```
that would print out the answer and the given x-value in this format

`sigmoid(0.5) => 0.62245935`
### Implementation (f64::sigmoid):
```rust
pub fn sigmoid(x:f64) -> f64 {
    1 as f64 / (1 as f64 + std::f64::consts::E.powf(-x))
}
```
___
## bstep(y):
* [Informations](#informations-f64bstep)
* [Example](#example-f64bstep)
* [Implementation](#implementation-f64bstep)
### Informations (f64::bstep):
#### Parameter:
```rust
// variable stands for parameter

let x:f64;          // float64

```
#### Used inside:
```rust
//      variables
let x:f64;          // parameter
let result:f64;     // return variable

//      functions
std::f64::consts::E.powf();

```
#### Return:
```rust
// variable stands for return

let result:f64;     // float64

```
### Example (f64::bstep):
```rust
let x:f64   = 0.5;
let answer  = bstep(x);

println!("bstep({}) => {}",x,answer);
```
that would print out the answer and the given x-value in this format

`bstep(0.5) => 1.0`
### Implementation (f64::bstep):
```rust
pub fn bstep(x:f64) -> f64 {
    if x<0 as f64 {
        0 as f64
    } else {
        1 as f64
    }
}
```
___
## tanh(y):
* [Informations](#informations-f64tanh)
* [Example](#example-f64tanh)
* [Implementation](#implementation-f64tanh)
### Informations (f64::tanh):
#### Parameter:
```rust
// variable stands for parameter

let x:f64;          // float64

```
#### Used inside:
```rust
//      variables
let x:f64;          // parameter
let result:f64;     // return variable

//      functions
std::f64::consts::E.powf();

```
#### Return:
```rust
// variable stands for return

let result:f64;     // float64

```
### Example (f64::tanh):
```rust
let x:f64   = 0.5;
let answer  = tanh(x);

println!("tanh({}) => {}",x,answer);
```
that would print out the answer and the given x-value in this format

`tanh(0.5) => 0.46211714`
### Implementation (f64::tanh):
```rust
pub fn tanh(x:f64) -> f64 {
    (std::f64::consts::E.powf(x) - std::f64::consts::E.powf(-x)) / (std::f64::consts::E.powf(x) + std::f64::consts::E.powf(-x))
}
```
___
## relu(y):
* [Informations](#informations-f32relu)
* [Example](#example-f32relu)
* [Implementation](#implementation-f32relu)
### Informations (f32::relu):
#### Parameter:
```rust
// variable stands for parameter

let x:f32;          // float32

```
#### Used inside:
```rust
//      variables
let x:f32;          // parameter
let result:f32;     // return variable

//      functions
std::f32::consts::E.powf();

```
#### Return:
```rust
// variable stands for return

let result:f32;     // float32

```
### Example (f32::relu):
```rust
let x:f32   = 0.5;
let answer  = relu(x);

println!("relu({}) => {}",x,answer);
```
that would print out the answer and the given x-value in this format

`relu(0.5) => 1.0`
### Implementation (f32::tanh):
```rust
pub fn relu(x:f32) -> f32 {
    if x<=0 as f32 {
        0 as f32
    } else {
        1 as f32
    }
}
```
___
## silu(y):
* [Informations](#informations-f64silu)
* [Example](#example-f64silu)
* [Implementation](#implementation-f64silu)
### Informations (f64::silu):
#### Parameter:
```rust
// variable stands for parameter

let x:f64;          // float64

```
#### Used inside:
```rust
//      variables
let x:f64;          // parameter
let result:f64;     // return variable

//      functions
std::f64::consts::E.powf();

```
#### Return:
```rust
// variable stands for return

let result:f64;     // float64

```
### Example (f64::silu):
```rust
let x:f64   = 0.5;
let answer  = silu(x);

println!("silu({}) => {}",x,answer);
```
that would print out the answer and the given x-value in this format

`silu(0.5) => 0.31122968`
### Implementation (f64::silu):
```rust
pub fn silu(x:f64) -> f64 {
    x / (1 as f64 + std::f64::consts::E.powf(-x))
}
```
___
## gaussian(y):
* [Informations](#informations-f64gaussian)
* [Example](#example-f64gaussian)
* [Implementation](#implementation-f64gaussian)
### Informations (f64::gaussian):
#### Parameter:
```rust
// variable stands for parameter

let x:f64;          // float64

```
#### Used inside:
```rust
//      variables
let x:f64;          // parameter
let result:f64;     // return variable

//      functions
std::f64::consts::E.powf();

```
#### Return:
```rust
// variable stands for return

let result:f64;     // float64

```
### Example (f64::gaussian):
```rust
let x:f64   = 0.5;
let answer  = gaussian(x);

println!("gaussian({}) => {}",x,answer);
```
that would print out the answer and the given x-value in this format

`gaussian(0.5) => 0.7788008`
### Implementation (f64::gaussian):
```rust
pub fn gaussian(x:f64) -> f64 {
    std::f64::consts::E.powf(-(x*x))
}
```
___

