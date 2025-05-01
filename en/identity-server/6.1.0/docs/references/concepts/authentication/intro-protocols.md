# Introduction to Authentication Protocols

## What is an authentication protocol?

A protocol is a set of pre-defined rules used when two or more parties communicate with each other. An authentication protocol
is a type of computer communications protocol that is designed to transfer authentication data between two or more entities.

---

## Password authentication protocol

This is one of the oldest protocols used for authentication. When
using this protocol, authentication happens using the typical **username
and password** approach. Although this approach is simple to use and
deploy, it has some security considerations. If a malicious user is able
to guess or obtain the password of a legitimate user, he/she will be able to 
access the system.

![password authentication]({{base_path}}/assets/img/concepts/password-authentication-protocol.png)

As a solution for the security issues raised for the typical password authentication protocol, advanced authentication protocols came into play in order to securely transmit authentication data between entities.

---

## Advanced authentication protocols

- [OpenID Connect](intro-oidc.md)
- [SAML 2.0](intro-saml.md)
<!-- - [NTLM](ntlm.md)-->
<!-- - [Kerberos](kerberos.md)-->
- [WS-Trust](intro-ws-trust.md)
- [WS-Federation](intro-ws-federation.md)
