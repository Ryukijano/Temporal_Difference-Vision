## Learned User Preferences
- Use conda env `tdv` (Python 3.11) with PyTorch 2.10+cu126 for training and eval.
- Install `aiohttp` via conda-forge before `pip install -r requirements.txt --no-deps` to avoid Python 3.11 build failures.
- Log experiments with Weights & Biases; set `HF_HOME` and optionally `HF_TOKEN` for Hugging Face caches.

## Learned Workspace Facts
- Project root: `/scratch/kcwp264/Temporal_Difference-Vision`; GitHub `Ryukijano/Temporal_Difference-Vision`, branch `main`.
- TDV learns joint frame and motion encoders so current embedding plus motion predicts the next frame embedding (no augmentations required).
- Evaluated on semantic segmentation, optical flow, and stereo depth; matches DINO/iBOT on segmentation, surpasses on flow/depth.
- Vendored forks include `repos/ibot-with-online-knn` and `mmsegmentation-tdv` for baselines and downstream eval.
- Model code under `model/cv/tdv/`; paper and site at temporal-difference-vision.github.io.
- PyTorch install: `pip install torch==2.10.0+cu126 torchaudio torchvision --index-url https://download.pytorch.org/whl/cu126`.
- Supports x86_64 and aarch64/GH200 via the cu126 wheel index.
- Parent workspace scratch: `/scratch/kcwp264`; unrelated to `endofm-lv` unless explicitly shared.
