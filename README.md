從視覺辨識到情緒分析
深度學習與自然語言處理的完整實作紀錄。本專案涵蓋了從環境配置、模型架構設計到邊界案例測試的完整流程。


一、核心實作內容

1. 手寫數字辨識
模型演進：從基礎的MLP起步，理解全連接層原理。
  進階實作 CNN 卷積神經網路，在 10 個 Epoch 內達到 98% 的測試準確率。
環境配置實戰：成功解決 RTX 5060 本地端 CUDA 環境相容性問題。
  實現靈活的 `device = torch.device("cpu")` 切換邏輯，確保程式碼在不同設備上的穩定性。

2. Hugging Face 情緒分析
多國語言模型：** 使用 `transformers` 庫載入 `lxyuan/distilbert-base-multilingual-cased-sentiments-student`。
邊界測試案例 ：針對台灣網路迷因進行情緒測試。
分析結論：發現純學術/維基百科訓練的模型對在地文化脈絡及諷刺語氣的理解限制，強調了未來進行模型微調的重要性。


二、開發環境與工具
語言：Python 3.10 / C++ (學習背景)
架構：PyTorch, Transformers (Hugging Face)
環境：Miniconda / VS Code (Jupyter Notebook)
硬體優化：針對 ASUS TUF A16 進行環境調校


三、檔案說明
`lab.ipynb`: 包含 CNN 訓練與 NLP 測試的完整程式筆記。
`my_cnn_brain.pth`: 準確率 98% 的 CNN 模型權重檔。


Created by Chen Kuo-Ching @ NTUST CSIE
