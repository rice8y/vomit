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

---

### Overleaf installation

1. Download the `vomit.cls` file from the repository.  
2. Upload `vomit.cls` to the root folder of your Overleaf project.  
3. In your main `.tex` file, set:
   ```tex
   \documentclass{vomit}
   ```

**Requirements:** LuaLaTeX + [bxcoloremoji](https://ctan.org/pkg/bxcoloremoji)

## License

This package is distributed under the BSD 2-Clause License. See [LICENSE](LICENSE).