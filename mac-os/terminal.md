# customize terminal, set default python3(installed from brew - to override default python3)
# .zshrc

    export PATH=/opt/homebrew/bin:$PATH
    export PATH=/opt/homebrew/opt/python@3.8/bin:$PATH

    PROMPT='%B%F{cyan}%1~%f %F{178}$%f %b'

# when python3 venv does not work 

    apt-get install python3.4-dev python3.4-venv