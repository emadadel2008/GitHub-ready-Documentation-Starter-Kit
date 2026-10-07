# 02 - Project Overview

## Purpose

This document explains the project to someone who has never seen it before.

## Template

### Executive Summary

`<Project Name>` is a `<system/application/platform>` designed to `<business purpose>`.

### Business Problem

Describe the problem before describing the technology.

### Users

- Internal users
- Customers
- Administrators
- Automation / integrations

### Key Capabilities

1. Authentication
2. Order processing
3. Reporting
4. Notifications

### Scope

#### In Scope

- API
- Database
- Authentication
- Deployment pipeline

#### Out of Scope

- Customer billing platform
- Corporate identity platform

## Example

> The Orders API receives customer orders from the web application, validates them, stores them in PostgreSQL, and publishes an event for downstream fulfillment.

## Important

Avoid statements such as:

> "This is a highly available platform."

unless availability has actually been verified.

Prefer:

> "The application runs across two instances. High availability configuration requires validation against the production deployment."
