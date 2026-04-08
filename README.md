# Minecraft-datapacks
# 至尊礼包数据包 (JoinReward)

这是一个为《我的世界》版本设计的顶级新手礼包数据包。当玩家首次加入服务器或世界时，系统会自动为其发放一套极其强大的顶级装备、武器、工具、食物和特殊物品，并伴有华丽的音效和粒子特效，旨在为玩家提供最顶级的开局体验。

<img width="1920" height="1013" alt="2026-03-23_18 45 37" src="https://github.com/user-attachments/assets/e3da85e8-caf7-4c61-9451-b8c1d8a7423f" />


## ✨ 主要功能

- **自动发放**：玩家首次进入游戏时，自动触发礼包发放流程，无需任何命令。
- **顶级装备**：提供全套经过强化的下界合金装备（头盔、胸甲、护腿、靴子），拥有史诗级名称、属性修饰符和附魔。
- **强力武器**：包括自定义命名的“轩辕剑”、“梨花枪”、“雷神锤”等，拥有超高攻击力和特殊属性。
- **高效工具**：“时运斧”、“时运镐”、“时运铲”等工具，附带时运和效率附魔，大幅提升采集能力。
- **丰富物资**：包含海量附魔金苹果（整箱）、强力不死图腾、豪华烟花火箭等。
- **华丽视觉**：发放时伴随炫酷的标题、消息、环绕粒子特效和史诗级音效，仪式感十足。
- **轻量化设计**：使用计分板系统，通过一个简单的tick函数高效检测并发放奖励，对服务器性能影响极小。

## 📦 安装方法

1.  **下载数据包**：将 `JoinReward.zip` 文件夹（或解压后的 `JoinReward` 文件夹）放入游戏或服务器的 `datapacks` 文件夹中。
2.  **应用数据包**：
    *   **单机**：进入世界前，在“创建世界”的“数据包”页面中，将本数据包从左侧移至右侧。
    *   **服务器**：将数据包放入 `datapacks` 文件夹后，运行 `/reload` 命令以加载。
3.  **确认加载**：加载成功后，管理员（或后台）会看到加载成功的提示信息。

## 📋 奖励清单

### ⚔️ 武器
*   **轩辕剑**（下界合金剑）：超高攻击力与攻击速度，横扫之刃。
*   **梨花枪**（下界合金矛）：超远攻击距离，带有冲刺效果。
*   **雷神锤**（重锤）：强力击退与击飞效果。
*   **引雷戟/激流戟**（三叉戟）：具备引雷或激流功能。

### 🛠️ 工具
*   **时运斧/镐/铲**：极高挖掘效率，并带有时运附魔。
*   **精采系列工具**（斧、镐、铲、锄）：“武器装备工具箱”内包含，拥有极高挖掘效率。
*   **太公**（钓鱼竿）：高幸运值，可钓出宝藏。
*   **刀镰**（打火石）、**盾**等特殊工具。

### 🛡️ 护甲
*   **三叉束发紫金冠**（下界合金头盔）
*   **兽面吞头连环铠**（下界合金胸甲）
*   **鎏金黑耀鱼鳞裤**（下界合金护腿）
*   **黄金锁子紫光靴**（下界合金靴子）
*   **璀璨明玉绮罗翼**（鞘翅）：所有护甲均拥有超高的护甲值、韧性、生命值加成和强力附魔。
*   **马铠**、**鹦鹉螺铠**（宠物/坐骑装备）：提供巨额属性加成。

### 🍎 食物与特殊物品
*   **一整箱附魔金苹果**（黄潜影盒）：每颗提供长达10000tick（约500秒）的强力状态效果。
*   **一整箱不死图腾**（紫潜影盒）：死亡时触发，移除负面效果并赋予吸收、生命恢复和抗性。
*   **烟花火箭**（品红潜影盒）与**烟花爆竹**（红潜影盒）：用于庆祝或快速飞行。
*   **武器装备工具箱**（黑潜影盒）：内含上述所有武器、工具和两件特殊马铠。
*   **其他**：末影箱、调试工具等。

### ✨ 视觉效果
*   全屏标题动画（“🌟 传奇开始 🌟”）。
*   环绕玩家的豪华粒子特效（龙息、心形、彩色墨囊、传送门等）。
*   史诗级音效序列（信标激活、唱片、雷击、挑战完成等）。
*   短暂的发光、缓降、生命恢复状态效果。

## 💻 技术信息

*   **游戏版本**：1.21.11
*   **数据包格式**：94 (兼容 71-99)
*   **主要函数**：
    *   `init.mcfunction`：初始化计分板。
    *   `tick.mcfunction`：循环检测未获得奖励的玩家。
    *   `give_reward.mcfunction`：发放奖励的主函数。
    *   `messages.mcfunction`：显示消息和特效。
*   **计分板**：`joinreward.given` (dummy)，用于追踪玩家是否已领取礼包。

## ⚙️ 自定义与扩展

您可以根据服务器需求修改奖励内容：

*   **修改奖励物品**：编辑 `data/joinreward/functions/rewards/` 目录下的 `armor.mcfunction`、`weapons.mcfunction` 等文件。
*   **修改特效与音效**：编辑 `data/joinreward/functions/messages.mcfunction` 中的粒子、音效和标题部分。
*   **禁用某些奖励**：在 `data/joinreward/functions/give_reward.mcfunction` 中，注释或删除对应的 `function` 调用行。

## ⚠️ 注意事项

*   **首次加载**：建议在加载数据包后，所有玩家重新进入世界或服务器，以确保计分板正确初始化。
*   **命令权限**：数据包内的 `give` 命令需要服务器拥有给予物品的权限。在单人模式下，这会正常工作。
*   **兼容性**：本数据包专为 **1.21.11** 版本设计，使用了该版本的物品组件（如 `attribute_modifiers`, `consumable` 等），在其他版本可能无法工作或导致错误。
*   **背包空间**：奖励物品数量较多，请确保玩家背包有足够的空间，否则物品可能会掉落在脚下。

## 📖 使用说明与命令参考

### 奖励发放逻辑
数据包通过计分板 `joinreward.given` 来记录玩家的奖励状态。其逻辑如下：
*   **未发放**：玩家计分板值为 `0` 或 `空值`（即从未加入过服务器）。
*   **已发放**：玩家计分板值会被设置为 `1`。
*   **自动触发**：`tick.mcfunction` 函数会持续检测所有在线玩家，当发现玩家的计分板值为 `0` 或 `空值` 时，便会自动调用 `give_reward.mcfunction` 为其发放完整礼包，并将计分板值标记为 `1`。

### 核心函数
您也可以手动执行以下函数来管理奖励发放（需要管理员权限）：
*   `/function joinreward:give_reward`：为**当前玩家**发放礼包。前提是该玩家的 `joinreward.given` 计分板值为 `0` 或空。
*   `/function joinreward:rewards/armor`：单独发放全套护甲。
*   `/function joinreward:rewards/food`：单独发放食物。
*   `/function joinreward:rewards/special`：单独发放特殊物品（如图腾、烟花等）。
*   `/function joinreward:rewards/tools`：单独发放工具。
*   `/function joinreward:rewards/weapons`：单独发放武器。

### 常用命令参考

#### 1. 查看与管理玩家状态
| 功能 | 命令 |
| :--- | :--- |
| **查看所有未领取的玩家** | `/execute as @a[scores={joinreward.given=0}] run tellraw @a ["",{"selector":"@s"},{"text":" 需要发放奖励","color":"yellow"}]` |
| **查看所有已领取的玩家** | `/execute as @a[scores={joinreward.given=1}] run tellraw @a ["",{"selector":"@s"},{"text":" 已获得奖励 (值=1)","color":"green"}]` |
| **重置自己（可再次领取）** | `/scoreboard players set @s joinreward.given 0` |
| **重置他人（可再次领取）** | `/scoreboard players set <玩家名> joinreward.given 0` |
| **手动标记已领取** | `/scoreboard players set <玩家名> joinreward.given 1` |
| **查看某玩家的当前值** | `/scoreboard players get <玩家名> joinreward.given` |
| **重置所有玩家状态** | `/scoreboard players reset * joinreward.given` |

#### 2. 计分板显示设置
| 功能 | 命令 |
| :--- | :--- |
| **在屏幕右侧显示** | `/scoreboard objectives setdisplay sidebar joinreward.given` |
| **在玩家列表 (Tab) 显示** | `/scoreboard objectives setdisplay list joinreward.given` |
| **移除侧边栏显示** | `/scoreboard objectives setdisplay sidebar` |
| **移除列表显示** | `/scoreboard objectives setdisplay list` |

#### 3. 调试与数据查看
| 功能 | 命令 |
| :--- | :--- |
| **查看所有计分板** | `/scoreboard objectives list` |
| **查看自己的生命值** | `/data get entity @s Health` |
| **查看自己的护甲值** | `/attribute @s minecraft:armor get` |
| **查看自己的护甲韧性** | `/attribute @s minecraft:armor_toughness get` |
| **查看手上物品的完整NBT数据** | `/data get entity @s SelectedItem` |
| **查看自己背包中所有物品的NBT** | `/data get entity @s Inventory` |

---

## 📜 许可与致谢

本数据包为免费资源，可用于个人服务器或游玩。您可以根据需要进行修改和分发。

祝您在《我的世界》中游戏愉快！🎉


