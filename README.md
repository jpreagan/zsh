# Zsh configuration files

My personal configuration files for [Zsh](https://www.zsh.org/) with [Prezto](https://github.com/sorin-ionescu/prezto).

## Install

01. Launch Zsh:

    ```console
    zsh
    ```

02. Clone the prezto repository:

    ```console
    git clone --recursive https://github.com/sorin-ionescu/prezto.git "${ZDOTDIR:-${XDG_CONFIG_HOME:-$HOME/.config}/zsh}/.zprezto"
    ```

03. Configure `$XDG_CONFIG_HOME` and `$ZDOTDIR` in _`$HOME/.zshenv`_:

    ```sh
    export XDG_CONFIG_HOME="${XDG_CONFIG_HOME:=$HOME/.config}"
    export ZDOTDIR="${ZDOTDIR:=$XDG_CONFIG_HOME/zsh}"
    source "$ZDOTDIR/.zshenv"
    ```

04. Create a new Zsh configuration by copying/linking the Zsh configuration
    files provided:

    ```console
    setopt EXTENDED_GLOB
    for rcfile in "${ZDOTDIR:-$HOME}"/.zprezto/runcoms/^README.md(.N); do
      ln -s "$rcfile" "${ZDOTDIR:-$HOME}/.${rcfile:t}"
    done
    ```

05. Clone this repository:

    ```console
    git clone git@github.com:jpreagan/zsh.git
    ```

06. Set Zsh as your default shell:

    ```console
    chsh -s /bin/zsh
    ```

07. Open a new Zsh terminal window or tab.

## License

Distributed under the MIT License. See `LICENSE` for more information.
