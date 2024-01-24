# Presentations Repository

This repository contains a collection of presentations designed to be rendered with the Marp extension in Visual Studio Code or via the command line using Pandoc.

## Getting Started

These instructions will get you a copy of the presentations up and running on your local machine for development and presentation purposes.

### Prerequisites

Before you begin, ensure you have the following installed:
- [Visual Studio Code](https://code.visualstudio.com/)
- [Marp for VS Code Extension](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)
- [Pandoc](https://pandoc.org/) (for command line rendering)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/your-repository-name.git   
   ```

2. Open the cloned repository in Visual Studio Code.
3. Install the Marp for VS Code extension if you haven't already.

## Usage

To view or edit the presentations:

### Using Marp in Visual Studio Code

1. Open the `.md` file you wish to view or edit.
2. Use the Marp panel in VS Code to see the slide preview.

### Using Pandoc

To render the presentations into a slide deck (e.g., PDF), run:

```bash
pandoc your-presentation.md -t beamer -o your-presentation.pdf
```

Replace `your-presentation.md` with the name of your Markdown file and `your-presentation.pdf` with the desired output file name.
