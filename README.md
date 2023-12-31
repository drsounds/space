# Space Design Language

Space is a multi paradigm CSS theme like bootstrap that aims to use pure 100% non preprocessed CSS like SCSS and the cutting edge CSS technology.

The goal of this project is to create a native pure CSS framework which is modular set of design features and controlled by classes and CSS variables. Being pure standardized but yet flexible, this framework will be easy to set up and maintain in a wider scope of projects.

This project will support common denominators for common elements such button classes is both .btn-* and .button-* to make it easy to implement and the framework will follow Bootstrap's class naming conventions.

This framework will use bootstrap.grid only css for basic layou so we don't have to reinvent the wheel.

As this framework ditches preprocessed CSS like SCSS and PostCSS this framework will be extremely modular, as the imports is native CSS imports. The structure of the files is a tree meaning that developers can decide to only import a subset of the framework's features of components.
For those who want the advantage of precompiled CSS it is off course possible to import these CSS in a project that uses SCSS or Webpack, as scss and PostCSS can handle normal css too. Please note that you must adhere to the --* css variables and will be incompatible with SCSS variables

<img width="1128" alt="Skärmavbild 2023-12-10 kl  21 12 28" src="https://github.com/drsounds/space/assets/5108695/aa3f95d7-e299-4232-a325-6b1f4bc3379e">

# Folder structure

````

project_folder/
  css/
    index.css
    variables.css
    features/
       <feature name>/
          index.css
          variables.css
          components/
              index.css

````

Note: The scss folder with SCSS files was created in an earlier iteration before I decided to ditch sass and make a pure css native framework. I am in the process of porting these files to native CSS and once it is done the scss folder will be deleted.

# Features

The Space framework is modular in the sense it is built on a set of independent 'sub frameworks' aka 'features' which apply a cerain ui characteristic of styling like Skeudomorphic, flat, etc.

To use a feature, you will need to import the core style and the features you want to use like

````html

<link rel="stylesheet" href="<framework dir>/css/features/<feature id>/index.css">

<div class="sp-<feature id>">
... Your code
</div>

````

## Multiple features

It is possible to combine multiple features like this

````html
<html>
  <head>
    <link rel="stylesheet" href="<framework dir>/css/features/core/index.css">
    <link rel="stylesheet" href="<framework dir>/css/features/flat/index.css">
  </head>
  <body class="sp-core"> 
       <div class="sp-flat">
         ... Your code
       </div> 
  </body>
</html>
````

# License

MIT
