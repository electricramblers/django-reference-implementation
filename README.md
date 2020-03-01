# Project Purpose
This project is a reference implementation for a production-ready Django 
application with common use cases baked in. It is the base application that 
Simple CTO uses for its projects, and we hope that it can be helpful to you. 
It is quite opinionated as to its patterns, conventions, and library choices.

This is not prescriptive. That is to say that there are many ways to do 
build applications, and this is ours. You are welcome to fork, copy, and
imitate. We stand on the shoulders of giants, and you are welcome to as
well.

# Use cases covered
You will see a number of use cases covered:

  * Async tasks (sending email and sms, health-check PUSH)
  * Sending e-mail (with SMTP)
  * User Login, Logout, Registration, password reset (email, social)
  * Admin interface customization
  * Health-check (HEAD/GET used by Load Balancers)
  * Simple template tags (quick image thumbnails)
  * Serving static assets from Django vs. needing nginx/apache


# Project Principles

  * Use as little abstraction as possible. It should be easy to trace the code
    paths and see what is going on. Therefore, we will not be using too
    many advanced patterns, domains, and other things that create indirection.
  * [12-factor](https://12-factor.net) ready
  * Simplicity, with a path forward for scaling the parts you need.
  * Single developer friendly
  * Single machine friendly
  * Optimize for developer speed

## Requirements

  * Docker
  * Python 3.6 or later 
  * SMTP Credentials (I use Sendgrid)

# Developing locally
PyCharm's integration with the debugger and Docker leaves some things to be desired. 
This has changed how I work on the desktop. In short, I don't use docker for the django
part of development. I use the local development environment provided by MacOS.



## My Preferred developer stack

  * PyCharm (paid but community version is good, too)
  * Postgres installed via homebrew
  * Mailhog installed via Homebrew
  * Virtual environment


## Related projects

This project is tightly scoped to Django, but if you are interested
to learn more about a full production environment, then please refer
to this repo:

  * [simplecto/production-stack-template](https://github.com/simplecto/production-stack-template)
