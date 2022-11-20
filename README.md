AWS CloudWatch bundle
=====================

[![Build Status](https://api.travis-ci.com/Ang3/aws-cloudwatch-bundle.svg?branch=main)](https://app.travis-ci.com/github/Ang3/aws-cloudwatch-bundle)
[![Latest Stable Version](https://poser.pugx.org/ang3/aws-cloudwatch-bundle/v/stable)](https://packagist.org/packages/ang3/aws-cloudwatch-bundle)
[![Latest Unstable Version](https://poser.pugx.org/ang3/aws-cloudwatch-bundle/v/unstable)](https://packagist.org/packages/ang3/aws-cloudwatch-bundle)
[![Total Downloads](https://poser.pugx.org/ang3/aws-cloudwatch-bundle/downloads)](https://packagist.org/packages/ang3/aws-cloudwatch-bundle)

This bundle integrates AWS CloudWatch to your Symfony project.

**Features**

- Client

Installation
============

Step 1: Download the Bundle
---------------------------

Open a command console, enter your app directory and execute the
following command to download the latest stable version of this bundle:

```console
$ composer require ang3/aws-cloudwatch-bundle
```

This command requires you to have Composer installed globally, as explained
in the [installation chapter](https://getcomposer.org/doc/00-intro.md)
of the Composer documentation.

Step 2: Configure the bundle
----------------------------

In file `.env`, add the contents below and adapt it to your needs:

```dotenv
###> ang3/aws-cloudwatch-bundle ###
AWS_CLOUDWATCH_KEY="YOUR_KEY"
AWS_CLOUDWATCH_SECRET="YOUR_SECRET"
AWS_CLOUDWATCH_REGION="YOUR_REGION"
AWS_CLOUDWATCH_VERSION="latest"
###< ang3/aws-cloudwatch-bundle ###
```

Make sure to replace `YOUR_KEY`, `YOUR_SECRET`, `YOUR_REGION` by your AWS settings.

Usage
=====

Client
------

**Public service ID:** `ang3.aws_cloud_watch.client`

To use the ```CloudWatch``` log client, get it by dependency injection:

```php
namespace App\Service;

use Aws\CloudWatchLogs\CloudWatchLogsClient;

class MyService
{
    public function __construct(private CloudWatchLogsClient $cloudWatchLogsClient)
    {
    }
}
```

That's it!