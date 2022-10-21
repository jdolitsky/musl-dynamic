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
| `1.2.3-r1` `latest` | `sha256:fd06893b720ef1ee1720d38922f00338828eecf0774f297bb59ab38b2db7d7db`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:fd06893b720ef1ee1720d38922f00338828eecf0774f297bb59ab38b2db7d7db) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |


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
        "docker-manifest-digest": "sha256:fd06893b720ef1ee1720d38922f00338828eecf0774f297bb59ab38b2db7d7db"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "969c73ebe4900cd8008975c7e0fbfb1686ae91e6",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/musl-dynamic",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEUCIEc+piHFd3admvcfskNhcfygfQEB7lkHtPdGzjv5HB78AiEAr1b+mZFXa1mMOeWQ0nKKDdjZC2/idpM50wQcKHym898=",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiJmZTNkMzY4YjUyNTlhZDIxOGY1OTI2NzM4ZmZiN2NhMGJjMWMyODVhNWIxMDY1NzAwNmJmNjBkZTgxODYwZjMxIn19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJUURQQXI2dFFXWkNCVExvSi9Wb2FLNHhONjBYZW1tVEJTa1lycDdpdEEzYXB3SWdjQVFDT0hTWXI3Q3hOZmhkQTdjR1BLUmV2d1dpWmN1RkZXMHVrSW9scExRPSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUjFSRU5EUVhvMlowRjNTVUpCWjBsVlpWTTRkRmh6Um14WGVUQk5kamNyYTJkU1FpOVdjRWxFYm1abmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFFU1hkTlJFbDNUVlJKTkZkb1kwNU5ha2w0VFVSSmQwMUVTWGhOVkVrMFYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVZqT1UxMFp6bGtiM05CWTBaeVdITlJPVWRJY1hoVFV5OUxUVGhvZEZRclNXWkNUR0lLZERCMlJTOUtVbGxWVGpOc09HMUVVQ3R2UjNsUVZrdElOVmxSV0RVNVZtVjFXVTh3TVRsalZsUnBkbmxYWld0RFZFdFBRMEZzTUhkblowcGFUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlZ4WTFobUNubElORmRGTUZWaVdXcDBTSGhxWjFneWVpc3pXamRaZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDJKbldVUldVakJTUVZGSUwwSkhVWGRaYjFwbllVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5TVRGak1uZDBXa2hzZFZsWE1YQlplVGgxV2pKc01HRklWbWxNTTJSMlkyMTBiV0pIT1ROamVUbDVXbGQ0YkZsWVRteE1ibXhvQ21KWGVFRmpiVlp0WTNrNWIxcFhSbXRqZVRsMFdWZHNkVTFFYTBkRGFYTkhRVkZSUW1jM09IZEJVVVZGU3pKb01HUklRbnBQYVRoMlpFYzVjbHBYTkhVS1dWZE9NR0ZYT1hWamVUVnVZVmhTYjJSWFNqRmpNbFo1V1RJNWRXUkhWblZrUXpWcVlqSXdkMFpuV1V0TGQxbENRa0ZIUkhaNlFVSkJaMUZKWXpKT2J3cGFWMUl4WWtkVmQwNW5XVXRMZDFsQ1FrRkhSSFo2UVVKQmQxRnZUMVJaTlZsNlkzcGFWMHBzVGtScmQwMUhUbXRQUkVGM1QwUnJNMDVYVFROYVZFSnRDbGx0V21sTlZGazBUbTFHYkU5VVJteE9ha0ZqUW1kdmNrSm5SVVZCV1U4dlRVRkZSVUpCTlVSamJWWm9aRWRWWjFWdFZuTmFWMFo2V2xSQmMwSm5iM0lLUW1kRlJVRlpUeTlOUVVWR1FrSTFhbUZIUm5CaWJXUXhXVmhLYTB4WGJIUlpWMlJzWTNrNWRHUllUbk5NVjFJMVltMUdkR0ZYVFhkSVVWbExTM2RaUWdwQ1FVZEVkbnBCUWtKblVWQmpiVlp0WTNrNWIxcFhSbXRqZVRsMFdWZHNkVTFKUjB4Q1oyOXlRbWRGUlVGa1dqVkJaMUZEUWtnd1JXVjNRalZCU0dOQkNrTkhRMU00UTJoVEx6Sm9SakJrUm5KS05GTmpVbGRqV1hKQ1dUbDNlbXBUWW1WaE9FbG5XVEppTTBsQlFVRkhSRGg0TDBWS1owRkJRa0ZOUVZORVFrY0tRV2xGUVdwSGRrMXdPVVpGWnpac1dWb3JlSFkxUjBaQ2JERTRNakpxU1ZvNVJWRk1Ta3haZWxsalpFbENXRTFEU1ZGRGJuRmxVRlJNY0hkSWRGQjRjUXBwZUNzd09ITjNkMHh6WmtFMVN6Vm9XbEJXU0ZwNWFHTnNXV0prVkVSQlMwSm5aM0ZvYTJwUFVGRlJSRUYzVG05QlJFSnNRV3BDTkc0ME1YY3hiRTgzQ2tkTWRVczVWV2QzVFdrclRITXdVbmRFZDFGemRtaEZPRTFSYkV4T2MzUlhOazlrVlUxcldsbFdLMDlyWm1OWk1XdHZVVGxDYjJkRFRWRkVjVlI1T0UwS1lUWlpWMUpJZW5wSFNXWjVNbE4zVUZKS2VXWndWM2RaVFZGSmJsbEZWR2RHUm1kVFkzb3lVREIxV0d0aFJub3JWVEl2Wm5OT1JsRnhTRms5Q2kwdExTMHRSVTVFSUVORlVsUkpSa2xEUVZSRkxTMHRMUzBLIn19fX0=",
          "integratedTime": 1666231312,
          "logIndex": 5468042,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/musl-dynamic/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/musl-dynamic",
      "githubWorkflowSha": "969c73ebe4900cd8008975c7e0fbfb1686ae91e6",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3286288454",
      "sha": "969c73ebe4900cd8008975c7e0fbfb1686ae91e6"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

