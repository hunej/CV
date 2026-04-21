# 黃奕鈞 (Huang Yi-Chun) 履歷

**【個人摘要】**
任職於松翰科技股份有限公司 (Sonix Technology Co., Ltd.)，擁有超過 9 年的演算法與智能軟硬體開發經驗（任職期間：2016年11月至今），先後歷練演算法開發處語音與訊號處理部、智能軟體設計部及智能影音設計課。專精於**電腦視覺與影像辨識 (特別是 Microsoft HPD 相關技術)、語音與音訊訊號處理、多平台音訊編解碼 (Audio Codec) 優化，以及邊緣運算 (Edge AI) 上的深度學習技術**（包含聲音事件檢測、語音降噪、關鍵字喚醒、人臉與人形物件辨識等）。具備從頂尖論文研讀、神經架構搜尋 (NAS)、模型輕量化、底層 MCU 算力與記憶體壓縮，到 PC 端推論框架部署的完整實作能力，並具備 **Agentic Coding (AI 代理輔助開發)** 實戰經驗以大幅加速軟硬體開發流程。

---

**【核心專長】**
*   **深度學習與 AI 應用：** 熟練應用 CNN、RNN (GRU/LSTM)、U-Net 等架構於語音降噪 (SECNN/SENN)、關鍵字喚醒 (KWS) 及人體/人臉偵測與姿態估計。具備神經架構搜尋 (NAS)、模型輕量化設計、定點化 (NNoM)、分散式訓練 (Distributed Training)、知識蒸餾 (Knowledge Distillation) 及少樣本學習 (Few-Shot Learning) 經驗。
*   **模型推論與平台部署：** 熟悉 ONNX 生態系，並具備針對 Edge 端推論框架的優化與測試經驗。
*   **軟體工程與系統平台：** 精通 C、Assembly、Python，具備導入 **Agentic Coding (GitHub Copilot)** 加速演算法開發與程式碼優化之豐富經驗。熟悉多種嵌入式平台，包含 SNC 系列晶片 (SNC7312, SNC32F10, SNC86000, SNC7320, SNC7330, SNC7648)、ARM Cortex-M 架構。
*   **語音與音訊處理：** 聲音事件檢測 (AAD)、關鍵字喚醒 (KWS)、聲學迴聲消除 (AEC)、雜訊抑制 (SENN/NR)、波束成形 (Beamforming)、盲訊號分離 (BSS) 及空間殘響消除 (Dereverberation/WPE) 等。具備 MP3, AAC, DPCM-Based Codec, G.722.1-Based Codec 等 Audio Codec 多平台移植與優化經驗。

---

**【專案亮點】**

**一、Microsoft HPD (Human Presence Detection) 視覺 AI 引擎開發**
*   **研發與系統整合：** 深入研讀 Windows HPD 規範與 Intel Athena Project 標準，並與英業達 (Inventec) 合作進行 HPD 文件、程式碼與測試報告的分析與系統調適。
*   **全方位人臉視覺演算法開發：**
    *   **視線校正 (Eye Contact Correction, ECC)：** 研究 GazeFlow 與 ETH-XGaze，從零實作 Sonix ECC 訓練與推論框架。
    *   **頭部姿態估計 (Head Pose Estimation)：** 開發涵蓋大角度轉動 (Wide-range) 及配戴口罩 (Masked) 情境的輕量化模型 (SonixPose)，使用 300W-LP、CMU Panoptic 及自研資料集進行訓練，效能逼近大型 SOTA 模型。
    *   **人臉辨識 (FaceID)：** 整合 ArcFace、MobileFaceNet、ShuffleNet 等架構開發極輕量化模型 (約275K參數量)，於 LFW 達 99.38% 準確率。針對低照度/灰階環境進行優化。
    *   **人臉偵測與特徵點 (Face Detection & Landmark)：** 重構並訓練 PFLD、RetinaFace 模型，完成模型 ONNX 轉換，並應用於巨量資料庫 (WiderFace) 的自動化標註。

**二、AI 語音降噪模型 (SENN/ENC) 跨世代演進與極限優化**
*   **全頻帶高音質降噪演進：** 主導電競耳機 AI 降噪技術跨世代演進，由 16kHz 推進至 32kHz (Super-wideband) 及 48kHz (Full-band) 全頻帶模型。
*   **前瞻網路架構設計：** 導入 RNN 結合 Mel-domain 取樣以有效降低輸入維度與運算量；並借鑒 DTLN 論文思路，設計基於 FFT-domain 的 Magnitude Mask 作為網路輸出與損失函數優化。
*   **微控制器 (MCU) 算力極限突破：** 為突破 Cortex-M 的算力限制，於網路中以 `hard-sigmoid` 及 `softsign` 取代高耗能的 `sigmoid` 與 `tanh` 激活函數，大幅降低非線性運算負載卻依然維持高度降噪精度。後續完成 Sonix SENN 48k 函式庫釋出，並成功於 SNC7330 平台進行程式碼體積最佳化與前處理 C code 拆分。
*   **深度學習前期研發：** 早期即架設 TensorFlow 環境，成功實作基於生成對抗網路 (SEGAN) 及 U-Net 架構的語音增強演算法，並開發 GPU 加速的 ICNN 訓練工具。

---

**【工作經歷】**

**松翰科技股份有限公司 (Sonix Technology Co., Ltd.) | 2016/11 – 至今**

**智能影音設計課 | 2024/01 – 至今**
*   **Microsoft HPD (Human Presence Detection) 專案主導：** 負責開發上述視覺應用相關 AI 模型，涵蓋視線校正、人臉檢測、頭部姿態估計與極輕量化人臉辨識技術。
*   **AI 語音降噪模型 (SENN/ENC) 進階開發與架構設計：** 主導電競耳機 AI 降噪技術跨世代演進，由 16kHz 推進至 32kHz 及 48kHz 全頻帶模型。導入 RNN 結合 Mel-domain 取樣以降低運算量，並借鑒 DTLN 設計 Magnitude Mask 輸出。於網路中以 hard-sigmoid/softsign 取代高耗能激活函數突破 Cortex-M 算力限制。完成 Sonix SENN 48k 函式庫釋出，並於 SNC7330 平台進行程式碼體積最佳化與前處理 C code 拆分。
*   **Agentic Coding 與前瞻 AI 視覺開發 (Figure & Bad Posture Detection)：** 主導 Security 人形偵測 (Figure Detection) 系統，導入 Agentic Coding 模式大幅提升開發效率。結合神經架構搜尋 (NAS) 與知識蒸餾技術，針對邊緣裝置算力進行輕量化。近期進一步擴展至不良姿勢偵測 (Bad Posture Detection) 專案，主導巨量專屬資料集的建置與清洗工作。
*   **Agentic Coding 加速音訊編解碼優化 (HQDPCM)：** 運用 GitHub Copilot 等工具，針對 PC 端執行耗時的 HQDPCM Encoder 進行深度 C Code 程式碼優化，大幅縮減批量音檔的編碼運算時間。
*   **聲音事件檢測 (AAD) 與邊緣關鍵字喚醒 (KWS) 系統：** 從零到一完成 Cortex-M 平台上的聲音事件檢測 (Acoustic Activity Detection, AAD) 演算法開發。涵蓋 PCM-domain 底層實作、誤判率 (FAR) 調適及即時展示系統開發。同步開發 Keyword Spotting (KWS) 系統，導入知識蒸餾與少樣本學習技術。
*   **邊緣運算音訊底層開發 (RISC-V)：** 將 Audio32plus及HQDPCM 演算法移植至 Andes RISC-V 平台，成功進行 C model 的程式碼最佳化。

**智能軟體設計部 | 2020/04 – 2023/12**
*   **自研邊緣神經網路推論框架 (NN Inference Framework)：** 針對 SNC7320 平台自主開發底層 NN OP Firmware，深度結合硬體 FIR ASIC 加速器特性，實作卷積運算平行化及 Saturation Control。參考 ARM CMSIS-NN 建立定點化運算標準，開發多種卷積算子，並通過 ONNX/PyTorch Checksum 驗證。
*   **神經網路物件辨識：** 開發 7320 平台上的 CNN 繪本與圖卡辨識技術，涵蓋訓練資料擴增集生成，並利用 NNoM 工具進行模型的定點化轉換與 7330 平台的手寫辨識移植。
*   **ARM Cortex-M 音訊編解碼器優化與整合：** 
    *   **Audio32plus：** 將 Decoder 運算量由 22 MIPS 大幅壓低至 6.9 MIPS，Encoder 由 24 MIPS 降至 8.6 MIPS。
    *   **Helix MP3 Decoder：** 成功移植解碼器，將 48kHz Stereo 解碼運算量由 89.78 MIPS 降至 38.27 MIPS。透過 IMDCT/輸出緩衝區重疊等技術進行深度 RAM 優化，並建立完整解析與容錯機制修復異常，確保量產級穩定性。
*   **CNN 語音降噪 (SECNN) 與 PureVoice IP：** 接手 SNC7320 電競耳機開發神經網路降噪演算法，優化 MIPS 與 RAM 佔用；接手PureVoice IP並優化 AEC、NR、NLP 與 Beamforming 相關算法，成功應用於 Zoombox 視訊會議系統專案。
*   **進階視覺處理：** 實作及研究人像去背 (Portrait Matting)、視線校正 (Eye Contact Correction, ECC) 及人臉地標偵測 (Facial Landmark Detection) 技術。

**演算法開發處 語音與訊號處理部 | 2016/11 – 2020/03**
*   **多平台音訊編解碼器移植：** 負責 MP3、Audio32、MSADPCM、HQDPCM 在 SNC7312、SNC86000 及 SNC7320 等平台上的 C model 及定點 Assembly model 移植與效能優化。
*   **前端語音處理演算法：** 開發並驗證雙麥克風風切聲壓抑、基於獨立向量分析 (IVA) 的盲訊號分離 (BSS) 系統，以及以消除空間殘響為目標的 WPE 演算法。
*   **DSP 數學函式庫與影像辨識：** 完成 7312 平台 DSP Math Library 的 C model 驗證；開發卡片圖案辨識、GIF 解碼器以及 QR Code 解碼演算法，並針對低光源環境進行二值化算法優化。
*   **語音降噪深度學習前期研發：** 架設 TensorFlow 環境，成功實作基於生成對抗網路 (SEGAN) 及 U-Net 架構的語音增強演算法，並開發 GPU 加速的 ICNN 訓練工具。