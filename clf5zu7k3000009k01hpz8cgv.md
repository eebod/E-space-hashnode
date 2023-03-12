---
title: "Automating file re-organization on Windows with NodeJS"
datePublished: Sun Mar 12 2023 22:55:07 GMT+0000 (Coordinated Universal Time)
cuid: clf5zu7k3000009k01hpz8cgv
slug: automating-file-re-organization-on-windows-with-nodejs
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678459732167/4ab48d91-fb5e-40cd-a4f0-a544ea81165e.png
tags: operating-system, nodejs, automation, windows, scripting

---

I dual boot, which means I run two operating systems on my personal computer. I use Microsoft Windows operating system as my personal use OS and Linux Mint distro as my code-writing environment. Linux Mint, which is an Ubuntu-based Linux distribution allows me to tinker and play around with everything and anything on the OS, without fear of losing personal files.

While on Windows, I tend to take a lot of screenshots using the (🪟 + PrtSc) command. I do this for very different reasons. Over time, I came to realize there was an issue with how Windows labeled each screenshot in the screenshot folder where it saved these images. For every screenshot taken on Windows, it is named in the format &gt;&gt;( Screenshot + (Number) + .png ).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678463863528/b63f7a87-3011-4bb5-956d-ccb47ba8c761.png align="center")

The '**Screenshot**' is a description of how the image was taken, '**.png**' is the file format the image is saved in, and '**number**' there is a variable that gets incremented. The very first time you take a screenshot on windows, that first picture is stored as 'screenshot (1).png' and that number is then stored in Window's registry, the next time you take another screenshot, it pulls the last value saved in the registry, adds one(1) to it and names the new screenshot with the new value. That would mean the next screenshot saved after the first image would be saved as 'screenshot (2).png'.

The issue with this approach is that the numbering only goes up and doesn't adjust to take account of deleted images or a change in the file numbering, It just keeps on adding one to the last number saved to name the new file ahead.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678465854077/0621d7cf-935c-415d-92ca-c77833371e21.png align="center")

Taking a look at the image above, you would find discrepancies with the file naming/numbering in the screenshot folder, which is what we talked about and what we'll be fixing with the script I'll be writing later in this article.

You might say, but that's not a big deal, I could live with that and you'll be very right, millions of Windows users do and it in no way hinders how they use their machine. But unfortunately, I have been bestowed the power to write codes and make things conform, and I would love to use this power at this junction.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678466885239/3b8f39b6-8f3c-4bec-945f-2fb6f204518e.gif align="center")

Another angle to this is that it's all a fun process of telling your machine what to do, when to, and just exactly how to do what you want. Let's get into business.

## THE POWER IN CODE

**GOAL**  
The script I'll be writing would do three main things:

* Take a count of all the files(pictures) in the Screenshot Folder.
    
* Start from the top and then rename them based on the number of files present.
    
* Lastly, it would talk to Windows' registry to update the number with the new values.
    

To make the javascript file easily accessible, the file would be in the same directory as the screenshot folder, and to speed up execution time, there would be a 'sleight-of-hand' approach to run commands from Windows' search bar.

**REQUIREMENTS**  
In this article, I'll be using Node.js on a Windows machine to reorganize and rename files. Node.js is a popular tool for building server-side applications and provides several useful modules for working with the file system.

* Windows Operating System (Win-11, Win-10, Win-7, ...)
    
* NodeJS (Version 18 upwards)
    

To Install nodeJS on your windows machine:

* Download the NodeJS installer from the official website ([**https://nodejs.org/**](https://nodejs.org/)).
    
* Choose the appropriate installer based on your operating system, here we're using **Windows**.
    
* Run the installer and follow the instructions.
    
* Once the installation is complete, you can verify it by opening a terminal (or command prompt) and running the command `node -v`. This should display the version of Node.js that you just installed.
    

## Let's get Started

**Navigate into the Screenshot folder to create a new folder to house the nodeJS project, in the image folder, I created the folder and named it 're-order'.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678617074984/2c729387-3f84-4eba-bb91-4adf57019006.png align="center")

Use the context menu on the folder to open it in your preferable code editor, I use **Windows VS Code.** Within VS Code, you can use a terminal, the terminal is where I would perform all nodeJS-required executions from.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678618026684/42b117d3-6d8f-4a03-adec-5b77ba98e9f2.png align="center")

To start a new NodeJS project, we need to initialize the project with the first set of files required to function properly. To do that we use the command below

```plaintext
npm init -y
```

the '**\-y'** flag is to fill in every requirement with a default value, so we don't have to manually do that, but if you want to, you can simply drop the -y flag and fill it in yourself. A 'package.json' file is created.

The next thing would be to install the external dependencies needed, using npm. In this project, we would be mainly using the 'fs' and 'path' modules, which are built-in to nodeJS and don't need an install, but to talk to the Windows registry, we need an external package, '**regedit**'. To install 'regedit'.

```plaintext
npm install regedit
```

Before we get into writing the code fully, we can make some changes to the file structure and the 'package.json' file to speed up the writing and execution process.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678620318918/1a1bf0f1-effd-4789-b9dc-7a59f088fec6.png align="center")

Three main changes :

* Created the main javascript file where all the code would be written, named it 're-order.js'.
    
* Created a folder('src') to put the JS file into, for a level of organization.
    
* Updated the 'scripts' object in the package.json file, to point npm at the javascript file just created in the 'start' field. This makes it easier to run the code, rather than having to always type '**node re-order.js**' and having to keep track of the name and the folder you're in, you could just use '**npm start**' in the root of the directory and let npm handle the rest.
    

We're good to commence writing the code now. If you observed, there is a new **node\_modules** folder in the structure now, that's where the 'regedit' module we downloaded earlier is stored and also where any future module would be stored.

### Writing the Code

We can now head over to our r**e-order.js** file and make things happen. Earlier, we made three goals, the first being to '**take a count of all the files in the screenshot folder'**. Let's proceed.

```javascript
const fs        = require('fs');
const path      = require('path');
const regedit   = require('regedit');
```