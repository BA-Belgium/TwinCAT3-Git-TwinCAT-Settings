# Best practices XAE environment setup for git in TwinCAT 4024
## Informational video
PLC programming using TwinCAT 3 - Version control (Part 13/18)
https://www.youtube.com/watch?v=1g6eYnlzKtA&t=2866s

## Configuration of the TcProjectCompare for use with source control
https://infosys.beckhoff.com/content/1033/project_compare_tool/27021597866795659.html?id=7595618039726566519

## Save lineID's to an external file
A lot of internal markers and user bookmarks are no longer saved in the main project file but in separate files. This is easier for merge actions in source control.

![image](Source/4024/01 XAE Independent project files.png)

## Enable Multiple Project Files
Recommended, it will create a lot of smaller files, bit it reduces the number of code changes in the main project file. 
This is easier during code compare.
![image](https://user-images.githubusercontent.com/79637976/208901435-228b9c37-631c-4e32-8d50-ffea22ee1f0b.png)

## Minimize ID changes in the PLC project
This minimizes code change detections in source control.

![04 PROJECT Minimize ID changes](https://github.com/user-attachments/assets/e8cb9e2e-cfb0-4c3b-82a3-f728e8b0fe90)

## Remove check 'write project versions' in the PLC project
![03 PROJECT Write Product Versions](https://github.com/user-attachments/assets/8fa531cb-e072-4f76-aa18-21e88b969bc9)

