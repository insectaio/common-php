# insectaio/common

[![Latest Version](https://img.shields.io/packagist/v/insectaio/common.svg)](https://packagist.org/packages/insectaio/common)
[![Total Downloads](https://img.shields.io/packagist/dt/insectaio/common.svg)](https://packagist.org/packages/insectaio/common)

Protocol Buffers (Protobuf) shared types used across insectaio gRPC SDKs, including money and metadata types.

**Latest version: v1.0.1**

## Installation

```bash
composer require insectaio/common:^1.0
```

## Usage

This package provides generated PHP classes from [buf.build/insecta/common](https://buf.build/insecta/common).

```php
use Insecta\Common\Money;

$price = new Money();
$price->setCurrencyCode('USD');
$price->setUnits(25);
$price->setNanos(990000000);
```

## Autoload

```json
{
  "autoload": {
    "psr-4": {
      "Insecta\\Common\\": "generated/common_php/Insecta/Common/",
      "GPBMetadata\\": "generated/common_php/GPBMetadata/"
    }
  }
}
```

## Requirements

- PHP 8.0+
- [google/protobuf](https://github.com/protocolbuffers/protobuf) `^4.31`
- [grpc/grpc](https://github.com/grpc/grpc) `^1.57`

---

### License

MIT
