# Vomit Class 🤮

Turn all your LaTeX text into vomit… literally! Every non-command character becomes the vomit emoji 🤮.  
A fun demo of LuaTeX callbacks.

## Features

- Replaces text characters with `\coloremojicode{1F92E}`
- Keeps LaTeX commands, braces, and spaces intact
- Temporarily disable/re-enable vomit mode with `\stopvomit` / `\startvomit`

## Usage

```tex
\documentclass{vomit}
\begin{document}

Hello, world!  % becomes 🤮🤮🤮🤮🤮🤮 🤮🤮🤮🤮🤮🤮

\stopvomit
Normal text here.  % becomes Normal text here.

\startvomit
Everything is 🤮 again!  % becomes 🤮🤮🤮🤮🤮🤮🤮🤮🤮🤮 🤮🤮 🤮 🤮🤮🤮🤮🤮🤮

\end{document}
```

## Installation

### Local installation

1. Clone the repository:
    ```bash
    git clone https://github.com/rice8y/vomit.git
    cd vomit
    ```

2. Install using the LaTeX3 build system:
    ```bash
    l3build install
    ```
   This will compile the `.dtx` and install `vomit.cls` into your local TeX tree.

### Overleaf installation

1. Download the `vomit.cls` file from the repository.  
2. Upload `vomit.cls` to the root folder of your Overleaf project.  
3. Since Overleaf (as of TeX Live 2024) does not include the latest `BXcoloremoji` package (registered on CTAN on 2024-11-11), you need to manually add it:
   - Download `bxcoloremoji.sty` and `bxcoloremoji-names.def` from https://github.com/zr-tex8r/BXcoloremoji  
   - Upload both files to your Overleaf project folder.

**Requirements**

- **LuaLaTeX**  
- **BXcoloremoji** package:
  - **Local installation:** TeX Live 2025 or later includes `BXcoloremoji` by default.  
  - **Overleaf:** TeX Live 2024 does not include the latest `BXcoloremoji`. You must manually download `bxcoloremoji.sty` and `bxcoloremoji-names.def` from https://github.com/zr-tex8r/BXcoloremoji and upload them to your project folder.


## License

This package is distributed under the BSD 2-Clause License. See [LICENSE](LICENSE).