# hyp

MS-CEINTL.vscode-language-pack-zh-hans
run = "py .pythonlibs/bin/flask"
modules = ["nodejs-20:v8-20230920-bd784b9", "python-3.10:v25-20230920-d4ad2e4"]

[nix]
channel = "stable-23_05"

[[ports]]
localPort = 5000
externalPort = 80

[deployment]
deploymentTarget = "cloudrun"
run = ["sh", "-c", "python3 main.py"]
