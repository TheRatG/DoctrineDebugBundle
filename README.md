Sidus/DoctrineDebugBundle Documentation
==================================

## Introduction

This bundle adds a stack trace to each doctrine query in the profiler.

![Example](Resources/documentation/exemple.png)

## Installation

### Require the bundle with composer:

````bash
$ composer require sidus/doctrine-debug-bundle:~1.0 --dev
````

### Add the bundle to config/bundles.php

```php
<?php
return [
    ///...
    Symfony\Bundle\WebProfilerBundle\WebProfilerBundle::class => ['dev' => true, 'test' => true],
    // HERE
    Sidus\DoctrineDebugBundle\SidusDoctrineDebugBundle::class => ['dev' => true],
    //...
];

```
