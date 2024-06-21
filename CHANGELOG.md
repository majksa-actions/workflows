# Changelog

## [1.10.4](https://github.com/majksa-actions/workflows/compare/v1.10.3...v1.10.4) (2024-06-21)


### Bug Fixes

* also tag full version without v prefix ([093ae0f](https://github.com/majksa-actions/workflows/commit/093ae0f3ca1a17cbcdce3fbbbe794f8aaf61b924))

## [1.10.3](https://github.com/majksa-actions/workflows/compare/v1.10.2...v1.10.3) (2024-06-21)


### Bug Fixes

* rename action ([89989ec](https://github.com/majksa-actions/workflows/commit/89989ec9232137c1fd1da9eeb465a89c9deadbe3))

## [1.10.2](https://github.com/majksa-actions/workflows/compare/v1.10.1...v1.10.2) (2024-06-21)


### Bug Fixes

* after release please regex to match version with a slash ([9a54457](https://github.com/majksa-actions/workflows/commit/9a54457759fcecc2875f25be840269296a439f0c))

## [1.10.1](https://github.com/majksa-actions/workflows/compare/v1.10.0...v1.10.1) (2024-06-21)


### Bug Fixes

* remove requirement for PR reviews ([6f40d5d](https://github.com/majksa-actions/workflows/commit/6f40d5dd87ef690e7cb28c1ceef083ab2899b293))
* remove settings file ([#23](https://github.com/majksa-actions/workflows/issues/23)) ([b77fe1e](https://github.com/majksa-actions/workflows/commit/b77fe1e32dfc0ae33a18a7f42c0285f1fca91ad0))
* try setting restrictions ([8d5361f](https://github.com/majksa-actions/workflows/commit/8d5361f754b28896300a6ccc5cb573ead56788ed))

## [1.10.0](https://github.com/majksa-actions/workflows/compare/v1.9.1...v1.10.0) (2024-06-18)


### Features

* add after release please version tagger ([da2a2d5](https://github.com/majksa-actions/workflows/commit/da2a2d58eadca96691a93598514ef2967d2ef6d1))
* use cargo with cache ([5423edd](https://github.com/majksa-actions/workflows/commit/5423edd56e94dc14c72294e752eae46d4a4bb364))


### Bug Fixes

* change status checks ([635ddea](https://github.com/majksa-actions/workflows/commit/635ddeaabee1724fa00406ac8444abdc0c913694))
* **deps:** bump actions/checkout from 2 to 4 ([e32585a](https://github.com/majksa-actions/workflows/commit/e32585a2c745ef0a50c8840d6ab2a9fe55750748))
* **deps:** bump docker/build-push-action from 5 to 6 ([66f469e](https://github.com/majksa-actions/workflows/commit/66f469ebc0798a775122cee8c9b1008ce6dd67e8))
* **deps:** bump peter-evans/create-pull-request from 5 to 6 ([4b66c25](https://github.com/majksa-actions/workflows/commit/4b66c259a441939061aa8495198c8f1636791fb0))

## [1.9.1](https://github.com/majksa-actions/workflows/compare/v1.9.0...v1.9.1) (2024-05-11)


### Bug Fixes

* rename job ([eecb880](https://github.com/majksa-actions/workflows/commit/eecb8804a2610a639ae537820438adffdb9a3b20))

## [1.9.0](https://github.com/majksa-actions/workflows/compare/v1.8.2...v1.9.0) (2024-05-11)


### Features

* **rust-test:** add clippy check ([a1f2f30](https://github.com/majksa-actions/workflows/commit/a1f2f3082cea4c89ea1ab2c4f2bf916dbfa817e8))
* **rust-test:** run tests using nextest ([2d7ec54](https://github.com/majksa-actions/workflows/commit/2d7ec5466a65ba6bb1067bd98c95f545b65fbd5c))

## [1.8.2](https://github.com/majksa-actions/workflows/compare/v1.8.1...v1.8.2) (2024-05-11)


### Bug Fixes

* **rust-docs:** upgraded to use environment files ([9ae0ecb](https://github.com/majksa-actions/workflows/commit/9ae0ecb0df16c7c2f838d8662da8f7d6677ae8d6))

## [1.8.1](https://github.com/majksa-actions/workflows/compare/v1.8.0...v1.8.1) (2024-05-11)


### Bug Fixes

* **rust-docs:** deploy dependency ([333ff5d](https://github.com/majksa-actions/workflows/commit/333ff5d86268b4517b95f2c1bcc5804e7cb0a457))

## [1.8.0](https://github.com/majksa-actions/workflows/compare/v1.7.0...v1.8.0) (2024-05-11)


### Features

* **rust-docs:** publish docs to github pages ([0c6eb98](https://github.com/majksa-actions/workflows/commit/0c6eb98c3b5b00f1b867fe450b7513c24e3fb4a0))

## [1.7.0](https://github.com/majksa-actions/workflows/compare/v1.6.1...v1.7.0) (2024-05-11)


### Features

* **release-please:** add config-file ([ba84c68](https://github.com/majksa-actions/workflows/commit/ba84c6822cc590424db62d94c6de83d3fc2715f1))

## [1.6.1](https://github.com/majksa-actions/workflows/compare/v1.6.0...v1.6.1) (2024-03-19)


### Bug Fixes

* docker tags ([e7484e7](https://github.com/majksa-actions/workflows/commit/e7484e781203c2de196bd29972e13e5aca9c4f2b))

## [1.6.0](https://github.com/majksa-actions/workflows/compare/v1.5.0...v1.6.0) (2024-03-19)


### Features

* **docker:** add all platforms ([7569033](https://github.com/majksa-actions/workflows/commit/75690330843d5001709fdea533d052c5d4ebb703))

## [1.5.0](https://github.com/majksa-actions/workflows/compare/v1.4.0...v1.5.0) (2024-03-19)


### Features

* multi stage docker build ([ca90dc0](https://github.com/majksa-actions/workflows/commit/ca90dc019fa2464d82695c73313ba25be921192e))

## [1.4.0](https://github.com/majksa-actions/workflows/compare/v1.3.1...v1.4.0) (2024-03-02)


### Features

* create deployment manifest ([931d867](https://github.com/majksa-actions/workflows/commit/931d8679bed965b299a984ae5a1af6fe47da9c6a))

## [1.3.1](https://github.com/majksa-actions/workflows/compare/v1.3.0...v1.3.1) (2024-03-02)


### Bug Fixes

* update actions ([e106c14](https://github.com/majksa-actions/workflows/commit/e106c14ecd507c8f50bbf1d4cf464d7acb845d34))

## [1.3.0](https://github.com/majksa-actions/workflows/compare/v1.2.0...v1.3.0) (2024-03-01)


### Features

* add vitest ([cdbf38f](https://github.com/majksa-actions/workflows/commit/cdbf38f66722ac82c20ad1dc2fac86f0c5275484))

## [1.2.0](https://github.com/majksa-actions/workflows/compare/v1.1.1...v1.2.0) (2024-03-01)


### Features

* add biome reusable workflows ([e1527d6](https://github.com/majksa-actions/workflows/commit/e1527d63b2982ce1d3b4386ed46bf1dfbb6d98f8))

## [1.1.1](https://github.com/majksa-actions/workflows/compare/v1.1.0...v1.1.1) (2024-02-28)


### Bug Fixes

* features input should be array with one empty string, not empty array ([50338d0](https://github.com/majksa-actions/workflows/commit/50338d0c33864b03647a5ebf7010cbdff6ad4492))
* specify secrets manually ([2afc9e9](https://github.com/majksa-actions/workflows/commit/2afc9e98dd253b0d668fcf3d4bca5339c4e74f09))

## [1.1.0](https://github.com/majksa-actions/workflows/compare/v1.0.0...v1.1.0) (2024-02-28)


### Features

* add branch prefix input ([15bafc4](https://github.com/majksa-actions/workflows/commit/15bafc4872cde640639ba2be1206a1350d2facee))
* add portainer deploy ([f323a6b](https://github.com/majksa-actions/workflows/commit/f323a6b5d764bb60df1d89e5304184054de6f72e))
* linting prs validates single commits ([6045e2c](https://github.com/majksa-actions/workflows/commit/6045e2c22e2b428a64ced0ebe447c8462d6e83c8))
* rust specific actions ([0acb3eb](https://github.com/majksa-actions/workflows/commit/0acb3ebeea48b2fa1651249e607d82706b30fd2b))


### Bug Fixes

* use better github ref env variable ([8b0cd90](https://github.com/majksa-actions/workflows/commit/8b0cd9051d4e625a14594d30eecb7fecf28f8a52))

## 1.0.0 (2024-02-19)


### Features

* add docker build and push ([b9ab7aa](https://github.com/majksa-actions/workflows/commit/b9ab7aaba8adfd5be4f28024a1e6a5d8ee8fb54e))
* add release please ([7df25fb](https://github.com/majksa-actions/workflows/commit/7df25fb793afd6c472b007b2dc9c580c63977da9))
* add sematic pr ([60a50e8](https://github.com/majksa-actions/workflows/commit/60a50e83f975637382ae308b0758b3506fffd76d))
* update readme and tweak workflows ([614d51a](https://github.com/majksa-actions/workflows/commit/614d51a9470a81323e6354fd13f52b018f1b92cb))
