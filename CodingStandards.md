# Coding Standards

Overview: https://www.browserstack.com/guide/coding-standards-best-practices

## Key Points

- Maintain uniformity of code styles by utilizing the relevant code formatters and linters. More specific recommendations may be found in [Languages](Frameworks.md)
- If a configuration file does not exist for a language/dialect that you intend to use:
    - Spaces, not tabs. Accommodate as many editors as possible.
    - Wrap lines to 80 characters, at most.
- Make use of type definitions wherever possible.
- Document as you code -- ideally, your commit should be accompanied by the relevant documentation changes.
- Err on the side of _more_ descriptive language:
    - DON'T: You can retrieve the data by `GET`ting the second endpoint.
    - DO: To retrive the data, send a `GET` request to `second/endpoint`.
- Documentation should include notes on how to reproduce environments reliably.
- Once you're done with the gruesome coding parts of your job, it helps to give your documentation a once-over for typos and grammatical error.

## Useful Links

- http://www.blackwasp.co.uk/gofpatterns.aspx
