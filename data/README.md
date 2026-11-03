# 資料說明：筆電規格與價格資料集

本目錄的 `laptops.csv` 是由公開資料集清洗而來的筆電規格表，僅供演練使用。

## 來源

- 資料集：Hugging Face `Ammok/laptop_price_prediction`（資料集頁面：https://huggingface.co/datasets/Ammok/laptop_price_prediction ）
- 原始檔案：`laptops_test.csv`（https://huggingface.co/datasets/Ammok/laptop_price_prediction/raw/main/laptops_test.csv ）
- 下載日期：2026-11-03
- 原檔 SHA-256：`019d1b6091337c8a0e5be885a30c7b1bace57035f3fa7ff289d0aea683deff72`
- 原檔規模：49,570 bytes、325 筆資料列、13 欄

## 授權

- 資料集卡片（README 的 metadata）標示 `license: apache-2.0`；卡片未載明資料的原始來源（原始來源未載明）。
- 本 repo 以 Apache-2.0 轉載，授權全文見 [`LICENSE-Apache-2.0.txt`](LICENSE-Apache-2.0.txt)。

## 清洗後檔案概況

- 檔案：`laptops.csv`
- 筆數：325 筆（與原檔相同，未刪列、列序不變）
- 欄數：11 欄
- 編碼：UTF-8、無 BOM、LF 換行
- 欄位順序：Manufacturer, Model Name, Category, Screen Size, CPU, RAM, Storage, GPU, Operating System, Weight, Price (currency unspecified)

## 修改項目

與原檔相比，共做了下列修改：

| 編號 | 項目 | 說明 | 影響 |
| --- | --- | --- | --- |
| 1 | 去除前後空白 | 去除所有欄名與儲存格的前後空白 | 欄名 1 個（` Storage` 改為 `Storage`）；儲存格 3 格，都在 GPU 欄（`Intel HD Graphics 620 `、`Nvidia GeForce GTX 980 `、`Nvidia GeForce 920MX `） |
| 2 | 編碼錯字 | Lenovo IdeaPad Y700-15ISK 的 GPU，原檔為字面文字 `Nvidia GeForce GTX 960<U+039C>`，改為 `Nvidia GeForce GTX 960M`（依原意；資料中本來就有 `GTX 960M` 的寫法）。`Portégé Z30-C-16K` 的 é 是正確字元，保留未改 | 1 筆 |
| 3 | `Screen Size` | 原檔如 `15.6"`，改為純數字 `15.6`（只去掉雙引號，數字寫法不變） | 全部 325 筆 |
| 4 | `Storage` | 連續空白縮成一個，例如 `256GB SSD +  1TB HDD` 改為 `256GB SSD + 1TB HDD` | 48 筆 |
| 5 | 刪除欄位 | 刪除 `Screen`、`Operating System Version` 兩欄 | 13 欄變 11 欄 |
| 6 | `Price` 欄名 | 改為 `Price (currency unspecified)`，數值原樣（原資料未標示幣別） | 欄名 1 個 |

清洗腳本只在講者本機執行，未納入本 repo。

## 刻意原樣保留

- `RAM`：全為「數字＋GB」（如 `8GB`），未改動。
- `Weight`：寫法不一，未統一。324 筆為「數字＋kg」，小數位數不一（例如 `2.04kg`、`2kg`、`0.920kg`）；1 筆為 `4kgs`（Asus Rog G752VL-GC088D）。

## 使用聲明

- 公開資料集，僅供演練；機種年代較舊，不反映現行市場。
- 價格幣別未標示，數值僅供演練。
