<<<<<<< HEAD
# Build an Alexa Skill using basic Python functions

![build-status](https://travis-ci.org/wray/alexa_python.svg?branch=master "build-status")
=======
# Build an Alexa Skill from a JSON file
>>>>>>> wray/s3

## What You Will Learn

This repo contains several branches with different python-based lambda
<<<<<<< HEAD
services and related skills intents and utterances that fulfill a basic facts-oriented skill. The example use
=======
services and related skills intents and utterances  that fulfill a basic facts-oriented skill. The example use
>>>>>>> wray/s3
case provides a simple Voice User Interface presence for a small
business. You know, just like every business needs a website, now
every business needs an Alexa Skill (Voice Site).

* Introduction to building an Alexa Skill without getting too much
into code.
* Voice User Interface (VUI) design
* SSML
* Lambda Services
<<<<<<< HEAD
* Simple Python functions
* S3 (on S3 branch)
=======
* S3
>>>>>>> wray/s3
* Optional Github to Cloud deployment via Travis

## What You Will Need

* [Amazon Developer Portal Account](http://developer.amazon.com)
* [Amazon Web Services Account](http://aws.amazon.com/)
<<<<<<< HEAD
* The sample code on [GitHub](https://github.com/techemstudios/alexa_python).

## What Your Skill Will Do

An Alexa skil built using a Python lambda function that delegates to a
simple Python file with a basic function for each intent.
=======
* The sample code on the s3 branch on
[GitHub](https://github.com/techemstudios/alexa_python).

## What Your Skill Will Do

An Alexa skil built using a Python lambda function that fetchs a JSON
file from S3 that encodes the responses for your intents.
>>>>>>> wray/s3

Suppose you name your skill ACME Inc., you will be able to interact
with your skill with phrases like, "Alexa, ask ACME Inc. for contact
info" or "Alexa, ask ACME Inc. for their upcoming events." or "Alexa,
ask ACME Inc. for general info about ACME." or "Alexa, tell me about
ACME Inc."

## Make it Your Own

By simply copying and pasting the
intentSchema and Utterances into the Skill builder, you can create the
<<<<<<< HEAD
lambda, zip the code in src and upload into your configured lambda and you can quickly have
a working skill.

You can then easily update the responses in your my_py.py file and
re-test your skill.
=======
lambda, copy and paste the code into your configured lambda, give the
lambda role read permissions to your S3, create the "alexa-python-biz"
bucket and upload the "discplines.json" there and you can quickly have
a working skill.

You can then easily update the responses in your JSON file, upload
again to S3 and modify your skill.
>>>>>>> wray/s3

Update the invocation name to a different business and match your
response to provide relevant information for the business.

But, wait, that's not all. Go ahead and completely change the skill to
a different set of information for something different. Change your
invocation to brew facts and create different/new intents and
utterances to for randomFacts, localBeers, etc. And then you'll
quickly be ready to start using parameters to make things even more
dynamic (watch here for the parameter version).

So, as long as you keep your JSON intents in sync with your skill intentSchema, you can
<<<<<<< HEAD
simply update or add intents as functions in the my_py file and the lambda service will use them.
=======
simply update or add intents to the JSON file in S3 and the lambda service will use them.
>>>>>>> wray/s3
Intents in your Schema may be mixed case -- this code will convert to lower case.

### Cloud CI/CD with Travis

This repo includes a .travis.yml file ready to be updated to
facilitate updating your lambda and your JSON as you make changes and
push to github.

If you fork this repo or create your own copy and keep it as a public repo, you can use
<<<<<<< HEAD
Travis to deploy to your lambda. You'll want to change the following configs:
=======
Travis to deploy to your lambda/S3. You'll want to change the following configs:
>>>>>>> wray/s3

* in deploy-provider: lambda
  * function_name
  * role
  * access_key_id (available from AWS console)
<<<<<<< HEAD
  * secret_access_key (also available from AWS console, but make sure you use travis command line to encrypt your key)

=======
  * secret_access_key (also available from AWS console, but make sure you use travis command
  * line to encrypt your key)

* in deploy-provider: s3
  * bucket (if you have changed it)
  * access_key_id (can use the same one as above)
  * secret_access_key (also use the same one as above)
>>>>>>> wray/s3
