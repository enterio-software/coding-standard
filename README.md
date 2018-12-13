# Enterio Coding Standard
Enterio Coding Standard as PHPCS ruleset.

## Installation
Install the coding standard with the following command:

    composer require "enterio/coding-standard"

To use this coding standard in your project add the following phpcs.xml in the root directory:
```xml
<?xml version="1.0"?>
<ruleset>
    <arg name="basepath" value="."/>
    <arg name="extensions" value="php"/>
    <arg name="parallel" value="80"/>
    <arg name="cache" value=".phpcs-cache"/>
    <arg name="colors"/>

    <!-- Ignore warnings, show progress of the run and show sniff names -->
    <arg value="nps"/>

    <!-- Directories to be checked -->
    <file>src</file>
    <file>tests</file>

    <!-- Include full Doctrine Coding Standard -->
    <rule ref="Enterio"/>
</ruleset>
```

## Usage
You can check for violations with phpcs:

    vendor/bin/phpcs --standard=Enterio /path/to/file/to/validate
    
You can also do automatic fixes of violations with phpcbf:

    vendor/bin/phpcbf --standard=Enterio /path/to/file/to/validate
