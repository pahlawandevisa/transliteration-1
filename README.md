# Transliteration

PHP library for transliteration.

[![Scrutinizer Quality Score](https://img.shields.io/scrutinizer/g/fre5h/transliteration.svg?style=flat-square)](https://scrutinizer-ci.com/g/fre5h/transliteration/)
[![Build Status](https://img.shields.io/travis/fre5h/transliteration.svg?style=flat-square)](https://travis-ci.org/fre5h/transliteration)
[![CodeCov](https://img.shields.io/codecov/c/github/fre5h/transliteration.svg?style=flat-square)](https://codecov.io/github/fre5h/transliteration)
[![License](https://img.shields.io/packagist/l/fresh/transliteration.svg?style=flat-square)](https://packagist.org/packages/fresh/transliteration)
[![Latest Stable Version](https://img.shields.io/packagist/v/fresh/transliteration.svg?style=flat-square)](https://packagist.org/packages/fresh/transliteration)
[![Total Downloads](https://img.shields.io/packagist/dt/fresh/transliteration.svg?style=flat-square)](https://packagist.org/packages/fresh/transliteration)
[![Dependency Status](https://www.versioneye.com/user/projects/57b5b95e1dcdc900451877ef/badge.svg?style=flat-square)](https://www.versioneye.com/user/projects/57b5b95e1dcdc900451877ef)
[![SensioLabsInsight](https://img.shields.io/sensiolabs/i/ad4d26d5-cd6b-4fa6-8287-7d74234a2106.svg?style=flat-square)](https://insight.sensiolabs.com/projects/ad4d26d5-cd6b-4fa6-8287-7d74234a2106)
[![StyleCI](https://styleci.io/repos/15205247/shield?style=flat-square)](https://styleci.io/repos/15205247)
[![Gitter](https://img.shields.io/badge/gitter-join%20chat-brightgreen.svg?style=flat-square)](https://gitter.im/fre5h/transliteration)

## Requirements

* PHP 5.4 *and later*

## Install via Composer

```php composer.phar require fresh/transliteration='~1.1'```

## Available transliteration methods

<table>
    <thead>
        <tr>
            <th>From</th>
            <th>To</th>
            <th>Rules</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
                <img src="/resources/images/ukraine-flag.png" alt="Ukrainian" title="Ukrainian" />
                <br />
                Ukrainian
            </td>
            <td>
                <img src="/resources/images/united-kingdom-flag.png" alt="English" title="English" />
                <br />
                English
            </td>
            <td>
                Resolution of the Cabinet of Ministers of Ukraine №55 dated January 27, 2010
                <br />
                http://zakon1.rada.gov.ua/laws/show/55-2010-%D0%BF
            </td>
        </tr>
    </tbody>
</table>

## Using

```php
<?php

namespace Acme;

use Fresh\Transliteration\Transliterator;
use Fresh\Transliteration\UkrainianToEnglish;

class Foo
{
    public function bar($text)
    {
        // You can use in this way
        $transliterator = new Transliterator();
        $transliteratedText = $transliterator->ukToEn($text);

        // Or like this
        $transliteratedText = UkrainianToEnglish::transliterate($ukrainianText);
    }
}
```

## Some examples of *Ukrainian-to-English* transliteration

<table>
    <thead>
        <tr>
            <th>
                <img src="/resources/images/ukraine-flag.png" alt="Ukrainian" title="Ukrainian" />
                <br />
                Ukrainian text
            </th>
            <th>
                <img src="/resources/images/united-kingdom-flag.png" alt="English" title="English" />
                <br />
                Transliterated text
            </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Володимир</td>
            <td>Volodymyr</td>
        </tr>
        <tr>
            <td>Богдан</td>
            <td>Bohdan</td>
        </tr>
        <tr>
            <td>Жанна</td>
            <td>Zhanna</td>
        </tr>
        <tr>
            <td>Наталія</td>
            <td>Nataliia</td>
        </tr>
        <tr>
            <td>Олексій</td>
            <td>Oleksii</td>
        </tr>
        <tr>
            <td>Уляна</td>
            <td>Uliana</td>
        </tr>
        <tr>
            <td>Юрій</td>
            <td>Yurii</td>
        </tr>
    </tbody>
</table>

## Contributing

See [CONTRIBUTING](https://github.com/fre5h/transliteration/blob/master/CONTRIBUTING.md) file.
