
# S3 Bucket -> Lambda (Pandoc Conversion) -> S3 bucket

## Description

This is a serverless component consisting of:

- an S3 Upload Bucket that accepts files.

  - `toEmails`, Array of strings, that represent all the emails you want to send an email to,
  - `subject`, a string representing the subject of the email
  - `message`, a string representing the message of the email, can be either HTML or regular text
  It also accepts two optional ones: `ccEmails` and `replyToEmails`, both of Array of strings type.

- a Lambda that sends an email to one or more specified email addresses. Also, depending if the `message` is in a Text or HTML format, it will send it in either of those formats. The `toEmails`,`ccEmails`, and `replyToEmails` parameters must be of Array type.

- an S3 Results Bucket that receives files.

It's a Nuts & Bolts application component for AWS Serverless Application Repository.

## Deployment Parameters

This component has two CloudFormation deployment parameters:

- `FromEmail`, a required parameter, represents the email sender. Must be a SES verified email. If you attempt to send email using a non-verified address or domain, the operation results in an "Email address not verified" error.
- `CorsOrigin`, an optional parameter, where you can restrict access to only specified domains.

## Latest Release - 1.0.0

Initial release.

## Roadmap - Upcoming changes

Here are the upcoming changes that I'll add to this serverless component:

- ESLint
- Tests