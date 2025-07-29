---
sidebar_position: 4
---
# Troubleshooting
If you encounter issues while using the Dinosaurs AI API, refer to the common problems and solutions below:
| Issue | Possible Cause | Solution |
|-------|----------------|----------|
| 401 Unauthorized | Missing or invalid API key | Verify your API key is included in the `Authorization` header.|
| 403 Forbidden | Insufficient permissions | Check your account role and access level for the endpoint.|
| 404 Not Found | Incorrect endpoint or resource missing | Make sure the API URL and parameters are correct.|
| 429 Rate Limit | Too many requests in a short time | Wait for a cooldown period (usually 60 seconds) and retry.|
| 500 Internal Server Error | API service is currently experiencing problems | Try again later or check the status page.|