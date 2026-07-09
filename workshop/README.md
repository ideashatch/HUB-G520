# HUB G520 Workshop｜HUB G520 工作坊

Hands-on workshop materials for learning how to build Android-based edge AI applications on the HUB G520 platform.

本資料夾整理 HUB G520 工作坊所需的課程投影片與範例應用，協助使用者學習如何在 HUB G520 平台上建立 Android-based Edge AI 應用。

This workshop is organized as a progressive path:

本工作坊採循序漸進方式進行：

1. **GPIO control** — understand basic board I/O control from an Android application.  
   **GPIO 控制** — 了解如何透過 Android 應用程式進行基本板端 I/O 控制。

2. **TensorFlow Lite inference** — learn how to prepare and run an AI inference workflow.  
   **TensorFlow Lite 推論** — 學習 AI 模型推論流程的準備與執行方式。

3. **Vision AI / YOLO detection** — build toward an image-based object detection demo.  
   **Vision AI / YOLO 偵測** — 建立以影像為基礎的物件偵測示範應用。

> The goal is not only to run sample apps, but to understand the minimum development flow required to move from a prepared example to a board-level AI prototype.
>
> 本工作坊的目標不只是執行範例程式，而是理解從既有範例推進到板端 AI 原型開發所需的基本流程。

---

## Repository contents｜資料夾內容

| File | Purpose | 說明 |
| --- | --- | --- |
| [`Course1_GPIO_slides_v3.pdf`](./Course1_GPIO_slides_v3.pdf) | Course 1 slides for GPIO / basic board control. | 課程 1 投影片，說明 GPIO 與基本板端控制。 |
| [`Course2_TFLite_slides_v2.pdf`](./Course2_TFLite_slides_v2.pdf) | Course 2 slides for TensorFlow Lite workflow and AI inference. | 課程 2 投影片，說明 TensorFlow Lite 流程與 AI 推論。 |
| [`Course3_VisionMaster_Workshop.pdf`](./Course3_VisionMaster_Workshop.pdf) | Course 3 slides for the VisionMaster / vision AI workshop. | 課程 3 投影片，說明 VisionMaster / 視覺 AI 工作坊內容。 |
| [`GpioDemoApp.zip`](./GpioDemoApp.zip) | Demo application package for the GPIO course. | GPIO 課程使用的範例應用程式壓縮檔。 |
| [`YoloDetectApp.zip`](./YoloDetectApp.zip) | Demo application package for the YOLO / vision detection course. | YOLO / 視覺偵測課程使用的範例應用程式壓縮檔。 |

---

## Prerequisites｜事前準備

Before starting the workshop, prepare the following:

開始工作坊前，請先準備以下項目：

- HUB G520 development board  
  HUB G520 開發板
- Android Studio  
  Android Studio 開發環境
- USB cable or network connection for device deployment/debugging  
  可用於裝置部署與除錯的 USB 線或網路連線
- Any sensors, camera modules, display modules, or external wiring required by the course instructor or slide instructions  
  課程講師或投影片指定所需的感測器、相機模組、顯示模組或外部接線

Recommended baseline knowledge:

建議具備以下基礎知識：

- Basic Android Studio project usage  
  Android Studio 專案基本操作
- Basic command-line usage  
  基本命令列操作
- Basic understanding of GPIO, AI model inference, and image detection  
  GPIO、AI 模型推論與影像偵測的基本概念

---

## Clone the workshop files｜複製工作坊檔案

```bash
git clone https://github.com/ideashatch/HUB-G520.git
cd HUB-G520/workshop
```

If the ZIP files are missing, very small, or appear as text pointer files, pull the Git LFS objects:

如果 ZIP 檔案不存在、檔案大小異常偏小，或內容看起來像文字 pointer file，請執行 Git LFS 下載：

```bash
git lfs install
git lfs pull
```

Verify that the workshop packages were downloaded correctly:

確認工作坊壓縮檔已正確下載：

```bash
ls -lh *.zip
```

The ZIP files should be real binary packages, not tiny Git LFS pointer files.

ZIP 檔案應為實際的二進位壓縮檔，而不是很小的 Git LFS pointer file。

---

## Course flow｜課程流程

### Course 1 — GPIO demo｜課程 1 — GPIO 範例

Materials:

使用材料：

- `Course1_GPIO_slides_v3.pdf`
- `GpioDemoApp.zip`

Suggested steps:

建議步驟：

1. Read the Course 1 slides.  
   閱讀課程 1 投影片。
2. Extract `GpioDemoApp.zip`.  
   解壓縮 `GpioDemoApp.zip`。
3. Open the extracted project or package according to the slide instructions.  
   依照投影片指示開啟解壓縮後的專案或應用程式套件。
4. Build and deploy the demo to the HUB G520 board.  
   建置並部署範例至 HUB G520 開發板。
5. Verify that the GPIO behavior matches the expected result in the slides.  
   確認 GPIO 行為是否符合投影片中的預期結果。

Success criteria:

成功判準：

- The application can be deployed to the board.  
  應用程式可成功部署至開發板。
- The GPIO demo can be triggered successfully.  
  GPIO 範例功能可成功觸發。
- The observed board behavior matches the workshop instruction.  
  實際板端行為符合工作坊說明。

---

### Course 2 — TensorFlow Lite inference｜課程 2 — TensorFlow Lite 推論

Materials:

使用材料：

- `Course2_TFLite_slides_v2.pdf`

Suggested steps:

建議步驟：

1. Read the Course 2 slides.  
   閱讀課程 2 投影片。
2. Follow the TensorFlow Lite workflow described in the slides.  
   依照投影片說明執行 TensorFlow Lite 流程。
3. Confirm the model file, input format, output format, and runtime behavior.  
   確認模型檔案、輸入格式、輸出格式與 runtime 行為。
4. Run the inference example on the target environment.  
   在目標環境中執行推論範例。

Success criteria:

成功判準：

- The inference flow can be executed.  
  推論流程可成功執行。
- The model input and output can be inspected.  
  可檢查模型輸入與輸出結果。
- The result can be explained at a basic level.  
  可對推論結果進行基本說明。

---

### Course 3 — Vision AI / YOLO detection｜課程 3 — Vision AI / YOLO 偵測

Materials:

使用材料：

- `Course3_VisionMaster_Workshop.pdf`
- `YoloDetectApp.zip`

Suggested steps:

建議步驟：

1. Read the Course 3 slides.  
   閱讀課程 3 投影片。
2. Extract `YoloDetectApp.zip`.  
   解壓縮 `YoloDetectApp.zip`。
3. Open the extracted project or package according to the slide instructions.  
   依照投影片指示開啟解壓縮後的專案或應用程式套件。
4. Prepare the camera / image input required by the demo.  
   準備範例所需的相機或影像輸入。
5. Build and deploy the YOLO detection demo.  
   建置並部署 YOLO 偵測範例。
6. Verify that detection results are shown correctly.  
   確認偵測結果可正確顯示。

Success criteria:

成功判準：

- The vision demo can receive image or camera input.  
  視覺範例可接收影像或相機輸入。
- Detection results are produced by the application.  
  應用程式可產生偵測結果。
- The detected output can be checked against the expected workshop scenario.  
  偵測輸出可與工作坊預期情境進行比對。

---

## Troubleshooting｜問題排除

### ZIP file is too small or cannot be opened｜ZIP 檔案過小或無法開啟

This usually means the file was not pulled from Git LFS.

這通常代表檔案尚未透過 Git LFS 正確下載。

Run:

執行：

```bash
git lfs install
git lfs pull
```

Then check again:

然後再次確認：

```bash
ls -lh *.zip
```

---

### Large ZIP file cannot be pushed to GitHub｜大型 ZIP 檔案無法推送到 GitHub

Large binary files should remain tracked by Git LFS.

大型二進位檔案應由 Git LFS 追蹤管理。

Check LFS tracking:

確認 LFS 追蹤狀態：

```bash
git lfs ls-files
cat .gitattributes
```

If a large ZIP was committed as a normal Git object by mistake, migrate it into LFS before pushing:

如果大型 ZIP 檔案曾被誤 commit 成一般 Git 物件，請先將其遷移至 Git LFS 後再推送：

```bash
git lfs migrate import --include="workshop/YoloDetectApp.zip"
git push --force-with-lease origin main
```

Use force push only when you understand that it rewrites Git history.

只有在理解此操作會改寫 Git history 的情況下，才使用 force push。

---

### App cannot be deployed to the board｜應用程式無法部署至開發板

Check the following:

請確認以下項目：

- The board is powered on.  
  開發板已正確供電。
- The host PC can detect the device.  
  主機電腦可偵測到裝置。
- Android debugging / deployment settings are enabled.  
  Android 除錯或部署設定已啟用。
- The correct device target is selected in Android Studio.  
  Android Studio 中已選擇正確的目標裝置。
- The app permissions required by the demo are granted.  
  範例應用程式所需權限已授予。

---

## Repository maintenance notes｜Repository 維護注意事項

- Keep workshop slides as PDF files.  
  工作坊投影片建議維持 PDF 格式。
- Keep large demo packages in Git LFS.  
  大型範例應用程式壓縮檔應由 Git LFS 管理。
- Do not commit extracted ZIP contents unless they are intentionally part of the source tree.  
  除非有明確需求，否則不要將解壓縮後的 ZIP 內容 commit 至 repository。
- Do not commit Android Studio build outputs such as `build/`, `.gradle/`, or generated APK files unless explicitly required.  
  除非有明確需求，否則不要 commit Android Studio 產生的 `build/`、`.gradle/` 或 APK 等建置輸出。
- Prefer updating this README whenever course files are renamed, added, or removed.  
  當課程檔案重新命名、新增或移除時，建議同步更新此 README。

---

## Suggested workshop outcome｜建議學習成果

After completing the workshop, participants should be able to:

完成工作坊後，參與者應能夠：

- Understand the basic HUB G520 application development flow.  
  理解 HUB G520 應用程式開發的基本流程。
- Run a board-level GPIO demo.  
  執行板端 GPIO 範例。
- Understand the basic TensorFlow Lite inference process.  
  理解 TensorFlow Lite 推論的基本流程。
- Run or inspect a vision AI / YOLO detection demo.  
  執行或檢視 Vision AI / YOLO 偵測範例。
- Identify what must be changed when moving from a sample app to a custom prototype.  
  判斷從範例應用推進到自訂原型時，需要調整哪些項目。

---

## Disclaimer｜聲明

The files in this folder are workshop materials and sample packages. Actual board behavior may depend on the firmware image, OS version, connected peripherals, model files, and instructor-provided setup steps.

本資料夾中的檔案為工作坊教材與範例套件。實際板端行為可能會受到 firmware image、OS 版本、外接周邊、模型檔案，以及講師提供的設定步驟影響。
