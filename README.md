## How to run on Mac by uv ?

## issue
✗ uv run mineru -p demo/pdfs/demo1.pdf -o demo/pdfs/demo1_output
× No solution found when resolving dependencies:
╰─▶ Because mineru[pipeline-old-linux] depends on rapid-table==1.0.3 and mineru[all] depends on
rapid-table>=1.0.5,<2.0.0, we can conclude that mineru[all] and mineru[pipeline-old-linux] are
incompatible.
And because your project requires mineru[all] and mineru[pipeline-old-linux], we can conclude that
your project's requirements are unsatisfiable.

### How to fix 
remove  the pipeline_old_linux in pyproject.toml

##  Detail steps to run 

uv venv --python=3.10 .venv

uv pip install -e ".[core]"

uv run  mineru -p demo/pdfs/demo1.pdf -o demo/pdfs/demo1_output

## Log
 MinerU git:(master) ✗ uv venv --python=3.10 .venv
Using CPython 3.10.17
Creating virtual environment at: .venv
Activate with: source .venv/bin/activate





➜  MinerU git:(master) ✗ uv pip install -e ".[core]"

Resolved 126 packages in 5.36s
      Built mineru
Prepared 1 package in 354ms
Installed 126 packages in 1.13s
 + accelerate==1.9.0
 + aiofiles==24.1.0
 + albucore==0.0.24
 + albumentations==2.0.8
 + annotated-types==0.7.0
 + antlr4-python3-runtime==4.9.3
 + anyio==4.9.0
 + boto3==1.39.9
 + botocore==1.39.9
 + brotli==1.1.0
 + certifi==2025.7.14
 + cffi==1.17.1
 + charset-normalizer==3.4.2
 + click==8.2.1
 + coloredlogs==15.0.1
 + colorlog==6.9.0
 + contourpy==1.3.2
 + cryptography==45.0.5
 + cycler==0.12.1
 + dill==0.4.0
 + distro==1.9.0
 + doclayout-yolo==0.0.4
 + exceptiongroup==1.3.0
 + fast-langdetect==0.2.5
 + fastapi==0.116.1
 + fasttext-predict==0.9.2.4
 + ffmpy==0.6.0
 + filelock==3.18.0
 + flatbuffers==25.2.10
 + fonttools==4.59.0
 + fsspec==2025.7.0
 + ftfy==6.3.1
 + gradio==5.38.0
 + gradio-client==1.11.0
 + gradio-pdf==0.0.22
 + groovy==0.1.2
 + h11==0.16.0
 + hf-xet==1.1.5
 + httpcore==1.0.9
 + httpx==0.28.1
 + huggingface-hub==0.33.4
 + humanfriendly==10.0
 + idna==3.10
 + jinja2==3.1.6
 + jiter==0.10.0
 + jmespath==1.0.1
 + json-repair==0.47.8
 + kiwisolver==1.4.8
 + loguru==0.7.3
 + markdown-it-py==3.0.0
 + markupsafe==3.0.2
 + matplotlib==3.10.3
 + mdurl==0.1.2
 + mineru==2.1.1 
 + modelscope==1.28.0
 + mpmath==1.3.0
 + networkx==3.4.2
 + numpy==2.2.6
 + omegaconf==2.3.0
 + onnxruntime==1.22.1
 + openai==1.97.0
 + opencv-python==4.12.0.88
 + opencv-python-headless==4.12.0.88
 + orjson==3.11.0
 + packaging==25.0
 + pandas==2.3.1
 + pdfminer-six==20250506
 + pdftext==0.6.3
 + pillow==11.3.0
 + protobuf==6.31.1
 + psutil==7.0.0
 + py-cpuinfo==9.0.0
 + pyclipper==1.3.0.post6
 + pycparser==2.22
 + pydantic==2.11.7
 + pydantic-core==2.33.2
 + pydantic-settings==2.10.1
 + pydub==0.25.1
 + pygments==2.19.2
 + pyparsing==3.2.3
 + pypdf==5.8.0
 + pypdfium2==4.30.0
 + python-dateutil==2.9.0.post0
 + python-dotenv==1.1.1
 + python-multipart==0.0.20
 + pytz==2025.2
 + pyyaml==6.0.2
 + rapid-table==1.0.5
 + regex==2024.11.6
 + reportlab==4.4.2
 + requests==2.32.4
 + rich==14.0.0
 + robust-downloader==0.0.2
 + ruff==0.12.4
 + s3transfer==0.13.1
 + safehttpx==0.1.6
 + safetensors==0.5.3
 + scipy==1.15.3
 + seaborn==0.13.2
 + semantic-version==2.10.0
 + setuptools==80.9.0
 + shapely==2.1.1
 + shellingham==1.5.4
 + simsimd==6.5.0
 + six==1.17.0
 + sniffio==1.3.1
 + starlette==0.47.1
 + stringzilla==3.12.5
 + sympy==1.14.0
 + thop==0.1.1.post2209072238
 + tokenizers==0.21.2
 + tomlkit==0.13.3
 + torch==2.7.1
 + torchvision==0.22.1
 + tqdm==4.67.1
 + transformers==4.53.2
 + typer==0.16.0
 + typing-extensions==4.14.1
 + typing-inspection==0.4.1
 + tzdata==2025.2
 + ultralytics==8.3.168
 + ultralytics-thop==2.0.14
 + urllib3==2.5.0
 + uvicorn==0.35.0
 + wcwidth==0.2.13
 + websockets==15.0.1






➜  MinerU git:(master) ✗ uv run  mineru -p demo/pdfs/demo1.pdf -o demo/pdfs/demo1_output
Uninstalled 2 packages in 15ms
Installed 2 packages in 8ms
2025-07-20 19:11:46.971 | WARNING  | mineru.backend.vlm.predictor:<module>:35 - sglang is not installed. If you are not using sglang, you can ignore this warning.
2025-07-20 19:12:18.036 | INFO     | mineru.backend.pipeline.pipeline_analyze:doc_analyze:124 - Batch 1/1: 13 pages/13 pages
2025-07-20 19:12:18.038 | INFO     | mineru.backend.pipeline.model_init:__init__:137 - DocAnalysis init, this may take some times......
Fetching 1 files: 100%|████████████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:00<00:00, 23172.95it/s]
Fetching 7 files: 100%|████████████████████████████████████████████████████████████████████████████████████████████████████████████| 7/7 [00:00<00:00, 21137.60it/s]
Fetching 1 files: 100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:00<00:00, 2584.29it/s]
Fetching 1 files: 100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:00<00:00, 3095.43it/s]
Fetching 1 files: 100%|████████████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:00<00:00, 12826.62it/s]
Fetching 1 files: 100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:00<00:00, 1314.01it/s]
2025-07-20 19:12:28.700 | INFO     | mineru.backend.pipeline.model_init:__init__:182 - DocAnalysis init done!
2025-07-20 19:12:28.700 | INFO     | mineru.backend.pipeline.pipeline_analyze:custom_model_init:64 - model init cost: 10.662137985229492
Layout Predict: 100%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████| 13/13 [00:02<00:00,  4.96it/s]
MFD Predict: 100%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 13/13 [00:03<00:00,  3.32it/s]
MFR Predict: 100%|████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 126/126 [00:07<00:00, 17.27it/s]
Fetching 1 files: 100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:00<00:00, 2644.58it/s]
Fetching 1 files: 100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:00<00:00, 9098.27it/s]
OCR-det ch: 100%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 69/69 [00:53<00:00,  1.28it/s]
Fetching 1 files: 100%|████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:00<00:00, 17189.77it/s]
Table Predict: 100%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 5/5 [00:14<00:00,  2.89s/it]
Fetching 2 files: 100%|████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 2/2 [00:00<00:00, 10205.12it/s]
Processing pages: 100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 13/13 [00:08<00:00,  1.52it/s]
OCR-rec Predict: 100%|████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 7/7 [00:01<00:00,  6.60it/s]
2025-07-20 19:14:02.904 | INFO     | mineru.cli.common:_process_output:156 - local output dir is demo/pdfs/demo1_output/demo1/auto