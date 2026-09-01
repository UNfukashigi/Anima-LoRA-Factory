# Anima LoRA Factory 🚀

<img src="https://github.com/UNfukashigi/Anima-LoRA-Factory/blob/main/image1.png">

Anima LoRA Factory は、次世代画像生成モデル Anima の LoRA 学習を、プログラミングの知識なしで誰でも簡単に行えるように設計された GUI ツールです。 特に最新の NVIDIA RTX 50シリーズ (Blackwell / sm_120) への対応や、複雑な環境構築の自動化にこだわっています。

> Anima LoRA Factory is a user-friendly GUI tool designed for training LoRAs for the next-generation Anima diffusion models. It simplifies the complex setup process and offers native support for the latest NVIDIA RTX 50 Series (Blackwell / sm_120) GPUs.

▼SDXLバージョンも公開しています。- SDXL version is also available.<br>
[https://github.com/UNfukashigi/SDXL-LoRA-Factory](https://github.com/UNfukashigi/SDXL-LoRA-Factory)

▼詳しい使い方については、以下の記事をご覧ください。- For detailed instructions on how to use it, please see the article below.<br>
[https://x.com/UNfukashigi/status/2045744319433490449](https://x.com/UNfukashigi/status/2045744319433490449)

---

## 🌟 主な機能 / Key Features

### ✅全自動環境構築 / Auto Setup

start.bat を実行するだけで、必要な学習エンジン (sd-scripts) やハードウェアに最適な PyTorch を自動的にセットアップします。  
Just run `start.bat` to automatically set up the required training engine (`sd-scripts`) and the best PyTorch version for your hardware.

### ✅ビジュアルタグエディタ / Visual Tag Editor

画像を見ながら直感的にキャプション（タグ）を編集可能。WD14 Tagger による自動タグ付け機能も内蔵しています。  
Edit captions/tags intuitively while viewing your images. Built-in automatic tagging with WD14 Tagger is also included.

### ✅リアルタイム進捗 / Real-time Progress

学習の進捗状況をプログレスバーとブラウザのタブタイトルでリアルタイムに確認できます。  
Check training progress in real time through the progress bar and the browser tab title.

### ✅Blackwell (RTX 50) 対応 / Blackwell Ready

最新GPUで発生しがちな CUDA エラーを自動検知し、最適な環境（CUDA 13.0 等）を構成します。  
Automatically detects common CUDA issues on the latest GPUs and configures an optimized environment, such as CUDA 13.0.

### ✅自動シャットダウン / Auto Shutdown

長時間の学習完了後に PC を自動でシャットダウンするオプションを搭載。  
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
1. ダウンロード: Anima-LoRA-Factory-v2.2.zipをダウンロードして解凍してください。
1. 起動: フォルダ内の start.bat をダブルクリックします。
1. 初期設定: 黒い画面（コマンドプロンプト）で環境構築が始まります。完了すると自動的にブラウザで GUI が開きます。
1. 学習開始: 画像フォルダを指定し、必要に応じてタグを編集します。Anima Base Model, VAE, Qwen3 のパスを指定します。「LoRA学習開始」ボタンを押せばトレーニングが始まります！

## 🚀 How to Use
1. Download: Download Anima-LoRA-Factory-v2.2.zip.
1. Launch: Double-click start.bat.
1. Initialization: The terminal will automatically setup the environment. The GUI will open in your browser once ready.
1. Start Training: Set your dataset path, configure model paths, and click "Start Training"!

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

<code>9/2 更新（Updated）**v5.0**<br>
・学習履歴機能を追加しました。直近30回分の素材フォルダ、設定内容、推定ステップ数、@付きトリガーワードを確認できます。- Added training history. You can view the last 30 runs, including dataset path, settings, estimated steps, and @ trigger words.<br>
・セットアップ時の依存関係チェックを改善しました。必要なライブラリのインストールに失敗した場合、起動前にエラーが分かるようになりました。- Improved dependency checks during setup. If required libraries fail to install, the error is shown before launching the app.</code><br>

<code>9/1 更新（Updated）**v4.9**<br>
・PyTorchインストール時の参照先指定を修正しました。通常のPythonパッケージはPyPIから取得しつつ、PyTorchのCUDA版も取得できるようになり、初回セットアップや環境修復がより安定します。- Fixed the PyTorch install index setting. Setup now uses PyPI for normal Python packages while also checking the PyTorch CUDA wheel index, improving first-time setup and repair stability.</code><br>

<code>8/31 更新（Updated）**v4.8**<br>
・RepeatsをUIから設定できるようにしました。デフォルト値は2です。- Added a UI setting for Repeats. The default value is 2.<br>
・画像枚数 × Repeats × Epochs に基づく推定ステップ数を表示するようにしました。- Added an estimated step count based on image count × Repeats × Epochs.<br>
・学習の強さと総ステップ数の目安を表示する説明欄を追加しました。- Added a guide explaining training strength and recommended total step ranges.<br>
・上級設定にDataLoader Workersを追加しました。0が最も安定し、旧バージョンと同じ挙動に近づけたい場合は8に設定できます。- Added DataLoader Workers to Advanced Settings. 0 is the most stable, and 8 is close to the previous version behavior.</code><br>

<code>7/6 更新（Updated）**v4.7**<br>
・依存関係や細かいバグの修正。-Fixes for dependencies and minor bugs.</code><br>

<code>7/5 更新（Updated）**v4.6.1**<br>
・学習中にログ表示用のWebSocket接続が途中で切断され、画面上では学習が停止したように見える場合がある問題への対策として、サーバー側の接続維持設定を調整しました。- Adjusted the server-side connection keep-alive settings to help prevent cases where the WebSocket connection used for training logs disconnects during training, making it appear as if training has stopped on the screen.</code><br>

<code>7/5 更新（Updated）**v4.6**<br>
・上級設定に左右反転 augmentation、タグ順シャッフル、keep_tokens、Min SNR Gamma を追加しました。各オプションは初期状態ではOFFで、必要な場合のみ有効化できます。Min SNR Gamma は数値変更に対応し、推奨値を5として案内しています。- Added Horizontal Flip Augmentation, Shuffle Caption, keep_tokens, and Min SNR Gamma to Advanced Settings. These options are off by default and can be enabled only when needed. Min SNR Gamma now supports custom values, with 5 shown as the recommended value.<br>
・Optimizer Args の入力欄がわかりにくかったため、入力例の表示と自動保存を削除しました。過去に保存された値も起動時に自動で消去され、通常は空欄のまま利用できます。- Removed the confusing example text and auto-save behavior from Optimizer Args. Previously saved values are now cleared on startup, so the field stays blank by default.<br>
・依存関係の不足やバージョン差によるエラー対策として、voluptuous を requirements に追加し、transformers を4系（transformers>=4.44,<5）に固定しました。これにより、新規環境でのセットアップ失敗や transformers 5系との互換性問題を避けやすくしています。- Added voluptuous to requirements and constrained transformers to version 4.x (transformers>=4.44,<5) to reduce setup failures and compatibility issues with transformers 5.x in fresh environments.</code><br>

<code>6/29 更新（Updated）**v4.0**<br>
・学習設定画面に「オプティマイザー」選択欄を追加し、AdamWに加えてProdigy / DAdaptation（学習率自動調整）を選択できるようにしました。Prodigy / DAdaptation選択時は学習率の表示が専用のヒント（推奨値1.0前後）に切り替わります。- Added an “Optimizer” selector to the training settings. In addition to AdamW, you can now choose Prodigy / DAdaptation (auto learning-rate tuning). Selecting Prodigy/DAdaptation switches the learning rate UI to a dedicated hint recommending a value around 1.0.<br>
・上級設定に「オプティマイザー追加引数 (--optimizer_args)」の入力欄を追加しました。decouple=Trueなどの追加パラメータを任意で指定できます。- Added an “Optimizer Args (--optimizer_args)” field to the advanced settings, allowing optional extra parameters such as decouple=True to be specified.<br>
・Prodigy / DAdaptation選択時に「低VRAM対策を強化する」チェックボックスを追加しました。有効にするとblocks_to_swap（SDXL版はキャッシュ系オプション）を追加し、VRAM消費を抑えます（学習はやや遅くなります）。- Added an “Extra low-VRAM offset” checkbox shown when Prodigy/DAdaptation is selected. Enabling it adds extra blocks_to_swap (or extra caching options on the SDXL version) to reduce VRAM usage, at the cost of slightly slower training.<br>
・requirements.txtにdadaptation・prodigyoptを追加し、「学習環境の再構築」ボタンで自動インストールされるようにしました。また同ボタンが常に再実行可能になり、依存パッケージの追加があった場合もいつでも再インストールできるようにしました。- Added dadaptation and prodigyopt to requirements.txt so they are installed automatically via the “Repair Environment” button. The button can now always be re-run, so newly added dependencies can be reinstalled at any time.<br>
・LoRAのランク (network_dim) ・アルファ (network_alpha) のデフォルト値を4/1から16/16に変更しました。キャラクターLoRA用途でより実用的な強さになります。- Changed the default LoRA rank (network_dim) and alpha (network_alpha) from 4/1 to 16/16, providing more practical training strength for character LoRA use cases.<br></code>

<code>6/29 更新（Updated）**v3.1**<br>
・タグ編集画面に「トリガーワード追加」ボタンを追加しました。通常の「一括追加」は全画像のキャプション末尾にタグを追加し、「トリガーワード追加」は全画像のキャプション先頭にキーワードを追加するように変更しています。- Added a “Trigger Word” button to the tag editor. Normal batch add now appends tags to the end of captions for all images, while trigger word add inserts keywords at the beginning of captions for all images.</code><br>

<code>・`start.bat` 内の `APP_PORT` を編集することで、GUIのポート番号をユーザーが自由に変更できるようにしました。- Added an `APP_PORT` setting in `start.bat`, allowing users to change the GUI port number freely.</code>

<code>6/28 更新（Updated）**v3**<br>
・セットアップ時に指定されていた古いPyTorch nightly固定バージョンが取得できず、インストールに失敗する問題を修正しました。RTX 50シリーズ向けのPyTorch / torchvisionは固定日付を外し、現在配布されているnightly版へ更新する形式に変更しています。- Fixed an issue where setup failed because the old fixed PyTorch nightly versions were no longer available. For RTX 50 series GPUs, PyTorch / torchvision installation now uses the currently available nightly build without fixed date-based versions.</code>

<code>5/2 更新（Updated）**v2.3**<br>
・英語と日本語以外の環境でエラーが発生する問題を修正しました。英語か日本語の環境であれば2.2でも問題なく利用可能です。中国語などほかの言語をご利用の場合は2.3をご利用ください。- We have fixed an issue where errors occurred in environments other than English and Japanese. Version 2.2 should work without problems in English or Japanese environments. For other languages ​​such as Chinese, please use version 2.3.</code>

<code>4/26 更新（Updated）**v2.2**<br>
・エラー報告の多かった原因のsd-scriptsを同梱しました。ZIP形式での配布に変更。Gitは不要になりました。- We've included sd-scripts, which were the cause of many error reports.Distribution format changed to ZIP.Git is no longer needed.</code>

<code>4/26 更新（Updated）**v2.1**<br>
・エラー報告の多かった原因として、PCのグローバル環境で環境変数PYTHONPATHが設定されている場合について、必ずvenv環境のPythonを利用するように更新しました。- Due to a high number of error reports, we have updated the code to always use the Python environment in a venv environment when the environment variable PYTHONPATH is set in the PC's global environment.</code>

<code>4/25 更新（Updated）<br>
・venv環境をツール内に構築する設計にしました。グローバル環境に影響を与えず、より安心してご利用頂けます。- The design now incorporates a venv environment within the tool. This ensures that it does not affect the global environment and can be used with greater peace of mind.<br>
・より安定して使えるようにモジュールチェック機能を強化し、自動インストールの機能も強化しました。- The module check function has been enhanced for greater stability, and the automatic installation function has also been improved.
・Anima版とSDXL版でURL（ポート番号）を分けました。キャッシュが被らないので表示も安定するはず。- I've separated the URLs (port numbers) for the Anima and SDXL versions. This should prevent cache conflicts and improve display stability.</code>

---

Further modifications have been made so that the following people can also use it.<br>
People using an NVIDIA GPU that is not the latest model.<br>
People who already have the CPU version of PyTorch installed on their PC.<br>
People whose torchvision has mysteriously disappeared.<br>
People who do not have a GPU (or have an AMD/Intel GPU).<br>

---

Created by [fukachan.jp](https://fukachan.jp/)<br>

X [https://x.com/UNfukashigi](https://x.com/UNfukashigi)
