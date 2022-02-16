# Exercise 11.1

Think about a hypothetical situation where we have an application being worked on by a team of about 6 people. The application is in active development and will be released soon.

Let us assume that the application is coded with some other language than
JavaScript/TypeScript, e.g. in Python, Java, or Ruby. You can freely pick the
language. This might even be a language you do not know much yourself.

---

### For a Python based application

What are the specific tools for taking care of these steps in the ecosystem of
the language you picked?

Linting:
- flake8
  - Finds style errors and reads out where they are coming from for you
- black
  - Isn’t a part of the standard Python library and doesn’t adhere 100% to PEP8 standards; however, it does do a phenomenal job at cleaning your code into a format that is easy to read and maintain
- pylint
  - Is a Python static code analysis tool which looks for programming errors, helps enforce a coding standard, sniffs for code smells and offers simple refactoring suggestions

Testing:
- pytest
  - Is a very easy to use and Pythonic testing library for Python projects
- codecov
  - which stands for “code coverage”, is a framework that keeps track of the percentage of lines of your code that are executed by your unit tests

Building:
- TravisCI
- CircleCI


Building:
- TravisCI
- CircleCI


What alternatives are there to set up the CI besides Jenkins and GitHub Actions?
- TravisCI
- CircleCI
- CodeShip
- Semaphore
- AWS CodePipeline
- Microsoft Team Foundation Server
- Oracle’s Hudson

Would this setup be better in a self-hosted or a cloud-based environment? Why? What information would you need to make that decision?

Cloud-based environment:

Pros
- No hardware or software infrastructure to maintain
- No need to worry about server maintenance or applying software updates/patches as they are handled by the CI/CD system
- Easy to set up

Cons
- Cost of usage may be high, especially with larger teams
- Not all services support all platforms, tools and environments - must make sure that technologies are supported by the CI/CD provider

Self-hosted environment:

Pros
- Extensibility - can be customized with plugins/extensions to enable functionality that is not included “out of the box”
- More support for development platforms, languages, and testing frameworks than many cloud-based options
- If there are no plugins/extensions available, you can usually make things work with some shell scripts

Cons
- You are required to manage your own infrastructure. This includes applying software updates/patches, and may include management of hardware.
- May require a time-intensive process to get set up. Between getting the system linked up to your VCS (Version Control System), issue/ticket tracking software, and notification system(s), there can be a steep entrypoint in getting your CI/CD system initialized.
- May be required to manage authentication and authorization for users in your organization if the system you choose doesn’t support your organization’s user management system (LDAP, Google GSuite, etc.)


## Reference
https://www.earthdatascience.org/blog/unit-testing-linting-ci-python/

https://medium.com/geekculture/build-a-python-ci-cd-system-code-quality-with-pylint-1b5e1a93de8d

https://www.parkmycloud.com/blog/ci-cd-saas-tool/
