* Always use synchronize instead of copy for large files or folders
    
    ```yaml 
    synchronize:
          archive: true
          src: "/Applications/Google Chrome.app/"
          dest: "/Applications/Google Chrome Work.app/"
    ```
    
