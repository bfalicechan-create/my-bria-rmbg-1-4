# Picture Studio（Hugging Face Space 嵌入頁）

這個本機網頁把 [Alice1026/my-bria-rmbg-1-4](https://huggingface.co/spaces/Alice1026/my-bria-rmbg-1-4)
這個 Hugging Face Space（BRIA RMBG 1.4 圖片去背工具）嵌入到頁面中，並採用深色霓虹科技風介面（青藍／紫色發光、玻璃面板、grid 背景與掃描線效果）。

## 使用方式

直接雙擊 `index.html` 用瀏覽器開啟即可。

若要透過本機伺服器開啟：

```powershell
cd "C:\Users\nickh\Desktop\Gemini-Web-App\picture"
python -m http.server 8000
```

然後瀏覽 <http://localhost:8000>。

## 功能

- 以 iframe 嵌入 Space 應用程式（靜態 Space 的實際網址：`https://alice1026-my-bria-rmbg-1-4.static.hf.space/index.html`）
- 新分頁開啟 Space 頁面 / 直接開啟應用程式
- 重新載入嵌入畫面
- 全螢幕模式
- 複製 Space 連結
- 若嵌入失敗，仍可透過連結直接使用工具

## 注意事項

- 需有網路連線；首次去背時模型會下載到瀏覽器快取。
- 使用 WebGPU 的瀏覽器速度較快，不支援時 Space 會自動退回 WASM。
- 去背運算在瀏覽器端進行，圖片不會上傳到外部伺服器。
