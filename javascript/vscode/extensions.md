## how to output installed extenstions

    code --list-extensions | xargs -L 1 echo code --install-extension > vscode_extensio
    ns.txt

## vs code extensions list

    code --install-extension batisteo.vscode-django
    code --install-extension bibhasdn.django-html
    code --install-extension bigonesystems.django
    code --install-extension christian-kohler.path-intellisense
    code --install-extension CoenraadS.bracket-pair-colorizer
    code --install-extension dbaeumer.vscode-eslint
    code --install-extension donjayamanne.javadebugger
    code --install-extension dsznajder.es7-react-js-snippets
    code --install-extension dzannotti.vscode-babel-coloring
    code --install-extension ecmel.vscode-spring-boot
    code --install-extension EQuimper.react-native-react-redux
    code --install-extension esbenp.prettier-vscode
    code --install-extension georgewfraser.vscode-javac
    code --install-extension leizongmin.node-module-intellisense
    code --install-extension ms-python.python
    code --install-extension msjsdiag.vscode-react-native
    code --install-extension Pivotal.vscode-boot-dev-pack
    code --install-extension Pivotal.vscode-concourse
    code --install-extension Pivotal.vscode-manifest-yaml
    code --install-extension Pivotal.vscode-spring-boot
    code --install-extension redhat.java
    code --install-extension redhat.vscode-xml
    code --install-extension ritwickdey.LiveServer
    code --install-extension sohibe.java-generate-setters-getters
    code --install-extension VisualStudioExptTeam.vscodeintellicode
    code --install-extension vscjava.vscode-java-debug
    code --install-extension vscjava.vscode-java-dependency
    code --install-extension vscjava.vscode-java-pack
    code --install-extension vscjava.vscode-java-test
    code --install-extension vscjava.vscode-maven
    code --install-extension vscjava.vscode-spring-boot-dashboard
    code --install-extension vscjava.vscode-spring-initializr
    code --install-extension xabikos.JavaScriptSnippets
    code --install-extension YouMayCallMeV.vscode-java-saber


## setting for django 

                {
            "window.zoomLevel": 2,
            "files.associations": {

                "*.myphp": "php",
                "*.go": "go",
            
                "*.py":"python"
            
            },
            "editor.quickSuggestions": null,
            "python.linting.pylintArgs": [
                "--load-plugins=pylint_django"
            ],

            "[python]": {

            },
        }