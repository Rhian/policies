# Development Security Guidelines

## Logging

- Do not log any sensitive user data without first performing both a risk assessment and a legitimate interest assessment, verified by the company DPO. Ideally all such decisions should be documented.
- Error messages containing stack traces or data dumps must **never** be revealed to a external user. This includes circumstances where one is debugging, guinea pigging, demonstrating, or screenshotting.

## Communication 

- Enforce secure communication. TLS is a must. No public endpoints should be available without TLS.
- Encrypt data in transit outside of internal VPCs. 
- Always authenticate requests.
- Do server-side validation.

## Understanding

- Know what strong encryption algorithms are, and what weak ones are; know what fast hashes are, and know what slow ones are; know the distinction between Cryptographically Secure Pseudorandom Number generators and Pseudorandom Number generators. Most crucially, know what each of these are used for and what they are not used for.
- Understand CORS, XSS, etc. Make sure you read and understood OWASP Top 10 vulnerabilities: <https://owasp.org/www-project-top-ten/>

## Utilities

- When typing in credentials of any form into your console, ensure that it isn't recorded in shell history. All machines in the Januus' `Core` have been configured to forego recall of commands that begin with whitespace.
- As a rule of thumb, maintain separation of concerns wherever possible.
- Do not make copies of things unless they absolutely need to be copied, even if one is convinced that it is only a temporary reprieve from a more tedious procedure.
- Maintain only local copies of data that needs to be immediately accessible. If data needs to be somewhere that is accessible from the wider internet, please have a chat about this with your colleagues.

## External Libraries

- Opt for pre-packaged solutions that come from recognized sources; pay heed to the quality of the maintenance of any library you use if it has the remotest security implications for us or our clients.
