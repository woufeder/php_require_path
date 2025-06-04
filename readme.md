# PHP 版型路徑問題解法

## 問題描述
1. 在各系統的資料夾下，想使用上層的共用 css
2. 所以把要使用的 css 但，放在 css.php 中給各 index.php require 進來使用
2. 在 css 中使用的圖，想在各階層下也能顯示正常

## 解法 2
1. require_once 就照正常寫法，同一層的就不加點不加斜線，上一層的就兩個點一個斜線
2. 被 require 進來的 php 中的 link 的網址有用 php 的簡便式方法插了路徑變數進去
3. css 內的圖檔使用，維持在根目錄中開發版型的路徑寫法，要往上一層到 images 下取得圖檔
4. 然後在根目錄的 index.php 要設置路徑變數為 `$cssLevel = "./";`
5. 然後在 cate 下的 index.php 要設置路徑變數為 `$cssLevel = "../";`