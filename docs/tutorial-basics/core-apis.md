---
sidebar_position: 2
---
# Core APIs
`GET /v1/dinosaurs`

Fetch a list of dinosaurs by time period.

**Example Request**:

`GET /v1/dinosaurs?period=cretaceous`

**Example Response**:
```jsx title="example-responce.js"
[
  {
    "name": "Tyrannosaurus Rex",
    "period": "Cretaceous",
    "diet": "Carnivore",
    "length_m": 12.3
  }
]
```
`POST /v1/image/generate`

Generate an AI image of a dinosaur.

**Payload**:
```jsx title="Sample-code.js"
{
  "species": "Triceratops",
  "style": "realistic"
}
```
**Response**:
```jsx title-"Sample-response.js
{
  "image_url": "https://dinosaurs.ai/images/triceratops_23123.png"
}
```


## API Response Parameters

The following table describes the common parameters returned in API responses:

| Parameter | Type | Description | Required | Example |
|-----------|------|-------------|----------|---------|
| `id` | string | Unique identifier for the resource | Yes | `"dino_12345"` |
| `name` | string | Common name of the dinosaur species | Yes | `"Tyrannosaurus Rex"` |
| `scientific_name` | string | Scientific taxonomic name | No | `"Tyrannosaurus rex"` |
| `period` | string | Geological time period | Yes | `"Cretaceous"` |
| `era` | string | Geological era | No | `"Mesozoic"` |
| `diet` | string | Dietary classification | Yes | `"Carnivore"` |
| `length_m` | number | Length in meters | No | `12.3` |
| `height_m` | number | Height in meters | No | `4.5` |
| `weight_kg` | number | Estimated weight in kilograms | No | `7000` |
| `habitat` | string | Primary habitat type | No | `"Forest"` |
| `discovered_year` | integer | Year of first discovery | No | `1905` |
| `fossil_locations` | array | Array of discovery locations | No | `["Montana", "Alberta"]` |
| `confidence_score` | number | AI confidence rating (0-1) | Yes | `0.87` |
| `image_url` | string | URL to generated image | No | `"https://dinosaurs.ai/images/trex_001.png"` |
| `created_at` | string | ISO timestamp of record creation | Yes | `"2024-01-15T10:30:00Z"` |
| `updated_at` | string | ISO timestamp of last update | Yes | `"2024-01-15T10:30:00Z"` |

### Response Status Codes

| Status Code | Description | When It Occurs |
|-------------|-------------|----------------|
| `200` | Success | Request completed successfully |
| `201` | Created | Resource created successfully |
| `400` | Bad Request | Invalid parameters or malformed request |
| `401` | Unauthorized | Missing or invalid API key |
| `403` | Forbidden | Insufficient permissions |
| `404` | Not Found | Resource does not exist |
| `429` | Rate Limited | Too many requests |
| `500` | Internal Server Error | Server-side error occurred |