## how to import fs module
    const fs = require('fs');
    const path = require('path');


## Create folder

    fs.mkdir(path.join(__dirname,'/test'),{},err=>{
        if(err) throw err;
        console.log("folder created");
    })

## create and write to file
    fs.writeFile(
        path.join(__dirname,'/test', 'hello.txt'),
        'Hello world',
        err=>{
        if(err) throw err;
        console.log("folder created");
    });

## append to file
    fs.appendFile(
        path.join(__dirname,'/test', 'hello.txt'),
        'I love node.js',
        err=>{
        if(err) throw err;
        console.log("folder created");
    });
## rename file

    fs.rename(
        path.join(__dirname,'/test', 'hello.txt'),
        path.join(__dirname,'/test', 'hell.txt'),
        (err)=>{
        if(err) throw err;
        console.log("renamed..");
    });


    