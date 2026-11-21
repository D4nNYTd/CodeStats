# CodeStats

CodeStats is a Roblox Studio plugin that scans scripts and displays line statistics.

## Features

- Scan all supported scripts in the game.
- Scan scripts inside a selected Folder.
- Scan selected Script, LocalScript, and ModuleScript objects.
- View total, code, comment, and blank line counts.
- Select a script to inspect its individual statistics.
- Export scan results as JSON.
- View scan progress and cancel a running scan.

## How lines are counted

CodeStats reads the source of each supported script and classifies its lines as code, comments, or blank lines.

- **Code** — lines containing Luau code. A line containing both code and a comment is counted as code.
- **Comments** — lines containing comments without code, including lines inside long comments.
- **Blank** — lines containing only spaces or tabs.

The total is the sum of code, comment, and blank lines. A final newline does not create an extra line.

## Installation

1. Open the CodeStats plugin page in the Roblox Creator Store.
2. Install the plugin.
3. In Roblox Studio, open **Plugins** and click **CodeStats** to open the panel.

## Usage

1. Open the CodeStats panel from the Plugins toolbar.
2. Choose a scan mode:
   - **Entire Game** — scans supported scripts throughout the game.
   - **Selected Folder** — scans supported scripts inside the selected Folder.
   - **Selected Scripts** — scans the selected Script, LocalScript, and ModuleScript objects.
3. Click **Refresh** to start scanning. The button changes to **Cancel** while a scan is running.
4. Select a script in the explorer list to view its individual statistics.
5. Click **Export** to display the scan results as JSON. Copy the displayed text; if it is split into parts, copy them in order and join them.

## Project structure

```
CodeStats
├── codeStatsUi
├── ui
│   ├── animations
│   ├── detailsPanel
│   ├── explorerList
│   └── mainUi
└── utils
    ├── counter
    ├── exportManager
    ├── formatter
    ├── scanner
    └── selectionManager
```

## Contributing

Issues and improvements are welcome. You can use, modify, and share this project freely.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).
