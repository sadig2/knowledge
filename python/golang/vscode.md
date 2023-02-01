# python and golang setup 

   ## let golang download all tools,
   ## create env in python install black formatter 
    
    ```
    pip install black
    
    ```

{
    "window.zoomLevel": 2,
    "python.formatting.provider": "black",
    "[python]": {
        "editor.formatOnSave": true,
    },

    "[go]": {
        "editor.formatOnSave": true,
        "editor.codeActionsOnSave": {
            "source.organizeImports": true
        },
    },

}