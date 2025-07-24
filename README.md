# code_generator-python_to_cpp-
LLM model CodeQwen1.5-7B-Chat
# 🔄 Python to C++ Code Generator using CodeQwen1.5

This project uses the [CodeQwen1.5-7B-Chat](https://huggingface.co/Qwen/CodeQwen1.5-7B-Chat) large language model to automatically convert Python code into optimized and high-performance C++ code, specifically tuned for M1 Mac systems.

## 🚀 Features

- Converts Python code to fast and efficient C++.
- Preserves output and logic fidelity.
- Utilizes quantized 4-bit transformer model for performance.
- Runs inference using Hugging Face's Transformers library.
- GPU-compatible (CUDA required).

## 📦 Requirements

Install dependencies using:

```bash
pip install --upgrade torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu124
pip install requests bitsandbytes transformers accelerate openai
```

## 🧠 Model

The script uses the `Qwen/CodeQwen1.5-7B-Chat` transformer model with 4-bit quantization (NF4) to reduce memory usage while maintaining accuracy.

## 🧪 Example

```python
from code_genrator import code_generator

python_code = '''
import time

def calculate(iterations, param1, param2):
    result = 1.0
    for i in range(1, iterations+1):
        j = i * param1 - param2
        result -= (1/j)
        j = i * param1 + param2
        result += (1/j)
    return result
'''

cpp_code = code_generator(python_code)
print(cpp_code)
```

## 📁 Output

The generated C++ code is also saved as a file named `optimized.cpp`.

## 🧹 Resource Management

The script explicitly clears GPU memory and garbage collects models after generation to manage VRAM efficiently.



---

🔧 Maintained by [Your Name]. Contributions welcome!
