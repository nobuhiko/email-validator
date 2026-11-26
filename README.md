# egulias/email-validator 1.2.15 running clean on PHP 7.4, for EC-CUBE 3.0.x

EC-CUBE 3.0.18 requires `egulias/email-validator` `^1.2`. 1.2.15 raises a notice on PHP 7.4. This fork keeps 1.2.15 and fixes it.

## Fixed

| Where | What |
|---|---|
| `Parser/Parser.php` | "Trying to access array offset on value of type null" when there is no previous token |

## Install

Requires Composer 2. In the shop's project root:

```
composer require umiushi-lab/email-validator:^1.2.15
```

The package `replace`s `egulias/email-validator` 1.2.15, so Composer removes the original and every other package keeps working against the same version.

## What this is, and is not

- The base is exactly the version EC-CUBE 3.0.18 ships. Nothing is upgraded; each fix is its own commit on the `eccube3/1.2` branch.
- Checked by running an EC-CUBE 3.0.18 shop (front pages, guest checkout to completion, contact form, admin screens) on PHP 7.1 and PHP 7.4 and comparing what PHP reports: with these changes PHP 7.4 reports nothing that PHP 7.1 does not.
- This is not an official release of the upstream project and is not supported by its maintainers. Upstream: https://github.com/egulias/EmailValidator
- EC-CUBE 3 が使っているバージョンのまま、PHP 7.4 で出る注意と警告だけを直したものです。保守: うみうしラボ
