[![Cloud Studio Template](https://cs-res.codehub.cn/common/assets/icon-badge.svg)](https://cloudstudio.net/t/10087)

# **[FireRed-Image-Edit-1.0-Fast](https://huggingface.co/spaces/prithivMLmods/FireRed-Image-Edit-1.0-Fast)**

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
