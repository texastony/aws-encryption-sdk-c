# Changelog

## 2.3.2 -- 2021-10-18

### Maintenance

* Mark high-memory proofs expensive ([#710](https://github.com/aws/aws-encryption-sdk-c/pull/710)) 
* Simplify / update build instructions ([#713](https://github.com/aws/aws-encryption-sdk-c/pull/713))
* Update submodules ([#726](https://github.com/aws/aws-encryption-sdk-c/pull/726)) 
* Remove OOM test, as OOM is no longer possible from aws allocators ([#728](https://github.com/aws/aws-encryption-sdk-c/pull/728)) 
* Pin newer aws-sdk-cpp in macOS CI builds ([#729](https://github.com/aws/aws-encryption-sdk-c/pull/729))

## 2.3.1 -- 2021-07-13

* Add [support policy](SUPPORT_POLICY.rst).
* Fix missing include in `kms_mrk_keyring.h` that could result in compilation failure.

## 2.3.0 -- 2021-06-16

- AWS KMS multi-Region Key support

  Added the new keyring KmsMrkAwareSymmetricKeyring that support AWS KMS
  multi-Region keys.
  Added the helper MultiKeyringBuilder that compose multiple
  KmsMrkAwareSymmetricKeyrings together to handle multiple CMKs.

  See https://docs.aws.amazon.com/kms/latest/developerguide/multi-region-keys-overview.html
  for more details about AWS KMS multi-Region Keys.
  See https://docs.aws.amazon.com/encryption-sdk/latest/developer-guide/configure.html#config-mrks
  for more details about how the AWS Encryption SDK interoperates
  with AWS KMS multi-Region keys.

## 2.2.0 -- 2021-05-27

* Improvements to the message decryption process.

  See <https://github.com/aws/aws-encryption-sdk-c/security/advisories/GHSA-r8cc-xhh9-rg65>

## 2.0.0 -- 2020-09-24

* Updates to the AWS Encryption SDK. c43d706

  This change includes fixes for issues that were reported by Thai Duong from
  Google's Security team, and for issues that were identified by AWS
  Cryptography.

  See: <https://docs.aws.amazon.com/encryption-sdk/latest/developer-guide/migration.html>

### BREAKING CHANGES

* AWS KMS KeyIDs must be specified explicitly or Discovery mode explicitly
  chosen.
* Key committing suites are now default.
* CommitmentPolicy requires commitment by default.

## 1.7.0 -- 2020-09-24

* Updates to the AWS Encryption SDK. 4ba5825

  This change includes fixes for issues that were reported by Thai Duong from
  Google's Security team, and for issues that were identified by AWS
  Cryptography.

  See: <https://docs.aws.amazon.com/encryption-sdk/latest/developer-guide/migration.html>

## 1.1.0 -- 2020-02-17

* Add security reporting instruction. (#467)
* Cbmc to master (#454)
* aws-cpp-sdk dependency bump to version 1.7.231

## 1.0.1 -- 2019-10-10
* Modified Doxygen config file to generate dependency graphs [#376](https://github.com/aws/aws-encryption-sdk-c/pull/376)
* Ran reformat [#426](https://github.com/aws/aws-encryption-sdk-c/pull/426)
* Strengthen memory_order for refcount_down [#433](https://github.com/aws/aws-encryption-sdk-c/pull/433)
* Update PR template [#391](https://github.com/aws/aws-encryption-sdk-c/pull/391)
* Refreshing the clang-format file and checking the version [#430](https://github.com/aws/aws-encryption-sdk-c/pull/430)
* Fix MultiKeyringNew proof so it runs again. [#444](https://github.com/aws/aws-encryption-sdk-c/pull/444)
* Windows build fixes [#446](https://github.com/aws/aws-encryption-sdk-c/pull/446)
* OSX build steps and README updates [#453](https://github.com/aws/aws-encryption-sdk-c/pull/)
* Fix duplicate in encryption context deserialization bug [#408](https://github.com/aws/aws-encryption-sdk-c/pull/408)
* Fix a bug where framefmt serialize returns a wrong ciphertext size [#385](https://github.com/aws/aws-encryption-sdk-c/pull/385)
* Fix: Improve initialization. [#451](https://github.com/aws/aws-encryption-sdk-c/pull/451)

## 1.0.0 -- 2019-05-20
* Changed links from awslabs to aws 
* Initial stable release 

## 0.2.0 -- 2019-05-13
* Added API function to make session from keyring
* Added API function to make caching CMM from keyring
* Added `_from_cmm` to end of `aws_cryptosdk_caching_cmm_new` function name
* Changed `aws_cryptosdk_session_get_algorithm` to `aws_cryptosdk_session_get_alg_id`
* Fixed HKDF bug

## 0.1.2 -- 2019-02-28
* Fixed empty string bug on git version of KMS user agent
* Local tests only by default
* Fix of MAP_ANONYMOUS issue for older Linuxes

## 0.1.1 -- 2019-02-21
* Fixed cmake bug regarding git version of KMS user agent
* Added CBMC header file needed by newer aws-c-common versions

## 0.1.0 -- 2019-02-05
* Initial public release
