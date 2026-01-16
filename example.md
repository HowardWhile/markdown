# 專案開發進度週報 (Project Weekly Report)

> **本週重點**：完成登入頁面 UI 翻新，並修復 API 連線逾時問題。

## 1. 待辦事項追蹤 (Task List)
- [x] **前端**：更換登入頁面背景圖
- [x] **後端**：修正 `API/Login` 的 Timeout 錯誤
- [ ] **測試**：壓力測試 (預計下週一)
- [ ] **文件**：更新 API 規格書

## 2. 程式碼變更範例 (Code Block)

我們修改了 Python 的連線重試邏輯，請參考以下寫法：

```python
import time

def connect_to_server(retries=3):
    """
    嘗試連線到伺服器，若失敗則s重試
    """
    for i in range(retries):
        try:
            print(f"Connecting... Attempt {i+1}")
            # TODO: 這裡放入實際連線程式碼
            return True
        except ConnectionError:
            time.sleep(2)
    return False
```

