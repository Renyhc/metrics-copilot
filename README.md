# GitHub Copilot Metrics API

This API provides endpoints to retrieve GitHub Copilot usage metrics at different organizational levels.

## Setup and Installation

1. Clone the repository
2. Install dependencies:
```bash
npm install
```
3. Configure your environment variables in config/config.js:
   - ENTERPRISE
   - ORG
   - TEAM_SLUG
   - API_VERSION

4. Start the server:
```bash
npm start
```

## API Endpoints

### Enterprise Level Metrics

#### Get Enterprise Metrics
```http
GET /enterprises/{enterprise}/copilot/metrics
```
Returns Copilot usage metrics for the entire enterprise.

#### Get Enterprise Team Metrics
```http
GET /enterprises/{enterprise}/team/{team_slug}/copilot/metrics
```
Returns Copilot metrics for a specific team within the enterprise.

### Organization Level Metrics

#### Get Organization Metrics
```http
GET /orgs/{org}/copilot/metrics
```
Returns Copilot usage metrics for the entire organization.

#### Get Organization Team Metrics
```http
GET /orgs/{org}/team/{team_slug}/copilot/metrics
```
Returns Copilot metrics for a specific team within the organization.

## Response Format

All endpoints return JSON responses with Copilot usage metrics data.

## Error Handling

The API uses standard HTTP response codes:
- 200: Success
- 400: Bad Request
- 401: Unauthorized
- 403: Forbidden
- 404: Not Found
- 500: Internal Server Error

## Authentication

All requests require proper GitHub authentication headers.
