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
    

We're good to commence writing the code now. As you observed, there is a new **node\_modules** folder in the structure now, that's where the 'regedit' module we downloaded earlier is stored and also where any future module would be stored.

### Writing the Code

We can now head over to our r**e-order.js** file and make things happen. Earlier, we made three goals, the first being to '**take a count of all the files in the screenshot folder'**. Let's proceed.

**The imports and constants**

```javascript
const fs        = require('fs');
const path      = require('path');
const regedit   = require('regedit');

//Path to screenshot folder
const screenshotFolder = 'C:\\Users\\Peter Ebode\\Pictures\\Screenshots';

//Registry key for screenshot counter
const keyPath = 'HKCU\\SOFTWARE\\MICROSOFT\\Windows\\CurrentVersion\\Explorer';
```

In the code body above, two main things are happening, first, is the import of modules that the program would later require to run. The modules used are :

* `'fs'` : The 'fs' module short for fileSystem, is a built-in module in Node.js that provides an interface for working with the file system. It allows you to read, write, and manipulate files and directories on your computer or server.
    
* `'path'` : The 'path' module in Node.js is a built-in module that provides utilities for working with file and directory paths.
    
* `'regedit'` : The 'regedit' npm module is a third-party package that provides a simple interface for working with the Windows registry in Node.js. The **Windows registry** is a database that stores configuration settings and options for the Windows operating system and other software applications.
    

The next two lines are for constants that hold the path to the screenshot folders and also the keypath to the screenshot counter variable in Windows registry. At this stage, I would like to point out that it is a bad idea to play around with the files and configurations in Windows registry, but I have taken my time to ensure we are only reading and writing to the right files, and if you are uncomfortable doing that, you could just comment out the section in the code, I would leave a comment in the code for that.

**Reading files in the directory and filtering**

```javascript
// Read all files in screenshot folder
fs.readdir(screenshotFolder, (err, files) => {
    if (err) {
      console.error(err);
      return;
    }
  
    // Filter only image files (png, jpg, jpeg)
    const imageFiles = files.filter(file => {
      const ext = path.extname(file).toLowerCase();
      return ext === '.png' || ext === '.jpg' || ext === '.jpeg';
    });

});
```

This section of the code uses the `fs` module to read all the files in the screenshot directory specified by the `screenshotFolder` variable. It then filters the list of files to only include image files with the extensions ".png", ".jpg", or ".jpeg". In a normal scenario, we should only have '.png' files in the screenshot folder, but just in case, there is an imported image or something changes, to handle that, we're picking jpg, png and jpeg files and to also stop the code from picking up the re-order folder we created for the code. A more detailed breakdown of the code :

* `fs.readdir(screenshotFolder, (err, files) => {...})`: This line reads the contents of the screenshot directory specified by the `screenshotFolder` variable and passes the result as an array of filenames to the callback function. If there is an error, the `err` argument will be set, and the error will be logged to the console.
    
* `const imageFiles = files.filter(file => {...})`: This line filters and returns the list of image files by creating a new array (`imageFiles`) that includes only the files that meet the condition that the file extension (determined using the `path.extname` function) must either be ".png", ".jpg", or ".jpeg".
    

**Sorting screenshot image files in order**

```javascript
// Sort image files by filename (numeric order)
imageFiles.sort((a, b) => {
  const aFile = parseInt(path.basename(a, path.extname(a)).match(/\d+/)[0]);
  const bFile = parseInt(path.basename(b, path.extname(b)).match(/\d+/)[0]);
  return aFile - bFile;
});
```

This is a continuation of the previous code, here it sorts the list of image files obtained in the previous step (`imageFiles`) in numerical order based on their filenames. Here's a breakdown of the code:

* `imageFiles.sort((a, b) => {...})`: This line calls the `sort()` method on the `imageFiles` array and passes a callback function as an argument. The callback function is used to compare two elements in the array and determine their sort order.
    
* `const aFile = parseInt(path.basename(a, path.extname(a)).match(/\d+/)[0]);`: An example of what this section does is that it would pull out the number **33** in the word 'Screenshot (33).png' and save it in the variable `aFile` . This is done by first using the `path.basename()` function to extract the filename without the extension, then using a regular expression (`/\d+/`) to match the first sequence of digits in the filename, and finally using `parseInt()` to convert the matched digits into an integer.
    
* `const bFile = parseInt(path.basename(b, path.extname(b)).match(/\d+/)[0]);`: This line does the same thing as the previous line but for the second file being compared (`b`). The numeric part of the filename is extracted and stored in the `bFile` variable.
    
* `return aFile - bFile;`: This line is the comparison function used by `sort()`. It returns a negative value if `a` should be sorted before `b`, a positive value if `b` should be sorted before `a`, and zero if their order doesn't matter. In this case, it compares `aFile` and `bFile` variables (which hold the numeric parts of the filenames) and returns the difference between them. This has the effect of sorting the array in ascending order based on the numeric part of the filenames, hence the screenshot file names are sorted in descending order based on their number value.
    

**Renaming the files to have sequential file names in the order from the previous sort**

```javascript
// Rename image files to have sequential filenames (starting from 1)
    console.log('Screenshots file Re-organization started...')
    imageFiles.forEach((file, i) => {
        const oldPath = path.join(screenshotFolder, file);
        const newPath = path.join(screenshotFolder, `Screenshot (${i + 1})${path.extname(file)}`);
        fs.rename(oldPath, newPath, err => {
            if (err) {
                console.error(err);
                return;
            }
        });
    });
    console.log(`Screenshots file(${imageFiles.length}) Re-organization complete.`)
```

This also continues on the previous code, the file renaming happens here, this is the code breakdown:

* `console.log('Screenshots file Re-organization started...')`: This line logs a message to the console to indicate that the file renaming process has started.
    
* `imageFiles.forEach((file, i) => {...})`: This line loops through each file in the `imageFiles` array and passes it to a callback function. This callback function also receives the index of the current file (`i`) as an argument.
    
* `const oldPath = path.join(screenshotFolder, file);`: This line constructs the path of the original file by joining the `screenshotFolder` variable (which holds the path to the directory containing the files) with the current filename (`file`).
    
* `const newPath = path.join(screenshotFolder,` Screenshot (${i + 1})${path.extname(file)}`);` : This line constructs the path of the new file by joining the `screenshotFolder` variable with a new filename that includes the index (`i`) plus 1, and the original file extension. The new filename is enclosed in backticks (` `` `) to allow for string interpolation.
    
* `fs.rename(oldPath, newPath, err => {...});`: This line renames the original file to the new filename using the `fs.rename()` method. If there is an error, it is logged to the console.
    
* `console.log(`Screenshots file(${imageFiles.length}) Re-organization complete.`)`: This line logs a message to the console to show that the file renaming process is complete, along with the total number of files that were renamed.
    

That's all for the screenshot files counting, sorting and renaming process, the first two set goals have been achieved. The last one to talk to the registry to update it with the files we counted in the screenshot folder is all that's left.

**Talking to Windows registry to read and update windows screenshot counter value**

```javascript
    //REGISTRY UPDATE
    // Get the previous screenshot counter value from the registry
    regedit.list([keyPath], (err, result) => {
        if (err) {
        console.error(err);
        return;
        }
    
        const previousValue = result[keyPath].values['ScreenshotIndex'].value; //Previous Screenshot Value
        const newValue      = imageFiles.length; //New Value from Directory scan


        // Update the screenshot counter value in Windows' registry
        regedit.putValue({
                [keyPath]: {
                    'ScreenShotIndex': {
                        value: newValue,
                        type: 'REG_DWORD'
                    }
                }
            },(err) => {
            if (err) {
            console.error(err);
            return;
        }

            console.log(`\nRegistry Screenshot counter value updated from ${previousValue}, to a New value of ${newValue}.\n`);
        });
    
    });
```