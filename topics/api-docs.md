# API Overview

<!-- This document provides an introduction into your API. -->

## Introduction

The Payments SDK is a combination of hand-crafted, idiomatic interfaces to a few microservices that, in combination, provide secure,
malleable payment automation workflows for any kind of business process or transaction. Building upon the same ideas that your existing
codebase builds upon, we provide a reusable library of low-level actions, such as requesting a payment from a contactable entity, or
a wallet object that tracks funds for a user. The SDK enables you to map your business workflow onto those primitives without
ever seeming like you're making an API call.

## What you can do using this API

Provide some simple usage examples to help users get started quickly.

## Authentication

Our APIs all operate on the principle of least privilege - we utilise OAuth, and expect that the credentials used to call
most of our APIs are scoped down to a single user. For instance, when fetching the account balance of a user's wallet, we expect
the credentials to be issue via an OAuth authorization_code flow via a preregistered OAuth app client belonging to each tenant.

There are some APIs that are privileged in nature; for those, using an access token obtained via the client_credentials flow is appropriate.

## Base URL

|---------|-----------|
| Production | https://milestone.prod.hitchpin.zone |
| Staging | https://milestone.staging.hitchpin.zone |

## Rate Limiting

Explain any rate limiting policies, if applicable.

## Error Handling

Exceptions are documented where appropriate, and are always expressed via the [ProblemDetails](https://datatracker.ietf.org/doc/html/rfc7807) format.

## Versioning

Backwards incompatible changes will never be made. Before launch, the entire set of APIs will be placed under a v1 resource.
