# musl-dynamic

<!---
Note: Do NOT edit directly, this file was generated using https://github.com/chainguard-images/readme-generator
-->

[![CI status](https://github.com/jdolitsky/musl-dynamic/actions/workflows/release.yaml/badge.svg)](https://github.com/jdolitsky/musl-dynamic/actions/workflows/release.yaml)

Base image with just enough files to run static binaries!<br/><br/>This image is meant to be used as a base image only, and is otherwise useless. It contains the `alpine-baselayout-data` package from Alpine, which is just a set of data files needed to support glibc and musl static binaries at runtime.<br/><br/>This image can be used with `ko build`, `docker`, etc, but is only suitable for running static binaries.

## Get It!

The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/musl-dynamic:latest
```

## Supported tags

| Tag | Digest | Arch |
| --- | ------ | ---- |
| `migration-20221118` | `sha256:93015eb394223d6305ae12b44781bc6c349db2f02ece7a9a147b3e07b8680d99`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:93015eb394223d6305ae12b44781bc6c349db2f02ece7a9a147b3e07b8680d99) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration` `migration-20221129` | `sha256:334ff88118d71756f09dc283ec606a97b684ad00ff5202c102198b3da3214184`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:334ff88118d71756f09dc283ec606a97b684ad00ff5202c102198b3da3214184) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration-20221122` | `sha256:c61266738c474e1110acb6c8936142a9ef42a41ad698b4991ef9f937467eb106`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:c61266738c474e1110acb6c8936142a9ef42a41ad698b4991ef9f937467eb106) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration-20221124` | `sha256:e4f8d28ee12b2673498f96d1eb87162b19bf985bb313a6976e027e617f452faf`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:e4f8d28ee12b2673498f96d1eb87162b19bf985bb313a6976e027e617f452faf) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration-20221120` | `sha256:d55a5a5ff0f7706bc2d8b80d4a2b71ea153214ce4d1296ecd322877baa590c2a`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:d55a5a5ff0f7706bc2d8b80d4a2b71ea153214ce4d1296ecd322877baa590c2a) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration-20221123` | `sha256:37fbfe0108235f0adaa7a584452864380bc9256c76d9a5468558ad1973e886ba`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:37fbfe0108235f0adaa7a584452864380bc9256c76d9a5468558ad1973e886ba) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration-20221127` | `sha256:86666e0339fbc3cfaa569b6bd19ef597c3b86688b99262e2e1b51a4db7f59cb4`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:86666e0339fbc3cfaa569b6bd19ef597c3b86688b99262e2e1b51a4db7f59cb4) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `1.2.3-r1` | `sha256:d90edc1058857946aa925234d35d1eb01d274c1645050ef55804adda1276f990`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:d90edc1058857946aa925234d35d1eb01d274c1645050ef55804adda1276f990) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `1.2.3-r2` | `sha256:c20eb50943802a18a47511dd7f4789794a46cc9f73c510cb3966b05fbb665a29`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:c20eb50943802a18a47511dd7f4789794a46cc9f73c510cb3966b05fbb665a29) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration-20221126` | `sha256:b692d71484c16bba2cb2e1f6e016c98cd237622bea47fad34a459d41e093be8a`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:b692d71484c16bba2cb2e1f6e016c98cd237622bea47fad34a459d41e093be8a) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `1` `1.2` `1.2.3` `1.2.3-r4` `latest` | `sha256:cca9d11ad009b989247df980df7a3a5fb8f475da44ac262a3a55d961e201f1fc`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:cca9d11ad009b989247df980df7a3a5fb8f475da44ac262a3a55d961e201f1fc) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration-20221119` | `sha256:6eb25a90a2192a54ddc27833030ee7bec506124b9c4869ea7256fedd1d871223`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:6eb25a90a2192a54ddc27833030ee7bec506124b9c4869ea7256fedd1d871223) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration-20221121` | `sha256:16982d648f4589e6304fc74535ecd36a79008e74c8e047fc4e6ef862f3a97827`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:16982d648f4589e6304fc74535ecd36a79008e74c8e047fc4e6ef862f3a97827) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration-20221125` | `sha256:9a40c87bda1610b396cda257e4bbc60c6589c3002e37d75e92553134b7c8d77a`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:9a40c87bda1610b396cda257e4bbc60c6589c3002e37d75e92553134b7c8d77a) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration-20221128` | `sha256:e2feccd04044ac5f7d00a3e59a1a15f8f5221d65b570d69164c9ff4f062a1358`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:e2feccd04044ac5f7d00a3e59a1a15f8f5221d65b570d69164c9ff4f062a1358) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |


## Usage

See the [examples/](./examples/) directory for
an example C program and associated Dockerfile
that can be used with this image.


## Signing

All Chainguard Images are signed using [Sigstore](https://sigstore.dev)!

<details>
<br/>
To verify the image, download <a href="https://github.com/sigstore/cosign">cosign</a> and run:

```
COSIGN_EXPERIMENTAL=1 cosign verify cgr.dev/chainguard/musl-dynamic:latest | jq
```

Output:
```
Verification for cgr.dev/chainguard/musl-dynamic:latest --
The following checks were performed on each of these signatures:
  - The cosign claims were validated
  - Existence of the claims in the transparency log was verified offline
  - Any certificates were verified against the Fulcio roots.
[
  {
    "critical": {
      "identity": {
        "docker-reference": "ghcr.io/chainguard-images/musl-dynamic"
      },
      "image": {
        "docker-manifest-digest": "sha256:cca9d11ad009b989247df980df7a3a5fb8f475da44ac262a3a55d961e201f1fc"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "push",
      "1.3.6.1.4.1.57264.1.3": "bdf7b9748989bdf4d43d08546b97dc28bc39b229",
      "1.3.6.1.4.1.57264.1.4": ".github/workflows/release.yaml",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/images",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEYCIQCW/KM9VcjRwRJ7SX7zZMaU/9vVRkYbQcjtOWu2Fr/5kAIhALYMCjlpgSS9b2b30t2YuUsDElK+65bfuiMw7ZKur9VH",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiJmY2JiN2IxNTM0MmYwMDBhMTU3Zjc2MmEwZTY0OGNkOTExNmY1ODVkZTNmNjllMWM0NGNiNzcyNTA2ZjA3YjdmIn19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FWUNJUUQyMmttbU9HMDN0NkJnUWMvU1Z1ZkVCQ0FqY0VjSythcWNCMENKV2JMdUZRSWhBSUYyR0RhSWJaUmxDVktrM0FQNzFnS0tKTlZMdFpvRmFOVlN0K0ZtZVVaUSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUjBha05EUVhveVowRjNTVUpCWjBsVlNteG9VbEZhV1RsdVVFWm1WM1Z2SzNWek0yZzFiVFZRZVV4emQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcE5kMDFVUlhoTmFrMTRUMVJOTkZkb1kwNU5hazEzVFZSRmVFMXFUWGxQVkUwMFYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVV3YURWd01UZFNWMDkzY25rM0wzVnBOVVF5V0N0eFpGQTBOMDE2YWt0SmMxQTJTbE1LUjNSU2VFZHZiSE5MTTNaeGJrVk1UbTF5ZGxBd2R6SjJiVlpzUjBWVGVTOTZTbFZyYm5sNmMwSnJNR1pCVFZjeFNuRlBRMEZzZDNkblowcFpUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlYyT0VwT0NpOUVObFpXWnpoQmJrUlFObFl2ZFZOV1VrdE9kRFpSZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDJGQldVUldVakJTUVZGSUwwSkdOSGRZU1ZwaFlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5YkhSWlYyUnNZM2s0ZFZveWJEQmhTRlpwVEROa2RtTnRkRzFpUnprelkzazVlVnBYZUd4WldFNXNURzVzYUdKWGVFRmpiVlp0Q21ONU9XOWFWMFpyWTNrNWRGbFhiSFZOUkd0SFEybHpSMEZSVVVKbk56aDNRVkZGUlVzeWFEQmtTRUo2VDJrNGRtUkhPWEphVnpSMVdWZE9NR0ZYT1hVS1kzazFibUZZVW05a1Ywb3hZekpXZVZreU9YVmtSMVoxWkVNMWFtSXlNSGRGWjFsTFMzZFpRa0pCUjBSMmVrRkNRV2RSUldOSVZucGhSRUV5UW1kdmNncENaMFZGUVZsUEwwMUJSVVJDUTJocFdrZFpNMWxxYXpOT1JHYzFUMFJzYVZwSFdUQmFSRkY2V2tSQk5FNVVVVEpaYW1zeldrZE5lVTlIU21wTmVteHBDazFxU1RWTlEzZEhRMmx6UjBGUlVVSm5OemgzUVZGUlJVaHBOVzVoV0ZKdlpGZEpkbVF5T1hsaE1scHpZak5rZWt3elNteGlSMVpvWXpKVmRXVlhSblFLWWtSQmJVSm5iM0pDWjBWRlFWbFBMMDFCUlVaQ1FtaHFZVWRHY0dKdFpERlpXRXByVEZkc2RGbFhaR3hqZVRsd1lsZEdibHBZVFhkSVVWbExTM2RaUWdwQ1FVZEVkbnBCUWtKblVWQmpiVlp0WTNrNWIxcFhSbXRqZVRsMFdWZHNkVTFKUjB0Q1oyOXlRbWRGUlVGa1dqVkJaMUZEUWtoM1JXVm5RalJCU0ZsQkNqTlVNSGRoYzJKSVJWUktha2RTTkdOdFYyTXpRWEZLUzFoeWFtVlFTek12YURSd2VXZERPSEEzYnpSQlFVRkhSbTk1U0VseWQwRkJRa0ZOUVZKNlFrWUtRV2xGUVc5T2FYSndSazl0TW5OYWNXOVlLMGRVU0UxaGRrSkNhazFvVG5sTU1WQlJSemw2YVNzd05uSmpjMVZEU1VodFlVc3JNVGszWkVwU09VWkZXZ3BpT1RSWVNubFZjSGxMVFhjMmJWWnFXRGN6V201cWRtVldXR0ZVVFVGdlIwTkRjVWRUVFRRNVFrRk5SRUV5WTBGTlIxRkRUVU5GTUdwck5XTkRVMjlHQ2xvMk9WQk5kM1ZTVWpSMWMweEVkMnhGWld3ek5qRkJVRGQxWWtSMFdHWTFSRXBNWmpSb1ZsUnZVM2RITHpOeWQyODRPSEJNUVVsM1RVbHdjVzExV1ZBS09VdHZNVTQzY3pKdk5FTktXRUpvYWs5SU9EWjRjRXRrYm5aRVFXeHVZVTl3WVVGWk9GUkRWMlZvYkhZM2IwdGplbTF5V2tSSGNXZ0tMUzB0TFMxRlRrUWdRMFZTVkVsR1NVTkJWRVV0TFMwdExRbz0ifX19fQ==",
          "integratedTime": 1673479213,
          "logIndex": 10981000,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/images/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": ".github/workflows/release.yaml",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/images",
      "githubWorkflowSha": "bdf7b9748989bdf4d43d08546b97dc28bc39b229",
      "githubWorkflowTrigger": "push",
      "run_attempt": "1",
      "run_id": "3897553673",
      "sha": "bdf7b9748989bdf4d43d08546b97dc28bc39b229"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

