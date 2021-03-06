![start2](https://cloud.githubusercontent.com/assets/10303538/6315586/9463fa5c-ba06-11e4-8f30-ce7d8219c27d.png)

# PharTools
A powerful PHP-CLI tool to create, extract and get info of phar files

## Category

PHP Command Line Interface script

## Requirements

PHP >= 5.3.0<br>

## Overview

**PharTools** is a powerful PHP-CLI tool to create, extract and get info of phar files

***Don't run this script directly. Run it from a cmd.exe or from a Linux Terminal instance instead***

***If you install PharTools on Windows directories (like Program Files, Program Files (x86), ...) you need to run cmd.exe as Administrator***

***To create phar files you need to set php.readonly to 0 in php.ini configuration***

## Documentation

**Configuration:**

###### Windows

To configure PharTools on Windows you need only to edit *%PHP_PATH* and *%PHP_EXE* variables in *phartools.cmd* file where *%PHP_PATH* must be the PHP binaries path and *%PHP_EXE* must be the main PHP executable file (usually *php.exe*)

###### Linux

On Linux, PharTools usually doesn't require to be configured but if you have some problems, edit *phartools.sh* file.

**Commands:**

If you are running PharTools on Windows you can simply run it calling *phartools.cmd* on Command Shell. On Linux you have to run phartools using *./phartools.sh* instead.

###### Create Phar:

To create phar files use the -c command

*phartools -c <source_path|source_file> <destination_phar> [options]*

**Options:**<br>
-c gzip|bzip2 Compress the phar file using gzip or bzip2 compression<br>
-m <metadata> Add metadata to the phar file (metadata format must be like 'key=>value,key2=>value2')<br>
-s <stub> Set stub string for the phar<br>
-r <regex> Include only files matching the regular expression<br>

**Example:**

phartools -c mysource myphar.phar (Windows)

./phartools.sh -c mysource myphar.phar (Linux)

###### Extract Phar:

To extract phar files use the -e command

*phartools -e <phar_file> [extract_directory]*

If *extract_directory* is not specified, files will be extracted in the current directory

**Example:**

phartools -e myphar.phar (Windows)

./phartools.sh -e myphar.phar (Linux)

###### Get Phar Info:

To get some infos about a phar file use the -i command. You will get the size, the signature, the signature type, metadata, the stub and some other infos about the specified phar file

*phartools -i <phar_file>*

**Example:**

phartools -i myphar.phar (Windows)

./phartools.sh -i myphar.phar (Linux)

###### Get PharTools Version:

*phartools -v*

**Example:**

phartools -v (Windows)

./phartools.sh -v (Linux)

## Available PharTools Downloads

**All platforms:**

PharTools_v1.0.zip (Only the script)

**Windows:**

PharTools_v1.0_win_installer (Preconfigured Script + Precompiled PHP binaries)
PharTools_v1.0_win_portable (Preconfigured Script + Precompiled PHP binaries, No Installer)

***Please note that precompiled PHP binaries provided in the Portable and Installer versions are provided with minimal extensions and configuration***

## Usage Example

###### Windows

*1. Open Windows Command Shell*<br>
![1](https://cloud.githubusercontent.com/assets/10297075/7434716/2d8a500c-f03d-11e4-84c2-9ef8ab6fee5d.png)<br>
*2. Go to PharTools directory*<br>
![2](https://cloud.githubusercontent.com/assets/10297075/7434729/61c77962-f03d-11e4-89cb-a78ba782f9be.png)<br>
*3. Run PharTools*<br>
![3](https://cloud.githubusercontent.com/assets/10297075/7434743/7b4bbf06-f03d-11e4-83df-493a92ac7075.png)<br>

###### Linux

*1. Open Linux Terminal*<br>
![1 2](https://cloud.githubusercontent.com/assets/10297075/7435028/12525408-f040-11e4-8cf5-94f6e1a18bce.png)<br>
*2. Go to PharTools directory*<br>
![2 2](https://cloud.githubusercontent.com/assets/10297075/7435029/12544d12-f040-11e4-9e9b-e6c44740926f.png)<br>
*3. Run PharTools*<br>
![3 2](https://cloud.githubusercontent.com/assets/10297075/7435030/126e09dc-f040-11e4-84f2-d4c19d9ee5ae.png)<br>

## Contributing

If you want to contribute to this project please follow the [Contribution Guidelines](https://github.com/EvolSoft/PharTools/blob/master/CONTRIBUTING.md)


