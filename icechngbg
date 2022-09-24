#!/usr/bin/env node

var fs = require("fs");         //needed for file actions
const { exit } = require("process");
const readline = require('readline');   //needed to get user choice
const execSync = require('child_process').execSync; //to do CLI for img load

//set interface for user input
const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});

//What folder?  TODO, get as command line arg
const bgfolder = '/usr/share/backgrounds/fedora-workstation/';
let bglist = []; //empty array for list of bg images
let num = 1;    //number of file in menu


//Read folder and create menu
fs.readdir(bgfolder, (err, data) => {
    if(err) {
        return console.err(err);
    }
        //turn return data into an array of strings
        bglist = data.toString().split(',');

        //create menu
        bglist.forEach((file) => {
            
            console.log(num + ". " + file);
            num++;
        });

});


rl.question("Choose number of following file list:\n ", (choice) => {
    if(isNaN(choice) || choice < 0 || choice > num){
        console.log("Background has not been changed.");
        console.log("You might have entered the file name instead of menu number.");
        console.log("Or, you might have entered an out of range menu number.");
        rl.close();
        
    }else{
        var selection = bglist[choice - 1];
        execSync("icewmbg --image="+bgfolder+selection+" --center=1  --scaled=1")
        console.log("Background has been changed.");
        rl.close();
    }
});

rl.on('close', ()=>exit(0));
