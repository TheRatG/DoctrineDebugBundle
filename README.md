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

<<<<<<< master
=======
use Symfony\Component\HttpKernel\Kernel;

class AppKernel extends Kernel
{
    public function registerBundles()
    {
        $bundles = [
            // ...
        ];

        if (in_array($this->getEnvironment(), ['dev', 'test'], true)) {
            // ...

            if ('dev' === $this->getEnvironment()) {
                $bundles[] = new Sensio\Bundle\GeneratorBundle\SensioGeneratorBundle();
                $bundles[] = new Symfony\Bundle\WebServerBundle\WebServerBundle();

                // HERE!
                $bundles[] = new Sidus\DoctrineDebugBundle\SidusDoctrineDebugBundle();
            }
        }

        return $bundles;
    }
    // ...
}
>>>>>>> master
```

## Changelog

### v1.0.2
Doesn't require xdebug to be installed anymore.

### v1.0.1
Fixing compatibility with Web Profiler 4
