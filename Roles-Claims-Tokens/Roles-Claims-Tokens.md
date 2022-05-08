# Read 19: Roles, Claims, JWT Tokens

## Adding claims checks

Claim based authorization checks are declarative, a developer writes them into the code.

If the claim value isn't a single value, use "RequireAssertion"

## Introduction to Authentication

Authentication: Who you are.

Authorization: What you are allowed to do.

The "user" property is of type ClaimsPrincipal.

ASP.NET uses the concept of Claims-based-authentication.

Claims are essentially key value pairs

- DateOfBirth: date
- FirstName: firstName
- name: value.

These are about who a user is, not what a user can do.

Principal is the user.

## What is JWT

There are three parts to JWT: Head.Payload.Signature

Header: States and verifies algorithm and type.

Payload: contains the claims.

Signature: Calculated by encoding the header and payload and concatenating them wit ha period as a separator.

Server1(Consumer): Secret Key > Serer 3(Producer): valid response data > Server 2(consumer 2)

Steps in a contract

1. Share the secret.
2. Prepare the payload.
3. Get the token.
4. Identify the consumer.
