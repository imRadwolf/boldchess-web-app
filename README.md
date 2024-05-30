# BoldChess Web App

![Web GUI](https://img.shields.io/badge/Web_GUI-Responsive-526ba2)
![JavaScript](https://img.shields.io/badge/Language-JavaScript-f0db4f)
![Node.js Version](https://img.shields.io/badge/Node.js-v22.1.0-339933)
![Express.js](https://img.shields.io/badge/Express.js-4.19.2-259dff)
![Stockfish Chess Engine](https://img.shields.io/badge/Stockfish_Version-16-358853)
![Mobile Ready](https://img.shields.io/badge/Mobile_Ready-Yes-985b68)
![Issues](https://img.shields.io/github/issues-search/LabinatorSolutions/boldchess-web-app?label=Known%20Bugs&query=is%3Aissue+is%3Aopen+label%3Abug)
![License](https://img.shields.io/badge/License-AGPL_v3-663366)

The official chess web-based app of [BoldChess.com](https://boldchess.com/).
It is a responsive web GUI for the Stockfish chess engine, offering analysis, evaluation, and graphical features.

## Features

- Load your chess position or game using FEN, PGN, or a move list.
- Set up pieces manually in edit mode.
- Browse game history with arrows or mouse wheel.
- List and show all legal moves on the chessboard.
- Analyze positions and legal moves using the JavaScript version of Stockfish.
- Display an evaluation graph with visual indicators for blunders.
- Open a position or game in a new window via a URL.
- Play against the computer (Stockfish) and set its difficulty level.
- Detect opening categories or ECO codes.
- Customize the styling of the chessboard.
- Print arrows or mark squares on the chessboard.
- Visualize relevant squares based on Stockfish's static evaluation terms.
- Dark interface with a pitch-black background for OLED screens, enhancing battery life and user experience.
- Support for PCs, tablets, smartphones, and touch devices.

## GUI Instructions

- To open your FEN or PGN, copy it to the clipboard and paste it into the input box above the chessboard.
- To browse the game, use the mouse wheel on the chessboard or the arrow buttons.
- To open or hide windows, click on the small icons at the top of the GUI.
- To play against the engine or set its difficulty level, click on the hamburger menu.
- To change the board styling, flip the board, or open it in a new window, click on the hamburger menu.

---

## Installation

1. **Prerequisites**:
   - Ensure Node.js is installed. If not, download and install it from the [Node.js official website](https://nodejs.org/).

2. **Repository Setup**:
   - Clone the repository to your local machine.
   - Navigate to the project directory.

3. **Dependency Installation**:
   - Install the project dependencies:
     ```bash
     npm install
     ```

4. **Local Server**:
   - Start the local development server:
     ```bash
     npm run start
     ```
   - Access the application at `http://localhost:3000` in a web browser.

---

## HTTP Headers Setup

The app is currently using **Stockfish NNUE 16 JS**, which utilizes the `SharedArrayBuffer`. To ensure the engine functions correctly, you need to enable SharedArrayBuffer support both locally and on your server. This involves setting appropriate HTTP headers.

To enable `SharedArrayBuffer`, you must configure the following HTTP headers:

1. **Cross-Origin-Opener-Policy (COOP)**: This should be set to `same-origin`.
2. **Cross-Origin-Embedder-Policy (COEP)**: This should be set to `require-corp`.

These headers isolate the context of your page and provide the necessary security guarantees for using `SharedArrayBuffer`. Properly configuring these headers will allow the Stockfish NNUE 16 JS engine to operate efficiently. Alternatively, you can switch to the **Stockfish NNUE 16 Single JS** which does not utilize the `SharedArrayBuffer`.

Read more about `ShreadArrayBuffer` at [this link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/SharedArrayBuffer).

---

## Server and Deployment

The application is designed for easy deployment in any standard Node.js environment.

**Running the Server**: The main entry point is `server.js`, which serves the static files in the `public` directory, eliminating the need for a build process. This simplifies deployment and development.

**No Build Required**: Reflecting the application's simplicity and the direct use of vanilla JavaScript, the 'build' script in `package.json` is intentionally minimal: `echo 'No build required'`. This is due to the architecture's focus on serving static assets without complex build processes or server-side rendering.

---

## License

This project is licensed under the GNU AFFERO GENERAL PUBLIC LICENSE (AGPLv3). For more details, see the [AGPLv3 License](https://www.gnu.org/licenses/agpl-3.0.html).

---

## Credits

- [Stockfish](https://github.com/official-stockfish/Stockfish)
- [Stockfish.js (nmrugg)](https://github.com/nmrugg/stockfish.js)
- [TensorFlow](https://github.com/tensorflow/tensorflow)
- [PeshkaChess](https://github.com/hxim/PeshkaChess)
- [BoldChess](https://boldchess.com/)
- [Labinator](https://labinator.com/)
