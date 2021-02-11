# OWASP

## About

Non-profit run by mostly volunteers

"We advocate approaching application security as a people, process, and technology problem, because the most effective approaches to application security require improvements in these areas."

## The top 10

A1 - Injection

A2 - Broken Authentication

A3: Sensitive Data Exposure (formerly cross site scripting XSS)

A4: XML External entities XXE

A5: Broken access control (merging of Insecure direct object reference and Missing function leve access contr)

A6: Security Misconfig (previously Sensitive data exposure)

A7: Cross-site scripting XSS

A8: Insecure Deserialization (previously CSRF)

A9: Using components with known vulnerabilities

A10: Insufficient logging & monitoring (previously unvalidaterd redirects and forwards)

## Injection

SQL, NoSql, OS, LDAP, XPath, SMTP headers, ORM queries, XML parsers. injection occur when untrusted data is sent to an interpreter as part of a command or query. The injected data tricks the interpreter into doing stuff you did not intend

- almost any source of data and be an injection vector

- Scanners and fuzzers can help attackers find injection flaws.

- vulnerable when:

  - User supplied data is not validated or sanitized
  - dynamic queries without context aware escaping (**what is this**)

- source code review is best way to prevent

- Thorough automated testing should include testing of all parameters, cookies, JSON, SOAP, and XML inputs

- static analyzers in the pipeline can help identify newly introduced injection vulnerabilities

- how to prevent

  - use an API or ORM if possible
  - don't escape column names, table names, etc - user supplied structure names are dangerous

  



