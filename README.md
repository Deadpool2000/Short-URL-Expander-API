# Short URL Expander API

The **Short URL Expander API** allows you to expand shortened URLs and follow all possible redirections. This API is useful when you want to trace the final destination of a shortened URL.

## Features

- Expand shortened URLs
- Follow all possible redirections (3xx HTTP status codes)
- Get the final destination URL

## API Endpoints

### `GET /extract`

Expands a shortened URL by following all redirections until the final destination URL is reached.

#### Request

- **URL**: `/extract`
- **Method**: `GET`


#### Body Parameters:

| Parameter | Type   | Description                        | Required |
|-----------|--------|------------------------------------|----------|
| `url`     | string | The shortened URL to be expanded   | Yes      |

Example:

```
https://127.0.0.1:5000/expand?url=https://bit.ly/example
```
