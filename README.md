
# S3 Bucket -> Lambda Convert Markdown to HTML -> S3 Bucket

## Description

This is a serverless component that takes uploaded Markdown file from one S3 Bucket, converts them to an HTML document and uploads to another S3 Bucket. It contains:

- an Input S3 Bucket that accepts files.

- a Lambda that takes the Markdown file from the Input S3 bucket, converts it to a HTML one and uploads it to the Output S3 Bucket

- an Output S3 Bucket that receives files.

It's a Nuts & Bolts application component for AWS Serverless Application Repository.

## Deployment Parameters

This component has one CloudFormation deployment parameter:

- `ConversionTimeout`, an optional parameter, represents the timeout of the Conversion Lambda function. By default its 60 seconds.

## Latest Release - 1.0.0

Initial release.

## Roadmap - Upcoming changes

Here are the upcoming changes that I'll add to this serverless component:

- ESLint
- Tests