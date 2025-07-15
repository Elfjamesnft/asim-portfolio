# API Documentation

## Overview
This document describes the REST API endpoints for the Asim Shaikh AI Portfolio application.

## Base URL
- **Development**: `http://localhost:5000`
- **Production**: `https://your-domain.com`

## Authentication
Currently, no authentication is required for public endpoints. Admin endpoints are protected by session-based authentication.

## Endpoints

### Contact Form

#### Submit Contact Form
Submit a new partnership inquiry from potential incubators.

**Endpoint**: `POST /api/contact`

**Request Body**:
```json
{
  "name": "string",
  "email": "string", 
  "company": "string",
  "message": "string"
}
```

**Validation Rules**:
- `name`: Required, minimum 1 character
- `email`: Required, valid email format
- `company`: Required, minimum 1 character  
- `message`: Required, minimum 10 characters

**Response**:
```json
{
  "id": 1,
  "name": "John Doe",
  "email": "john@example.com",
  "company": "Tech Incubator",
  "message": "We're interested in partnership opportunities...",
  "createdAt": "2025-01-15T10:30:00Z"
}
```

**Status Codes**:
- `201 Created` - Successfully submitted
- `400 Bad Request` - Validation error
- `500 Internal Server Error` - Server error

**Example Request**:
```bash
curl -X POST http://localhost:5000/api/contact \
  -H "Content-Type: application/json" \
  -d '{
    "name": "John Doe",
    "email": "john@incubator.com",
    "company": "Tech Incubator",
    "message": "We are interested in discussing partnership opportunities with your AI projects."
  }'
```

#### Get Contact Submissions
Retrieve all contact form submissions (admin only).

**Endpoint**: `GET /api/contact`

**Response**:
```json
[
  {
    "id": 1,
    "name": "John Doe",
    "email": "john@example.com",
    "company": "Tech Incubator",
    "message": "We're interested in partnership opportunities...",
    "createdAt": "2025-01-15T10:30:00Z"
  }
]
```

**Status Codes**:
- `200 OK` - Successfully retrieved
- `500 Internal Server Error` - Server error

**Example Request**:
```bash
curl -X GET http://localhost:5000/api/contact
```

## Error Handling

### Error Response Format
All errors return a consistent JSON structure:

```json
{
  "error": "Error message describing what went wrong",
  "details": "Additional details (optional)"
}
```

### Common Error Codes

#### 400 Bad Request
Returned when request data is invalid or missing required fields.

**Example**:
```json
{
  "error": "Validation failed",
  "details": "Email is required"
}
```

#### 404 Not Found
Returned when requested resource doesn't exist.

**Example**:
```json
{
  "error": "Not found",
  "details": "The requested endpoint does not exist"
}
```

#### 500 Internal Server Error
Returned when server encounters an unexpected error.

**Example**:
```json
{
  "error": "Internal server error",
  "details": "Database connection failed"
}
```

## Data Types

### ContactSubmission
```typescript
interface ContactSubmission {
  id: number;
  name: string;
  email: string;
  company: string;
  message: string;
  createdAt: Date;
}
```

### InsertContactSubmission
```typescript
interface InsertContactSubmission {
  name: string;
  email: string;
  company: string;
  message: string;
}
```

## Rate Limiting
Currently no rate limiting is implemented. Consider implementing rate limiting for production use to prevent abuse.

## CORS Policy
CORS is configured to allow requests from:
- Development: `http://localhost:5000`
- Production: Your deployed domain

## Content Type
All requests should use `Content-Type: application/json` header.

## Request/Response Examples

### Successful Contact Form Submission

**Request**:
```http
POST /api/contact HTTP/1.1
Host: localhost:5000
Content-Type: application/json

{
  "name": "Maria Garcia",
  "email": "maria@startup-incubator.com",
  "company": "Startup Incubator Italy",
  "message": "Hello Asim, we've reviewed your AI projects and are very interested in discussing potential partnership opportunities. Our incubator specializes in AI startups and we believe your projects align well with our investment thesis. Would you be available for a call next week?"
}
```

**Response**:
```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": 5,
  "name": "Maria Garcia",
  "email": "maria@startup-incubator.com",
  "company": "Startup Incubator Italy",
  "message": "Hello Asim, we've reviewed your AI projects and are very interested in discussing potential partnership opportunities. Our incubator specializes in AI startups and we believe your projects align well with our investment thesis. Would you be available for a call next week?",
  "createdAt": "2025-01-15T14:22:33.456Z"
}
```

### Validation Error Example

**Request**:
```http
POST /api/contact HTTP/1.1
Host: localhost:5000
Content-Type: application/json

{
  "name": "",
  "email": "invalid-email",
  "company": "Test Company",
  "message": "Short"
}
```

**Response**:
```http
HTTP/1.1 400 Bad Request
Content-Type: application/json

{
  "error": "Validation failed",
  "details": "Name is required, Email must be valid, Message must be at least 10 characters"
}
```

## Future Enhancements

### Planned Features
- User authentication system
- Admin dashboard for managing submissions
- Email notifications for new submissions
- Webhook support for external integrations
- Advanced filtering and search for submissions

### Security Enhancements
- API key authentication
- Rate limiting implementation
- Input sanitization
- CSRF protection
- Request logging and monitoring

## Testing the API

### Using curl
```bash
# Test contact form submission
curl -X POST http://localhost:5000/api/contact \
  -H "Content-Type: application/json" \
  -d '{"name":"Test User","email":"test@example.com","company":"Test Co","message":"This is a test message for the API"}'

# Test retrieving submissions
curl -X GET http://localhost:5000/api/contact
```

### Using Postman
1. Import the endpoints into Postman
2. Set the base URL to your environment
3. Add the appropriate headers and request body
4. Test different scenarios including validation errors

### Using JavaScript fetch
```javascript
// Submit contact form
const response = await fetch('/api/contact', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
  },
  body: JSON.stringify({
    name: 'Test User',
    email: 'test@example.com',
    company: 'Test Company',
    message: 'This is a test message'
  })
});

const data = await response.json();
console.log(data);
```

This API provides a simple, efficient way to handle contact form submissions while maintaining data integrity and proper error handling.
