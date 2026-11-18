---
name: "apitestcase-response-validator-skill"
description: "Create, review, and validate API test cases using Playwright JavaScript. Covers HTTP status codes, response headers, JSON structure, data types, business rules, negative scenarios, boundary conditions, and API response consistency."
version: "1.0.0"
author: "Tanu Priya"
license: "MIT"
tags:
  - api-testing
  - playwright
  - javascript
  - response-validation
  - json-schema
  - negative-testing
  - automation
---

# API Response Validator

## Purpose

Provide reusable guidelines for designing and implementing reliable API response validation in the existing Playwright JavaScript automation framework.

## When to Use

Use this skill when:
- Creating API test cases.
- Validating API response status codes and headers.
- Validating JSON response structures and data types.
- Testing business rules and calculations.
- Creating negative and boundary test scenarios.
- Reviewing or debugging API response assertions.

## Instructions

### 1. Understand the API Contract

Before creating tests:
- Identify the endpoint and HTTP method.
- Review request headers, parameters, and payload.
- Understand the expected response structure.
- Identify mandatory, optional, and nullable fields.
- Review documented business rules.
- Do not invent expected responses or API behaviour.

### 2. HTTP Response Validation

Validate:
- HTTP status code.
- Content-Type.
- Required response headers.
- Response body.
- Response time when performance requirements exist.

### 3. JSON Structure Validation

Validate:
- Required properties.
- Property names.
- Data types.
- Nested objects.
- Array structures.
- Null and optional values.
- Enum values.

### 4. Business Rule Validation

Validate:
- Calculated values.
- Minimum and maximum limits.
- Date and time rules.
- Relationships between fields.
- Pagination and sorting.
- Data consistency.

### 5. Negative Testing

Consider:
- Missing mandatory fields.
- Invalid data types.
- Invalid input formats.
- Unauthorized and forbidden requests.
- Invalid resource identifiers.
- Duplicate requests.
- Unsupported HTTP methods.
- Boundary violations.

### 6. Response Consistency

Where applicable, verify:
- Created resources can be retrieved.
- Updated values are reflected in subsequent requests.
- Deleted resources behave as expected.
- Pagination metadata matches returned data.
- Related API responses remain consistent.

### 7. Framework Integration

- Use JavaScript only.
- Follow the repository's `copilot-instructions.md`.
- Reuse existing fixtures and utilities.
- Use Playwright API testing capabilities.
- Use `expect` assertions.
- Avoid duplicate validation utilities.
- Keep endpoint-specific expectations close to the relevant tests or API service layer.
- Do not add dependencies without permission.

### 8. Failure Analysis

When a validation fails, investigate:
- Incorrect test data.
- Incorrect expected response.
- API contract changes.
- Backend defects.
- Authentication issues.
- Environment configuration.
- Data dependencies.

Never weaken assertions or change expected values just to make tests pass.

## Expected Deliverables

When generating API test cases, include:
1. Test scenario name.
2. API endpoint and HTTP method.
3. Preconditions.
4. Request details.
5. Expected status code.
6. Expected response structure.
7. Field-level validations.
8. Business rule validations.
9. Negative and boundary scenarios.

When implementing tests, execute them whenever possible and report actual results.

## Quality Standards

- Write independent and maintainable tests.
- Use meaningful test names.
- Validate more than HTTP status codes.
- Use deterministic test data.
- Avoid hardcoded credentials.
- Do not expose sensitive information in logs.
- Never hide application defects.

## Final Principle

A successful API test must validate the correctness of the response, not merely the successful execution of the HTTP request.