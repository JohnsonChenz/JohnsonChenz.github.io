# Tps Multiplayer 開發紀錄
https://johnsonchenz.github.io/

* 此專案旨在實現一個小型多人連線合作遊戲，採第三人稱視角，將參照Call of Duty Zombies的玩法 [參考影片](https://www.youtube.com/watch?v=4Me6jgW3KAw)

* 簡單使用 [RiptideNetworking](https://github.com/RiptideNetworking/Riptide) 實現連線 (Server & Client 以明確定義 FuncID 的 RPC 進行溝通)

* 使用自研框架，並統一使用Addressable實現資源加載及管理(也可改用Resources)，並實現簡易的資源計數
1. UI Manager 負責生成 & 管控 UI
2. SR Manager 負責生成 & 管控 Scene(場景) & Resources(物件池 or Atlas)
3. PF Manager 負責生成 Prefab(玩家角色，攝影機等)，並不做管控，Prefab實例將自行掌管自身的生命周期
3. GS Manager 負責管控遊戲階段 例 : Init Stage(初始) => Preload Stage(預加載) => MainMenu Stage(主頁面) => Lobby Stage(開房) => Enter Stage(進入遊戲) => InGame Stage(遊戲中) => ..... => 回到MainMenu Stage
4. 尚未實現Media(音/視訊)相關功能

## 2023/02/21 完善武器系統 & 相關表現面優化
[角色IK & 初版武器系統](https://johnsonchenz.github.io/jekyll/update/2023/02/21/dev-1.html)

## 2023/02/07 更新角色IK，初版武器系統
[角色IK & 初版武器系統](https://johnsonchenz.github.io/jekyll/update/2023/02/06/dev-1.html)

## 2023/01/15 更新
[角色移動 & 動畫同步](https://johnsonchenz.github.io/jekyll/update/2023/01/15/dev-1.html)
