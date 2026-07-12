# cv-fundamentals

**Cluster:** rust-misc  
**Language:** Rust  
**Source:** [SuperInstance/cv-fundamentals](https://github.com/SuperInstance/cv-fundamentals)

## Intention

See README.

## How It Works

`cv-fundamentals` implements the fundamental algorithms taught in a first course on computer vision:

## What It's For

See README.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (249 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# cv-fundamentals

Computer vision in Rust. From pixels to features.

---

## What This Does

`cv-fundamentals` implements the fundamental algorithms taught in a first course on computer vision:

| Module | What it covers |
|---|---|
| `image` | Grayscale image type with pixel ops, histograms, Otsu thresholding, convolution |
| `filter` | Gaussian/box blur, sharpen, Sobel/Prewitt gradients, Canny edge detection, Laplacian |
| `morphology` | Erosion, dilation, opening, closing, gradient, top-hat, black-hat with configurable structuring elements |
| `feature` | Harris corner detection, Laplacian-of-Gaussian blob detection |
| `segmentation` | Thresholding (binary, range, adaptive), connected-component labelling, watershed |
| `transform` | Hough line detection, affine image transforms with bilinear interpolation |
| `stereo` | Stereo disparity via block matching (SSD), triangulation, depth maps, point clouds |
| `optical_flow` | Lucas-Kanade dense optical flow |

**67 tests · zero unsafe · serde-serializable**

---

## Install

```toml
[dependencies]
cv-fundamentals = "0.1"
```

```bash
cargo add cv-fundamentals
```

### Dependencies

| Crate | Purpose |
|---|---|
| `nalgebra` 0.33 | Vectors and matrices (stereo rig, 3D triangulation) |
| `serde` (derive) | Serialisable image data |

---

## Quick Start

```rust
use cv_fundamentals::{GrayImage, ImageError};
use cv_fundamentals::filter;
use cv_fundamentals::feature;
use cv_fundamentals::segmentation;

// Create an image
let mut img = GrayImage::new(100, 100);
for y in 0..100 {
    for x in 0..50 {
        img.set(x, y, 200.0).unwrap(); // left half bright
    }
}

// Gaussian blur
let blurred = filter::gaussian_blur(&img, 1.5);

// Sobel edge detection
let (magnitude, direction, gx, gy) = filter::sobel(&blurred);

// Canny edges
let edges = filter::canny(&img, 20.0, 60.0);

// Harris corners
let corners = feature::harris_corners(&img, 0.04, 1.0, 3);

// Otsu automatic threshold
let thresh = img.otsu_threshold();
let binary = segmentation::threshold(&img, thresh);

// Connected components
let components = segmentation::connected_components(&binary);
for comp in &components {
    println!("Component {}: area={}, centroid=({:.1}, {:.1})",
        comp.label, comp.area, comp.centroid.0, comp.centroid.1);
}
```

---

## API Reference

### `image` — Grayscale image type

```rust
// Construction
let img = GrayImage::new(width, height);
let img = GrayImage::from_vec(w, h, vec![...f64])?;
let img = GrayImage::from_u8(w, h, &bytes)?;

// Pixel access
img.get(x, y) -> Result<f64, ImageError>
img.get_padded(x: isize, y: isize) -> f64      // zero-padded boundary
img.get_clamped(x: isize, y: isize) -> f64     // clamp-to-edge boundary
img.set(x, y, val) -> Result<(), ImageError>

// Statistics
img.histogram() -> [usize; 256]
img.histogram_normalized() -> [f64; 256]
img.mean() -> f64
img.std_dev() -> f64
img.otsu_threshold() -> f64

// Transforms
img.map(|v| v * 2.0) -> GrayImage
img.zip_with(&other, |a, b| a + b
```
