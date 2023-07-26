# launch-config-debug-odoo16-vscode
```
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Python: Odoo16",
            "type": "python",
            "request": "launch",
            "stopOnEntry": false,
            "python": "D:\\Odoo16\\python\\python.exe",
            "console": "integratedTerminal",
            "program": "${workspaceRoot}\\odoo-bin",
            "args": [
                "--config=${workspaceRoot}\\odoo.conf",
            ],
            "cwd": "${workspaceRoot}",
            "env": {},
            "envFile": "${workspaceRoot}/.env",
        },
        {
            "name": "Odoo - Upgrade",
            "type": "python",
            "request": "launch",
            "stopOnEntry": false,
            "python": "D:\\Odoo16\\python\\python.exe",
            "program": "${workspaceRoot}\\odoo-bin",
            "args": [
                "--config=${workspaceRoot}\\odoo.conf",
            // I use "-u" and "request_module" to upgrade request modules
            "-u", "request_module",
            // I use "-d" and "request" to specify which database needs to upgrade
            "-d", "request",],
            "cwd": "${workspaceFolder}",
            "console": "externalTerminal",
            "env": {},
            "envFile": "${workspaceRoot}/.env",
        }
    ]
    
}
```
