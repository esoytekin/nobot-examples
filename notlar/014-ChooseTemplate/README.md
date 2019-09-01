Dependencies:

- _colors_
- _readline-sync_
- _path_
- _fs-extra_

Requirements:

- hold templates directory in `templatesDir` local variable
- create templates array `fse.readdirSync`
- Prompt user to select one of the templates `readLineSync.keyInSelect(templates)`
    - if no choice is made, exit `process.exit(0)`
- Ask for the porject folder `readLineSync.question("What is the name of your game?",{limit:"", limitMessage:""})`
- Ask for confirmation to create folder with given name `readLineSync.keyInYN`
- if confirmed
    - get selected template
    - create src directory by joining templatesDir and template 
    - create dest directory [dirnme, projectName]
    - copy src to dest `fse.copy(src, dest).then().catch(err)`


