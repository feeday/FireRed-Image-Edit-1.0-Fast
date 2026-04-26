[![Cloud Studio Template](https://cs-res.codehub.cn/common/assets/icon-badge.svg)](https://cloudstudio.net/t/10087)

# **[FireRed-Image-Edit-1.0-Fast](https://huggingface.co/spaces/prithivMLmods/FireRed-Image-Edit-1.0-Fast)**

FireRed-Image-Edit-1.0-Fast is a high-performance, AI-driven image editing application that utilizes advanced diffusers and the QwenImageEditPlusPipeline for precise, prompt-based image modifications. Incorporating rapid Transformer configurations, the application provides an interactive Gradio web interface with a custom Soft Blue theme for an aesthetically pleasing user experience. Users can leverage powerful flow match euler discrete schedulers to seamlessly edit visual content by submitting an original image alongside descriptive textual instructions. The application operates entirely in Python, efficiently utilizing CUDA capabilities for accelerated machine learning computations, and serves as a fast, state-of-the-art solution for automated, text-guided image manipulation without complex manual editing software.

<img width="1918" height="1753" alt="Screenshot 2026-03-21 at 15-27-14 FireRed Image Edit 1 0 Fast - a Hugging Face Space by prithivMLmods" src="https://github.com/user-attachments/assets/c88a82b6-f877-4312-94e3-fd3119b03318" />

## Features

* **Advanced Diffusers Pipeline:** Utilizes the QwenImageEditPlusPipeline integrated with FlowMatchEulerDiscreteScheduler for high-fidelity image editing based on user prompts.
* **Rapid AI Architecture:** Employs optimized transformer structures designed for fast inference, providing quick iterations and real-time responsiveness.
* **Custom Themed Interface:** Provides an interactive, user-friendly Gradio web interface styled with a custom Soft OrangeRed theme for an optimal visual layout.
* **Hardware Acceleration:** Automatically identifies and leverages CUDA-compatible devices for optimal computational performance, rendering complex edits rapidly.

## Installation

### 1. Clone

```bash
git clone https://github.com/feeday/FireRed-Image-Edit-1.0-Fast.git
cd FireRed-Image-Edit-1.0-Fast
```

### 2. Pip 

```bash
pip install -r pre-requirements.txt
pip install "safetensors==0.8.0rc0" -i https://pypi.org/simple/
pip install -r requirements.txt
pip install "gradio[mcp]"
```

### 3. Del 

```bash
rm -rf ~/.cache/pip
rm -rf ~/.cache/huggingface/hub/tmp*
```

#### .vscode/preview.yml

```
# .vscode/preview.yml
autoOpen: false # 打开工作空间时是否自动开启所有应用的预览
apps:
  # 以 hello-world.js 为例
  - port: 7860 # 应用的端口
    run: python demo.py
    root: ./ # 应用的启动目录
    name: my-first-app # 应用名称
    description: 我的第一个 App。 # 应用描述
    autoOpen: false # 打开工作空间时是否自动开启预览（优先级高于根级 autoOpen）
```

## How to Run

To start the application and load the local server, run the main Python script:

```bash
python demo.py
```

## Project Structure

* `app.py`: The main entry point script containing the custom Gradio interface setup, pipeline initialization, and inference logic.
* `qwenimage/`: Core directory housing the transformer and processor modules crucial for the underlying image manipulation techniques.
* `requirements.txt`: The primary file listing Python library requirements needed to operate the application correctly.
* `pre-requirements.txt`: A list containing earlier or auxiliary dependency specifications.
* `examples/`: Directory dedicated to storing sample images and expected outputs to verify application functionality.
* `LICENSE.txt`: The legal text detailing the licensing constraints and permissions.

## Workflow

1. Navigate to the local server URL provided after executing the application.
2. Upload a source image that you wish to edit into the input module.
3. Provide a clear, detailed text prompt describing the exact modifications you want the AI to perform on the image.
4. The system executes the QwenImageEditPlusPipeline via the underlying rapid transformers to compute the altered visual output.
5. Retrieve and save the edited image directly from the interface.

## License

This project is open-source. For detailed terms and conditions, refer to the included `LICENSE.txt` file within the repository.

## Contributing

Community contributions are encouraged. Please submit an issue for bug reports or create a Pull Request to propose features, optimize inference times, or improve the user interface.
