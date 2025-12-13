https://hippohippo-ai.github.io/CrossGo-Public/

# CrossGo

CrossGo is a unique, web-based strategy game that uses a Go-like board but features entirely original rules. It is a game of survival and territorial connection, where players must maintain a "line of sight" to their home edges to keep their pieces alive. The goal is to capture all of the opponent's stones.

---

## 📖 Table of Contents
- [English](#-english-version)
  - [Features](#features)
  - [Game Rules](#game-rules)
  - [Tech Stack](#tech-stack)
  - [Getting Started](#getting-started)
  - [License](#license)
- [中文版本](#-中文版本)
  - [功能特性](#功能特性)
  - [游戏规则](#游戏规则)
  - [技术栈](#技术栈)
  - [快速开始](#快速开始)
  - [开源协议](#开源协议)

---

## 🇬🇧 English Version

### Features

-   **Interactive Game Board**: A fully interactive and responsive game board.
-   **Unique Game Logic**: Implements the novel "CrossGo" ruleset.
-   **AI Opponent**: Play against a built-in AI player with multiple difficulty settings.
-   **Visual Analysis**: Displays stone-to-stone and stone-to-edge connections in real-time.
-   **Notifications**: Provides feedback to the user for valid and invalid moves.

### Game Rules

CrossGo is a game of survival where the objective is to **capture all of your opponent's pieces**.

1.  **The Board & Objective**: The game is played on a 13x13 board. Black's goal is to capture all of White's stones, and White's goal is to capture all of Black's.

2.  **Life Edges**: A player's stones must remain "connected" to their designated "Life Edges" to stay on the board.
    -   **Black's Life Edges**: The Top (Row 0) and Bottom (Row 12) edges.
    -   **White's Life Edges**: The Left (Column 0) and Right (Column 12) edges.

3.  **Connectivity (Sight & Link)**: Two friendly stones are "connected" if they are on the same straight line (horizontally, vertically, or diagonally) and the path between them is completely empty. This is a "line of sight" connection.

4.  **Life & Death**: A stone is considered **Alive** if it has a direct line of sight to its Life Edge, OR it has a line of sight to a friendly stone that is itself alive. If a stone loses its connection to its Life Edge, it is considered **Dead** and is captured (removed from the board).

5.  **Turn Sequence**:
    1.  Players take turns placing one stone on an empty intersection.
    2.  After placing a stone, any of the opponent's stones that are now "Dead" are removed.
    3.  Then, any of the current player's stones that are "Dead" are removed.

6.  **Illegal Moves**:
    -   **Overload Rule**: You **cannot** place a stone if it creates a contiguous, straight line of **4 or more** of your own stones.
    -   **Suicide Rule**: A move is illegal if the stone you just placed is immediately "Dead" after all captures for the turn are resolved.
    -   **Ko Rule**: A move is illegal if it would repeat the board state from two turns prior.

### Tech Stack

-   **Frontend**: React, TypeScript
-   **Build Tool**: Vite
-   **Styling**: A utility-first CSS framework (e.g., Tailwind CSS).

### Getting Started

Follow these instructions to get a copy of the project up and running on your local machine.

1.  **Clone the repository**
    ```sh
    git clone https://github.com/your-username/CrossGo.git
    cd CrossGo
    ```

2.  **Install dependencies**
    ```sh
    npm install
    ```

3.  **Run the development server**
    ```sh
    npm run dev
    ```
    The application will be available at `http://localhost:5173` (or another port if 5173 is in use).

### License

This project is licensed under the GPLV3 License - see the [LICENSE](LICENSE) file for details.

---

## 🇨🇳 中文版本

### 功能特性

-   **交互式棋盘**: 一个功能完善、响应式的游戏棋盘。
-   **原创游戏逻辑**: 实现了独特的“CrossGo”游戏规则。
-   **AI 对手**: 内置支持多种难度的人机对战 AI。
-   **可视化分析**: 实时显示棋子之间、棋子与“存活边界”之间的连接状态。
-   **通知系统**: 为合法及非法操作提供清晰的反馈。

### 游戏规则

CrossGo 是一款生存策略游戏，其核心目标是 **吃掉对方的所有棋子**。

1.  **棋盘与目标**: 游戏在 13x13 的棋盘上进行。黑方的目标是吃掉所有白棋，反之亦然。

2.  **存活边界 (Life Edges)**: 一方的棋子必须与它指定的“存活边界”保持连接，才能留在棋盘上。
    -   **黑方边界**: 棋盘的 **顶部 (第0行)** 和 **底部 (第12行)**。
    -   **白方边界**: 棋盘的 **左侧 (第0列)** 和 **右侧 (第12列)**。

3.  **连接性 (视线连接)**: 两个同色棋子，如果它们在同一条直线（横、竖、斜）上，并且它们之间的所有交叉点都是空的，那么它们就是“连接”的。这是一种“视线”连接。

4.  **存活与死亡**: 一个棋子，如果它能直接“看到”自己的存活边界，**或者** 它能“看到”另一个存活的己方棋子，那么它就是 **存活** 的。如果一个棋子失去了与它存活边界的所有连接路径，它就被视为 **死亡**，并被吃掉（从棋盘上移除）。

5.  **回合顺序**:
    1.  玩家轮流在棋盘的空交叉点上放置一颗棋子。
    2.  落子后，计算并移除所有现在变为“死亡”状态的 **对方** 棋子。
    3.  然后，计算并移除所有现在变为“死亡”状态的 **己方** 棋子。

6.  **非法走法**:
    -   **过载规则**: 你 **不能** 在落子后，使任何方向上形成一条由 **4颗或更多** 己方棋子组成的连续直线。
    -   **自杀规则**: 如果你落下的这颗棋子，在当前回合所有提子结算后，立即处于“死亡”状态，那么这一步是禁止的。
    -   **劫争规则**: 禁止通过一步棋使棋盘局面回到两个回合之前的状态。

### 技术栈

-   **前端**: React, TypeScript
-   **构建工具**: Vite
-   **样式**: Utility-first 的 CSS 框架 (例如 Tailwind CSS)。

### 快速开始

请按照以下步骤在您的本地环境中安装并运行项目。

1.  **克隆仓库**
    ```sh
    git clone https://github.com/your-username/CrossGo.git
    cd CrossGo
    ```

2.  **安装依赖**
    ```sh
    npm install
    ```

3.  **启动开发服务器**
    ```sh
    npm run dev
    ```
    应用将运行在 `http://localhost:5173` (如果 5173 端口被占用，可能会是其他端口)。

### 开源协议

该项目基于 GPL V3 协议开源 - 详情请参阅 [LICENSE](LICENSE) 文件。
