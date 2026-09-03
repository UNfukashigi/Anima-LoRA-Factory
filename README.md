# Anima LoRA Factory 🚀

<img src="https://github.com/UNfukashigi/Anima-LoRA-Factory/blob/main/image1.png">

Anima LoRA Factory は、次世代画像生成モデル Anima の LoRA 学習を、プログラミングの知識なしで誰でも簡単に行えるように設計された GUI ツールです。 特に最新の NVIDIA RTX 50シリーズ (Blackwell / sm_120) への対応や、複雑な環境構築の自動化にこだわっています。

> Anima LoRA Factory is a user-friendly GUI tool designed for training LoRAs for the next-generation Anima diffusion models. It simplifies the complex setup process and offers native support for the latest NVIDIA RTX 50 Series (Blackwell / sm_120) GPUs.

## 📥 ダウンロード / Download

👉 **[最新版をダウンロード / Download Latest Release](https://github.com/UNfukashigi/Anima-LoRA-Factory/releases/latest)**

▼SDXLバージョンも公開しています。- SDXL version is also available.<br>
[https://github.com/UNfukashigi/SDXL-LoRA-Factory](https://github.com/UNfukashigi/SDXL-LoRA-Factory)

▼詳しい使い方については、以下の記事をご覧ください。- For detailed instructions on how to use it, please see the article below.<br>
[https://x.com/UNfukashigi/status/2045744319433490449](https://x.com/UNfukashigi/status/2045744319433490449)

---

## 🌟 主な機能 / Key Features

### ✅全自動環境構築 / Auto Setup

start.bat を実行するだけで、必要な学習エンジン (sd-scripts) やハードウェアに最適な PyTorch を自動的にセットアップします。<br>
Just run `start.bat` to automatically set up the required training engine (`sd-scripts`) and the best PyTorch version for your hardware.

### ✅ビジュアルタグエディタ / Visual Tag Editor

画像を見ながら直感的にキャプション（タグ）を編集可能。WD14 Tagger による自動タグ付け機能も内蔵しています。 トリガーワードも簡単に追加できます。<br>
Edit captions/tags intuitively while viewing your images. Built-in automatic tagging with WD14 Tagger is also included.Trigger words can also be easily added.

### ✅リアルタイム進捗 / Real-time Progress

学習の進捗状況をプログレスバーとブラウザのタブタイトルでリアルタイムに確認できます。<br>
Check training progress in real time through the progress bar and the browser tab title.

### ✅学習履歴 / Training History

過去の学習設定を自動で保存し、あとから確認できます。素材フォルダ、推定ステップ数、主要な学習設定、@付きトリガーワードなどを直近30件まで記録します。<br>
Automatically saves past training settings so you can review them later. It records up to the latest 30 runs, including dataset folder, estimated steps, key training settings, and @ trigger words.

### ✅Blackwell (RTX 50) 対応 / Blackwell Ready

最新GPUで発生しがちな CUDA エラーを自動検知し、最適な環境（CUDA 13.0 等）を構成します。<br>
Automatically detects common CUDA issues on the latest GPUs and configures an optimized environment, such as CUDA 13.0.

### ✅自動シャットダウン / Auto Shutdown

長時間の学習完了後に PC を自動でシャットダウンするオプションを搭載。<br>
Includes an option to automatically shut down your PC after long training sessions finish.

### ✅ComfyUI 変換機能 / ComfyUI Conversion

学習完了後、自動的に ComfyUI で即座に使用可能な形式へ変換・出力します。  
After training completes, the LoRA is automatically converted and exported into a format that can be used immediately in ComfyUI.

---

## 📋 動作要件 / Requirements
- **OS**: Windows 10/11
- **GPU**: NVIDIA GPU (VRAM 8GB 以上推奨)
- **Python**: 3.10 以上

## 🚀 使い方
1. ダウンロード: Anima-LoRA-Factory-v*.zipをダウンロードして解凍してください。
1. 起動: フォルダ内の start.bat をダブルクリックします。
1. 初期設定: 黒い画面（コマンドプロンプト）で環境構築が始まります。完了すると自動的にブラウザで GUI が開きます。
1. 学習開始: 画像フォルダを指定し、必要に応じてタグを編集します。Anima Base Model, VAE, Qwen3 のパスを指定します。「LoRA学習開始」ボタンを押せばトレーニングが始まります！

## 🚀 How to Use
1. Download: Download Anima-LoRA-Factory-v*.zip.
1. Launch: Double-click start.bat.
1. Initialization: The terminal will automatically setup the environment. The GUI will open in your browser once ready.
1. Start Training: Set your dataset path, configure model paths, and click "Start Training"!

---

### 🔧 必要モデル / Required Models

- **Anima Base Model**
  - `anima-base-v1.0.safetensors`
  - https://huggingface.co/circlestone-labs/Anima/blob/main/split_files/diffusion_models/anima-base-v1.0.safetensors 
  - 派生モデルでの学習は動作保証していません。Training with derivative models is not officially supported.

- **Qwen3 Text Encoder**
  - `qwen_3_06b_base.safetensors`
  - https://huggingface.co/circlestone-labs/Anima/blob/main/split_files/text_encoders/qwen_3_06b_base.safetensors

- **Qwen Image VAE**
  - `qwen_image_vae.safetensors`
  - https://huggingface.co/circlestone-labs/Anima/blob/main/split_files/vae/qwen_image_vae.safetensors

---

## 📝 更新履歴 / Version History

v4.7以降の更新内容は **Releases**、それ以前の更新履歴は **CHANGELOG.md** をご覧ください。  
For version history, see **Releases** for v4.7 and later, and **CHANGELOG.md** for earlier versions.

- [Releases](https://github.com/UNfukashigi/Anima-LoRA-Factory/releases)
- [CHANGELOG.md](CHANGELOG.md)

---

## 🔗 参考・クレジット / References & Credits
このプロジェクトは、以下の素晴らしいリポジトリおよびモデルの成果に基づいています。

- Anima Model: [circlestone-labs/Anima (HuggingFace)](https://huggingface.co/circlestone-labs/Anima)
- Training Engine: [kohya-ss/sd-scripts](https://github.com/kohya-ss/sd-scripts)
- Anima Training Docs: [sd-scripts/anima_train_network.md](https://github.com/kohya-ss/sd-scripts/blob/main/docs/anima_train_network.md)

## 🔑License
This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

## 📝 免責事項 / Disclaimer
本ツールを使用して作成されたモデルや、その使用によって生じた損害について、開発者は一切の責任を負いません。 The developer is not responsible for any models created using this tool or any damage caused by its use.

---

Created by [fukachan.jp](https://fukachan.jp/)<br>

X [https://x.com/UNfukashigi](https://x.com/UNfukashigi)
