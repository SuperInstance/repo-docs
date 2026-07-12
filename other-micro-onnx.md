# micro-onnx

## Intention

ONNX export + benchmark pipeline for micro-models. 186x speedup over PyTorch CPU.

## How It Works

```bash
pip install micro-onnx[all]     # everything
pip install micro-onnx           # numpy only (validate without torch/ort)
pip install micro-onnx[export]   # torch + onnx for exporting
pip install micro-onnx[runtime]  # onnxruntime for inference
```

## What It's For

ONNX export + benchmark pipeline for micro-models. 186x speedup over PyTorch CPU.

## Who Would Use It

Machine learning engineers and researchers. Teams deploying or managing ML models.

## Language / Stack

- **Primary language:** Python
- **Technologies mentioned:** PyTorch, ONNX

## Status Assessment

**Status: MODERATE**

Reasonable README (71 lines), includes examples, has benchmarks.

- README length: 108 lines, 4649 characters
- Documented sections: Install, Quick Start, Why ONNX for Micro-Models?, FP32 vs INT8: When Smaller Isn't Faster, opset 17: The Sweet Spot

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**
